# S-IT-BRC-Tools – Changelog

Alle wesentlichen Änderungen werden in dieser Datei dokumentiert.

---

## v3.0.0.0 – 2026-08-09

Der Sprung auf 3.0 bringt zwei grundlegende Neuerungen: **Backup-Profile**
als gemeinsame Grundlage aller Einstellungen und die darauf aufsetzende
**automatische Zeitsteuerung**. Dazu kopiert die Engine jetzt blockweise,
und Restore wie Cleanup wurden überarbeitet.

### Neu – Backup-Profile
- Alle Einstellungen einer Sicherung (Laufwerk, Modus, Ordner, OneDrive,
  Zusatzverzeichnisse, Ausschlüsse) liegen in einem benannten **Profil**
  (`S-IT-BRC-Profile.ini`)
- Profilzeile mit **Speichern / Neu / Löschen**; die Auswahl lädt sofort,
  doppelte Namen werden abgelehnt
- Beim ersten Start entsteht automatisch ein Profil **Standard** aus den
  vorhandenen Einstellungen

### Neu – Automatische Zeitsteuerung
- **⏰ Zeitplan** im Backup-Modul: täglich, wöchentlich oder im Intervall,
  wahlweise still im Hintergrund; jeder Lauf lädt sein Profil frisch
- **Warteschlange**: Während eines Laufs fällige Termine starten unmittelbar
  danach, doppelte Termine desselben Profils werden verworfen; **⏹ Stopp
  bricht nur den laufenden Vorgang ab**
- Verpasste Termine (PC ausgeschaltet) werden am selben Tag nachgeholt;
  eigenes Protokoll `S-IT-Zeitsteuerung.log`
- **Autostart** nur, solange ein Zeitplan aktiv ist (unter *Ansicht*
  abschaltbar); das Fenster-X legt das Programm dann in den Infobereich
  (Systray), ein zweiter Programmstart holt die laufende Instanz nach vorn
- Abschlussfenster nächtlicher Läufe blockieren nicht — sie zeigen morgens
  der Reihe nach, was in der Nacht geschah

### Neu – Kopieren in Blöcken (Backup und Restore)
- Kopiert wird in Blöcken zu 1 MB statt Datei am Stück: **⏹ STOPP wirkt
  sofort**, auch mitten in einer großen Datei; Abgebrochenes wird entfernt
  statt als Bruchstück liegenzubleiben
- Fortschritt bewegt sich auch innerhalb großer Dateien, Anzeige von
  **Geschwindigkeit und Restzeit**

### Neu – Ausschlüsse und Speicherplatz-Prüfung
- Ausschlussliste je Profil mit 14 Vorgaben — Temp-Ordner, Caches,
  Papierkorb, `*.tmp` u. a. eingeschaltet; Abbilder, Archive, Videos und
  VM-Festplatten als echte Nutzdaten bewusst nicht — plus eigene Muster
- Vor dem Lauf Vergleich von freiem Platz und Schreibmenge; bei Enge
  Rückfrage mit exaktem Fehlbetrag, im zeitgesteuerten Lauf stattdessen
  Abbruch mit Protokolleintrag

### Restore – überarbeitet
- **Zielpfade sichtbar**: Jede Zeile zeigt Haken, Ordner und vollständigen
  Zielpfad; die Pfade wechseln live mit dem Ziel-Modus, Warnungen stehen
  direkt in der Zeile. Was angezeigt wird, ist genau das, was passiert
- **Klick auf den Zielpfad öffnet den Ordner im Explorer**
- **📌 Meine Ziele**: eigene Zielordner aus `S-IT-BRC-Ziele.ini`, mit
  Anzeige, ob sie gerade erreichbar sind (etwa USB-Platten)
- Log nennt Quelle **und Ziel** für jeden Posten; `-Rst`-Dateien werden
  mit vollem Pfad gelistet

### Cleanup – überarbeitet
- **🗄️ Altdateien im Archiv** werden im Programm angezeigt, neueste zuerst;
  **↩ Ausgewählte zurückholen** bringt einzelne Altdateien an ihren
  Ursprungsort zurück, die Zuordnung wird vorher angezeigt
- Simulation und echter Lauf sind eine ausdrückliche Auswahl; der
  Startknopf zeigt an, was er tut
- Analyse läuft im Hintergrund mit Fortschrittsanzeige; **⏹ STOPP** wirkt
  schon während der Zählung
- Zusatzverzeichnisse mit nicht erreichbarem Originalordner werden
  übersprungen statt vollständig ins Archiv verschoben

