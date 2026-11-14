# Lernhilfs-Imperium – öffentliche Android-Updates

Dieses öffentliche Repository enthält ausschließlich veröffentlichte Android-APK-Updates für Lernhilfs-Imperium. Der App-Quellcode liegt weiterhin im privaten Hauptrepository.

## Updates

Die App prüft beim Start und über „Nach Updates suchen“ die [neueste GitHub-Veröffentlichung](https://github.com/Rogger00/Lernhilfs-Imperium-Updates/releases/latest). Sobald dort eine neue, korrekt signierte APK mit einem höheren Versions-Tag (z. B. `v0.1.42`) verfügbar ist, zeigt sie „Update herunterladen“ oder „Später“ an.

Die APKs werden ausschließlich über einen manuell ausgelösten GitHub-Actions-Build im privaten Hauptrepository erstellt. Für die automatische Veröffentlichung müssen dort die Actions-Secrets `UPDATES_REPO_TOKEN`, `ANDROID_KEYSTORE_BASE64`, `ANDROID_KEYSTORE_PASSWORD`, `ANDROID_KEY_ALIAS` und `ANDROID_KEY_PASSWORD` eingerichtet sein. Der Token benötigt Schreibzugriff auf die Releases dieses öffentlichen Repositorys.

**Wichtig:** Android kann eine bereits installierte APK nur direkt aktualisieren, wenn beide APKs mit demselben Schlüssel signiert sind. Bereits installierte Debug-Builds mit anderer Signatur müssen vor dem Wechsel auf die dauerhaft signierten Updates gegebenenfalls deinstalliert werden. Vorher lokale Lerndaten sichern.
