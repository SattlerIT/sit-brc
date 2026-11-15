# S-IT-BRC-Tools – Changelog

Alle wesentlichen Änderungen werden in dieser Datei dokumentiert.

---

## v4.0 – 2026-11-15

*Die deutsche Fassung dieses Abschnitts steht unter der englischen.*

Version 4.0 adds a second type of backup alongside the existing file
backup: the **backup to a single file (.brc)**, encrypted if you wish and
with several versions. In addition there are a new interface, eight
languages and a help with pictures.

### New – Backup to one file (.brc)
- The **“Type”** field defines for each profile how the backup is made:
  as a file backup as before, or as a Backup (.brc) in a single file
- Inside, the file is a standard ZIP archive: as long as it is not
  encrypted, it can be unpacked with any archive program via “Open with”,
  also without BRC
- Files that occur several times in one run are stored only once; the log
  states how much space this has saved
- Photos, videos, music, PDF and other formats that are already packed
  are stored without packing them again — this saves time
- A checksum is stored for every file
- A backup carries the extension .brc only when it has been written
  completely

### New – Encryption
- A Backup (.brc) can be encrypted with a password (**AES-256**); the
  names of the files and folders then cannot be read from outside either
- The password is entered twice; a password hint can be stored
- For scheduled backups BRC saves the password if you wish, bound to your
  Windows account on this PC
- There is no back door: without the password the backup cannot be opened

### New – Versions, Manage and Verify
- **“Keep”** defines for each profile how many backups are kept in the
  target folder; next to it you see how much space this is expected to
  need and how much is free at the target
- An older backup is removed only when the new one has been written
  completely
- Individual backups can be marked with **Retain**; they are then not
  removed by any run
- The **“Manage”** window shows the backups of a profile. “Verify” reads
  a backup completely and compares every file with its checksum; “Verify
  all” does this for all of them, one after the other
- The backup folders of the file backup with date can be managed there
  as well

### New – Backup register
- BRC keeps a register of when a backup was made, with which profile and
  to where; the Backup page names the last backup
- The search in it finds files by their name in all backups that are
  currently reachable, and names the drives that are not connected

### Restore
- From a Backup (.brc) you restore **individual folders or files**
  without unpacking the whole backup — selected by folder or from the
  list of all files, with a search by name
- **“Search backups”** finds the backups on the connected drives
- Restoring goes to the original location, to another system or to a
  freely selectable target folder; next to each ticked folder you see
  where it will be restored to
- For files that already exist at the target you choose the procedure:
  skip identical files, restore the file from the backup in addition, or
  overwrite the existing one
- Every restored file is compared with its checksum

### Cleanup
- For the file backup, Cleanup works as before
- For Backups (.brc), Cleanup shows the backups from the target folders
  of your profiles and, if you wish, searches a drive; for each backup it
  states whether its profile still exists or whether it comes from
  another PC
- Backups you no longer need are removed from there; those marked with
  Retain are kept

### OneDrive
- Folders that Windows has redirected to OneDrive are marked in the
  folder selection
- Files that exist only online in the cloud are downloaded by BRC for the
  backup; afterwards the space is released again
- If such a file cannot be downloaded, it is listed in the result and in
  the log
- Every folder is backed up only once, even if it is selected by several
  ticks — for example “Documents” inside OneDrive

### Scheduling and progress
- The schedule serves both types of backup
- New: **“Monthly”** with selectable days and the last day of the month
- For large files a second bar shows the progress of the current file;
  total amount, speed and remaining time are shown as well — also in the
  window of a scheduled backup

### New interface
- A sidebar leads to Overview, Backup, Restore and Cleanup
- The Overview states the last backup, the next one according to the
  schedule and the free space at the target
- Under “Config” there are five colour schemes to choose from, from light
  to dark, and the display size from 90 to 200 %

### Eight languages, help with pictures
- Program and help in Deutsch, English, Français, Español, Nederlands,
  Italiano, Polski and Hrvatski; the language can also be changed at the
  bottom right of the window
