# SFM-Skripte für ATM 10 Aeronautics

Eine persönliche Bibliothek für **Super Factory Manager (SFM/SFML)** in **All the Mods 10: Aeronautics**.  
Ziel: Kopierbare Skripte, klare Mindestanforderungen, nachvollziehbare Änderungen.

> **Stand:** 04.11.2026. Diese Sammlung wurde aus den letzten Gesprächsfassungen erstellt. Die lokal in Minecraft gespeicherten Programme können durch eigene Änderungen neuer sein. Der Status wird daher pro Skript transparent ausgewiesen.

## Skripte

| Skript | Anlage | Funktionen | Status |
|---|---|---|---|
| [`01-latex-farm.sfm`](scripts/01-latex-farm.sfm) | Latex Farm | Redstone-Latex-Umschaltung, Dry Rubber | Nutzeranpassung übernommen |
| [`02-mob-farm.sfm`](scripts/02-mob-farm.sfm) | Mob Farm | Enchantments, Salvaging, Reject | **Entwurf / Löschrisiko** |
| [`03-hostile-neural-networks.sfm`](scripts/03-hostile-neural-networks.sfm) | HNN | Chambers, Matrices, Data Center | **Entwurf** |
| [`04-productive-bees.sfm`](scripts/04-productive-bees.sfm) | Productive Bees | Hive, Omega, Breeding, Gen-Mixing | Zusammengeführt / teils ungetestet |
| [`05-modern-industrialization.sfm`](scripts/05-modern-industrialization.sfm) | Modern Industrialization | Steam/Coke und zwei Maceratoren | Coke-Fix vom Nutzer bestätigt |
| [`06-draconic-fusion-crafting.sfm`](scripts/06-draconic-fusion-crafting.sfm) | Draconic Evolution | AE2 Processing, 12 Injectors | Funktion/FE-Optimierung bestätigt |

Die Skripte besitzen jeweils einen Kopfkommentar zu **Zweck, Mindest-Setup, Labels, Intervallen, Status und Besonderheiten**.

## Struktur

```text
sfm-atm10-aeronautics/
├── README.md
├── CHANGELOG.md
├── scripts/
│   ├── 01-latex-farm.sfm
│   ├── 02-mob-farm.sfm
│   ├── 03-hostile-neural-networks.sfm
│   ├── 04-productive-bees.sfm
│   ├── 05-modern-industrialization.sfm
│   └── 06-draconic-fusion-crafting.sfm
├── docs/
│   ├── konventionen.md
│   └── testcheckliste.md
└── templates/
    └── script-template.sfm
```

## Verwendung

1. Skript in `scripts/` öffnen und **nur den Dateiinhalt** kopieren.
2. In Minecraft die benötigten Maschinen über SFM-Kabel verbinden.
3. Labels mit der SFM Label Gun wie im Kopfkommentar vergeben.
4. Maschinen-Slots, Seiten, Upgrades und AE2-Einstellungen prüfen.
5. Mit kleinen Mengen testen; danach das Programm auf dem SFM Controller/Disk speichern.

## Neue Skripte hinzufügen

- `templates/script-template.sfm` kopieren und unter passendem Namen in `scripts/` ablegen.
- Kopfkommentar vollständig ausfüllen.
- **Getestet** erst vermerken, wenn das vollständige Skript ingame durchgelaufen ist.
- Im `CHANGELOG.md` Änderungen beschreiben.
- Bei riskanten Ausgaben (Trashcan, Lava, void etc.) zunächst einen sicheren Testpuffer verwenden.

## Versions- und Pack-Hinweise

- SFML-Kommentare beginnen mit `--`.
- Tags, Slots und IDs können sich durch Pack-/Mod-Updates ändern.
- Es gibt hier **keine automatisierten Ingame-Tests**; die Dateien sind reproduzierte Chat-Fassungen.
- Das AE2-Interface und ein gelabelter Flux Accessor können je nach Anlage unterschiedliche Energiequellen sein; die jeweiligen Kopfkommentare beachten.

## Referenzen

- [SFM Projekt](https://github.com/TeamDman/SuperFactoryManager)
- [GitHub: Neues Repository erstellen](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-new-repository)
- [GitHub: Dateien hochladen](https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository)