### Verbessert
- **Sieben** Zusatzverzeichnisse statt fünf — in Backup, Restore und Cleanup
- Backup-Seite als gleichmäßiges 2×2-Raster; Fenster startet breiter und
  weicht der Taskleiste aus; **Fenstergröße und Position merken**;
  zusätzliche Skalierungsstufe 90 %
- Eigenes Programmsymbol `BRC-Logo.ico`; lange Hinweiszeilen brechen um

### Behoben
- Ein späterer Backup-Lauf konnte die vermerkten Originalpfade der
  Zusatzverzeichnisse aus der Backup-INI entfernen — Restore und Cleanup
  fanden dann kein Ziel. Die Vermerke bleiben jetzt erhalten; fehlen sie
  in einem älteren Backup, ermittelt das Programm den Ort über die
  Backup-Profile und trägt ihn beim nächsten Lauf wieder ein
- Das Fenster eines aus dem Zeitplan gestarteten Laufs war nicht bedienbar,
  solange das Zeitplan-Fenster offen blieb; erneutes Öffnen des Zeitplans
  holt jetzt das vorhandene Fenster nach vorn statt ein zweites zu öffnen
- **⏹ STOPP war im Backup wirkungslos** — der Abbruch erreichte den
  Kopiervorgang nie
- Restore: Absturz im Modus „Gleicher PC"; Läufe nur mit einem
  Zusatzverzeichnis wurden abgelehnt; Zusatzverzeichnisse konnten ins
  Backup selbst zurückgeschrieben oder stillschweigend übersprungen werden
- Cleanup: Einfrieren bei Analyse und Archivliste; Zusatzverzeichnisse
  waren bei bereits eingetragenem Backup nicht auswählbar
- SCHLIESSEN auf der Backup-Seite funktionierte erst nach einem Lauf;
  Überschriften wurden ab 125 % Skalierung abgeschnitten; interne
  Fehlermeldungen beim Scrollen nach einem Seitenwechsel

---

## v2.2.0 – 2026-05-03

### Neu
- **Python/tkinter-Version**: Komplette Neuentwicklung in Python — ersetzt die bisherigen AutoIt-Module
- **DPI-Skalierung**: 100–200 % über den ⚙ Ansicht-Button einstellbar, persistent in `BRC-config.ini`
- **F11**: Header ein-/ausblenden für mehr Platz bei kleinen Bildschirmen
- **☑ Alle-Checkbox**: In Backup und Restore — alle Ordner auf einmal an-/abwählen
- **Zusatzverzeichnisse**: Bis zu 5 frei wählbare Ordner können gesichert, wiederhergestellt und bereinigt werden
- **OneDrive-Erkennung**: Automatisch aus der Registry; umgeleitete Pfade orange hervorgehoben
- **Auto-Button**: In Restore — durchsucht alle Laufwerke nach Backup-Ordnern (Archiv + Inkrement)
- **Lange Pfade**: Automatische Kürzung bei Pfaden > 259 Zeichen (Dateiendung bleibt erhalten)
- **Status-Anzeige**: Ordnername als Präfix — klar erkennbar welcher Ordner verarbeitet wird
- **Aussagekräftige Logs**: Pro Ordner Quelle, Neu/Übersprungen, Zusatzverzeichnisse

### Backup
- Echter Ordnername im Backup-Pfad (`\Extra\MeinOrdner\` statt `\Extra\Extra1\`)
- Zusatzpfade in `S-IT-Backup_SystemPaths.ini` unter `[ExtraPaths]` gespeichert
- OneDrive optional mitgesichert

### Restore
- Zusatzverzeichnisse aus INI angezeigt und gezielt wiederherstellbar
- Auto-Suche findet inkrementelle und Archiv-Backups
- AppData mit ⓘ-Tooltip statt langem Warntext
- Closure-Bug in Fehlermeldungen behoben
- `extra_paths` NameError behoben

### Cleanup
- Zusatzverzeichnisse in eigenem Kasten angezeigt, einzeln bereinigbar
- Optionen-Block zeigt Zusatzordner in eigener Zeile
- Jeder geprüfte Ordner im Log — auch ohne Verschobene

---

## v2.1.2 – 2026-04 (letzte AutoIt-Referenzversion)

- Alle vier AutoIt-Module auf gleichem Stand
- S-IT Corporate Design durchgängig
- Canvas+Scrollbar in allen Modulen
- Inkrementeller Vergleich per Dateigröße

---

## v1.x – 2025 (AutoIt, Ursprungsversion)

- Erste funktionsfähige Version als AutoIt-Paket
- Grundfunktionen Backup, Restore, Cleanup