- The help begins with the workflow in seven steps; the page
  “S-IT-BRC – made simple” describes backing up to a USB stick or an
  external hard drive
- The pictures in the help show the program in the respective language
- Manual as a PDF in German and in English

### Installation
- One setup for both ways: **“Install”** with shortcuts and an entry in
  the Control Panel, or **“Portable”** into a folder of your choice, for
  example on a USB stick
- The setup recognises an installed version 3 and takes over profiles,
  your own restore targets, schedules and settings; beforehand they are
  additionally backed up
- When uninstalling, profiles, schedules and settings are backed up if
  you wish; a later new installation offers to restore them

---

## v4.0 – 2026-11-15 (Deutsch)

Version 4.0 stellt neben die bisherige Dateisicherung eine zweite Art von
Sicherung: das **Backup in eine einzige Datei (.brc)**, auf Wunsch
verschlüsselt und mit mehreren Versionen. Dazu kommen eine neue
Oberfläche, acht Sprachen und eine Hilfe mit Bildern.

### Neu – Backup in eine Datei (.brc)
- Das Feld **„Art“** legt je Profil fest, wie gesichert wird: als
  Dateisicherung wie bisher oder als Backup (.brc) in einer einzigen Datei
- Die Datei ist innen ein ZIP-Archiv nach Standard: Solange sie nicht
  verschlüsselt ist, lässt sie sich mit jedem Packprogramm über
  „Öffnen mit“ entpacken, auch ohne BRC
- Dateien, die in einem Lauf mehrfach vorkommen, werden nur einmal
  gespeichert; das Protokoll nennt den gesparten Platz
- Fotos, Videos, Musik, PDF und andere bereits gepackte Formate werden
  abgelegt, ohne sie nochmals zu packen — das spart Zeit
- Zu jeder Datei wird eine Prüfsumme gespeichert
- Eine Sicherung trägt die Endung .brc erst, wenn sie vollständig
  geschrieben ist

### Neu – Verschlüsselung
- Ein Backup (.brc) lässt sich mit einem Kennwort verschlüsseln
  (**AES-256**); auch die Namen der Dateien und Ordner sind dann von außen
  nicht lesbar
- Das Kennwort wird zweimal eingegeben; eine Merkhilfe kann hinterlegt
  werden
- Für Sicherungen nach Zeitplan speichert BRC das Kennwort auf Wunsch,
  gebunden an Ihr Windows-Konto auf diesem PC
- Eine Hintertür gibt es nicht: Ohne das Kennwort lässt sich die
  Sicherung nicht öffnen

### Neu – Versionen, Verwalten und Prüfen
- **„Behalten“** legt je Profil fest, wie viele Sicherungen im Zielordner
  erhalten bleiben — von „Nur letzte Sicherung“ bis „Letzte und drei
  vorherige“; daneben stehen der voraussichtliche Platzbedarf und der
  freie Platz am Ziel
- Eine ältere Sicherung wird erst entfernt, wenn die neue vollständig
  geschrieben ist
- Einzelne Sicherungen lassen sich zum **Aufbewahren** markieren; sie
  werden bei keinem Lauf entfernt
- Das Fenster **„Verwalten“** zeigt die Sicherungen eines Profils.
  „Prüfen“ liest eine Sicherung vollständig und vergleicht jede Datei mit
  ihrer Prüfsumme, „Alle prüfen“ tut das für alle nacheinander
- Auch die Sicherungsordner der Dateisicherung mit Datum lassen sich dort
  verwalten

### Neu – Sicherungsverzeichnis
- BRC führt ein Verzeichnis darüber, wann mit welchem Profil wohin
  gesichert wurde; die Backup-Seite nennt die letzte Sicherung
- Die Suche darin findet Dateien nach ihrem Namen in allen Sicherungen,
  die gerade erreichbar sind, und nennt die Laufwerke, die nicht
  angeschlossen sind

### Restore
- Aus einem Backup (.brc) holen Sie **einzelne Ordner oder Dateien**
  zurück, ohne die ganze Sicherung zu entpacken — Auswahl „Ordnerweise“
  oder über „Alle Dateien“, mit Suche nach Namen
