# SentraAI Entrance – Releases

Öffentliche Update-Pakete (OTA) für die SentraAI-Zutrittskontrollsysteme.

## Überblick

Dieses Repository enthält ausschließlich Release-Pakete, keinen Quellcode. Jede Version erscheint als [GitHub-Release](../../releases) mit drei Dateien:

| Datei | Inhalt |
|-------|--------|
| `manifest.json` | Version, Prüfsumme (SHA-256), Signatur, Paketgröße und Änderungsliste |
| `sentra-update-<version>.tar.gz` | das Update-Paket |
| `sentra-update-<version>.tar.gz.sig` | Signatur des Pakets |

Die Änderungen der einzelnen Versionen stehen in den jeweiligen Release-Notizen. [`CHANGELOG.md`](CHANGELOG.md) enthält nur die frühe Historie (bis v2.0.9).

## So funktionieren Updates

1. Ein lizenziertes Gerät fragt dieses Repository regelmäßig (Standard: alle 6 Stunden) nach neuen Releases ab. Vorab-Versionen (als „Pre-release“ markiert) installiert es nur, wenn das ausdrücklich erlaubt ist.
2. Das Paket wird heruntergeladen und gegen die SHA-256-Prüfsumme und die Ed25519-Signatur geprüft. Ein Paket, das die Prüfung nicht besteht, wird nicht installiert.
3. Das Gerät sichert vor der Installation seinen Stand und prüft nach dem Neustart, ob es korrekt läuft. Schlägt das fehl, stellt es den vorherigen Stand automatisch wieder her.

## Für Geräte-Betreiber

Updates verwalten Sie im Dashboard des Geräts unter **System → Software-Updates**; dort starten Sie die Suche mit **Auf Updates prüfen**. Die Seite steht nur mit aktiver Lizenz zur Verfügung.
