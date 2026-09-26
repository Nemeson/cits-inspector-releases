# C-ITS Inspector 2.0 — Release Channel

Dieses Repository enthält ausschließlich **Release-Artefakte** des
C-ITS Inspector 2.0. Der Quellcode liegt in einem privaten Repository.

## Zweck

Dient als Update-Endpunkt für den integrierten Auto-Updater sowie als
Bezugsquelle für die Windows-Installer.

## Struktur

| Datei | Zweck |
|---|---|
| `latest.json` | Update-Manifest (wird von der Anwendung abgerufen) |
| `*_x64-setup.exe` | Windows-Installer (NSIS) |
| `*_x64-setup.exe.sig` | Minisign-Signatur des Installers |
| `*_x64_de-DE.msi` | Windows-Installer (MSI, de-DE) |
| `*_x64_de-DE.msi.sig` | Minisign-Signatur des MSI |

## Update-Endpunkt

Die Anwendung prüft:

```
https://github.com/Nemeson/cits-inspector-releases/releases/latest/download/latest.json
```

Ein Update wird nur installiert, wenn die Minisign-Signatur gegen den in der
Anwendung eingebetteten öffentlichen Schlüssel verifiziert. Ein manipulierter
Server oder ein gefälschtes Manifest kann kein Update einschleusen.

## Lizenz

Proprietary Commercial Software — Copyright (c) 2026 Kevin Seipel.
Alle Rechte vorbehalten. Der Download der Installer ist frei; die Nutzung
ist durch die Lizenzvereinbarung und einen gültigen Lizenzschlüssel geregelt.

Kontakt: vertrieb@seipel.uk