- **„Sicherungen suchen“** findet die Sicherungen auf den angeschlossenen
  Laufwerken
- Zurückgeholt wird an den ursprünglichen Ort, auf ein anderes System oder
  in ein frei wählbares Zielverzeichnis; hinter jedem angehakten Ordner
  steht, wohin er zurückgeholt wird
- Für Dateien, die am Ziel schon vorhanden sind, wählen Sie das Verfahren:
  gleiche Dateien überspringen, die Datei aus dem Backup zusätzlich
  zurücksichern oder die vorhandene überschreiben
- Jede zurückgeholte Datei wird mit ihrer Prüfsumme verglichen

### Cleanup
- Für die Dateisicherung arbeitet Cleanup wie bisher
- Für Backups (.brc) zeigt Cleanup die Sicherungen aus den Zielordnern
  Ihrer Profile und durchsucht auf Wunsch ein Laufwerk; zu jeder Sicherung
  steht, ob ihr Profil noch vorhanden ist oder ob sie von einem anderen PC
  stammt
- Sicherungen, die Sie nicht mehr brauchen, entfernen Sie von dort aus;
  zum Aufbewahren markierte bleiben erhalten

### OneDrive
- Ordner, die Windows auf OneDrive umgeleitet hat, sind in der
  Ordnerauswahl gekennzeichnet
- Dateien, die nur online in der Cloud liegen, lädt BRC für die Sicherung
  herunter und gibt den Platz danach wieder frei
- Lässt sich eine solche Datei nicht herunterladen, steht sie im Ergebnis
  und im Protokoll
- Jeder Ordner wird nur einmal gesichert, auch wenn er über mehrere Haken
  ausgewählt ist — zum Beispiel „Dokumente“ innerhalb von OneDrive

### Zeitsteuerung und Fortschritt
- Der Zeitplan bedient beide Arten von Sicherung
- Neu ist **„Monatlich“** mit wählbaren Tagen und „Letzter Tag des Monats“
- Bei großen Dateien zeigt ein zweiter Balken den Stand der laufenden
  Datei; dazu stehen Gesamtmenge, Tempo und Restzeit da — auch im Fenster
  einer zeitgesteuerten Sicherung

### Neue Oberfläche
- Eine Seitenleiste führt zu Übersicht, Backup, Restore und Cleanup
- Die Übersicht nennt die letzte Sicherung, die nächste laut Zeitplan und
  den freien Platz am Ziel
- Unter „Konfig“ stehen fünf Farbschemata zur Wahl, von hell bis dunkel,
  und die Größe der Anzeige von 90 bis 200 %

### Acht Sprachen, Hilfe mit Bildern
- Programm und Hilfe in Deutsch, English, Français, Español, Nederlands,
  Italiano, Polski und Hrvatski; die Sprache lässt sich auch unten rechts
  im Fenster umstellen
- Die Hilfe beginnt mit dem Ablauf in sieben Schritten; die Seite
  „S-IT-BRC – ganz einfach“ beschreibt das Sichern auf einen USB-Stick
  oder eine externe Festplatte
- Die Bilder der Hilfe zeigen das Programm in der jeweiligen Sprache
- Handbuch als PDF auf Deutsch und auf Englisch

### Installation
- Ein Setup für beide Wege: **„Installieren“** mit Verknüpfungen und
  Eintrag in der Systemsteuerung oder **„Portabel“** in einen Ordner Ihrer
  Wahl, zum Beispiel auf einem USB-Stick
- Das Setup erkennt eine installierte Version 3 und übernimmt Profile,
  eigene Restore-Ziele, Zeitpläne und Einstellungen; vorher werden sie
  zusätzlich gesichert
- Bei der Deinstallation werden Profile, Zeitpläne und Einstellungen auf
  Wunsch gesichert; eine spätere Neuinstallation bietet an, sie
  zurückzuholen

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

## © 2026 Sattler IT-Service, Greifenstein · Hans Udo Sattler
