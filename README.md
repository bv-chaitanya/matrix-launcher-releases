# Matrix Launcher — public release mirror

Public mirror of Matrix Launcher releases. The source code lives in the
private `matrix-launcher-compose` repo; this repo carries only the built
APKs and a machine-readable `latest.json` so the launcher itself can check
for updates without any login.

- `latest.json` — latest version: `versionName`, `versionCode`, `apkUrl`,
  `sha256`, and release notes.
- `Matrix-Launcher-vX.Y.Z.apk` — the release APK, signed with the same
  permanent release key as every Matrix release, so it installs as an
  update over any earlier version.

The launcher verifies the downloaded APK's SHA-256 against `latest.json`
before installing, and Android itself refuses an update signed with a
different key.
