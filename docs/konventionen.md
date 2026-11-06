# Konventionen

## Kopfkommentar (Pflicht)

Jedes `.sfm`-Programm hat vor `NAME` diese Angaben:

1. **Zweck:** Was wird automatisch verarbeitet?
2. **Mindest-Setup:** Maschinen und Hilfsblöcke ohne optionale Erweiterungen.
3. **Labels:** Exakte Namen der SFM Label Gun.
4. **Ausführung:** Trigger und Tick-Offset.
5. **Status:** Entwurf, teilweise getestet oder getestet.
6. **Hinweise:** Seiten, Slots, Filter, Risiken und besondere AE2-Einstellungen.

## Transport-/Performance-Prinzipien

- FE nur so häufig wie nötig, bei Hochlast ggf. jede Tick.
- Laufende Versorgung bevorzugt 20 Ticks.
- Langsame Ausgaben auf `EVERY 60 GLOBAL PLUS 5 TICKS DO` oder andere, bewusst verteilte Zeitpunkte legen.
- Für MI: **Auto-Output wo direkt möglich**, SFM für Steuerung und entfernte Transfers; keine Functional Storage Puller Upgrades.
- `FORGET` als Grenze zwischen logisch getrennten Ressourcen verwenden.
- Bei großen Speichern gezielte Item-IDs/Tags einsetzen; ungefilterte Zugriffe nur mit Messung beurteilen.
- Fehlersichere Transfers höher priorisieren als kurze Skripte.

## Praxisbefunde

- **MI Coke:** `INPUT 16 modern_industrialization:coke FROM storage` + `OUTPUT TO EACH macerator TOP SIDE` funktioniert. `RETAIN` ohne explizite Seite funktionierte nicht; Ursache wurde nicht isoliert.
- **Draconic FE:** `INPUT fe:: FROM interface` und `OUTPUT fe:: TO injector EACH SIDE` reichen aus. Keine Mehrfach-Ausgaben benötigt.
- **Latex:** Dry Rubber wird beim Nutzer über `INPUT FROM processor BOTTOM SIDE` entnommen.

## Sicherheitsregeln

- `trash` am Anfang als **Reject-Chest**, nicht als echte Trashcan, anschließen.
- Übertragungen in die Drawers oder AE2 zuerst mit wenigen Items testen.
- Verarbeitungsschritte mit mehreren Inputs nicht starten, bevor das ganze Rezept vorbereitet ist.
- Eigenständige, ingame funktionierende Fassungen haben Vorrang gegenüber Chat-Entwürfen.
