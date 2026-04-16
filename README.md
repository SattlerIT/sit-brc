# S-IT-BRC – Backup • Restore • Cleanup

Benutzerdaten sichern, wiederherstellen und inkrementelle Backups bereinigen.

Entwickelt von **Hans Udo Sattler · Sattler IT-Service, Greifenstein**

---

## Module

### 💾 Backup
Sichert persönliche Benutzerdaten (Desktop, Dokumente, Bilder, Musik, Videos, Downloads, AppData) auf ein externes Laufwerk – wahlweise inkrementell oder als vollständiges Archiv-Backup.

### 🔄 Restore
Stellt Daten aus einem Backup wieder her – in die Originalordner, in ein frei wählbares Zielverzeichnis, auf einen anderen PC oder direkt von einer ausgebauten Festplatte.

### 🧹 Cleanup
Bereinigt inkrementelle Backups von veralteten Dateien. Simulation vor dem echten Lauf möglich. Veraltete Dateien werden sicher in einen Archivordner verschoben, nicht gelöscht.

## Systemanforderungen

- Windows 10 oder Windows 11 (64-Bit)
- Administratorrechte werden beim Programmstart automatisch angefordert

## Installation

Das Setup (`S-IT-BRC-Setup.exe`) installiert das Programm wahlweise:
- **Festplatte** – mit Desktop-Verknüpfung, Startmenü-Eintrag und Deinstallations-Eintrag
- **Portabel** – auf USB-Stick oder beliebigen Ordner, ohne Systemeinträge

## Download

Aktuelle Version im [Release-Bereich](https://github.com/SattlerIT/sit-brc/releases).

> **Hinweis:** Windows SmartScreen oder Virenscanner können beim ersten Start anschlagen.  
> Dies ist ein bekanntes False Positive bei unabhängig entwickelten Windows-Tools.  
> Alle Dateien stammen ausschließlich von dieser offiziellen GitHub-Seite.

## Erwähnungen

- [Deskmodder.de](https://www.deskmodder.de/blog/2026/04/09/s-it-brc-backup-programm-mit-backup-restore-und-auch-einem-cleanup-tool/)

## Verwendete Komponenten

Dieses Programm verwendet **7-Zip** (als `S-IT-Expand.exe`) von Igor Pavlov zur Entpackung des Setup-Archivs.

- 7-Zip ist lizenziert unter der **GNU LGPL** und weiteren Open-Source-Lizenzen
- Lizenztext: siehe [`7zip-License.txt`](./7zip-License.txt) in diesem Repository
- Projektseite: https://www.7-zip.org

## Lizenz

© 2026 Hans Udo Sattler · Sattler IT-Service, Greifenstein  
Dieses Programm ist Freeware und darf kostenlos genutzt werden.  
Eine Weitergabe oder Veränderung ist ohne ausdrückliche Genehmigung nicht gestattet.

## Kontakt

**Sattler IT-Service**  
Hans Udo Sattler · Greifenstein  
kontakt@sattler-it.de  
http://sattler-it.de

