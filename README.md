# SafeRoo Spark — Android Releases

Official Android APK distribution for [SafeRoo Spark](https://saferoo.app),
the child friendly chat application.

This repository **only hosts signed release APKs**. SafeRoo's
application source code is maintained in a separate private repository.

---

## Download

→ **[Latest release](../../releases/latest)**

For the friendliest install experience — including a QR code, step-by-step
instructions, and a system-requirements check — visit
**[saferoo-spark.app/download](https://saferoo-spark.app/download)**.

---

## Verifying your download

Each APK is published alongside a `.sha256` checksum file. Always verify
before installing — the only place we publish official APKs is this
repository, but checksums prevent accidents in transit.

**Linux / macOS**

```bash
sha256sum -c saferoo-standard.apk.sha256
```

**Windows PowerShell**

```powershell
$expected = (Get-Content .\saferoo-standard.apk.sha256).Split(' ')[0]
$actual   = (Get-FileHash .\saferoo-standard.apk -Algorithm SHA256).Hash.ToLower()
if ($expected -eq $actual) { 'OK' } else { 'MISMATCH — do not install' }
```

The Managed APK's SHA-256 is also embedded in every Managed Mode
provisioning QR — the Android setup wizard verifies it automatically
before installing.

---

## Installation

1. On the child's Android phone, enable **Settings → Apps → Special
   access → Install unknown apps → [your browser] → Allow** (the exact
   path varies by manufacturer; Android 8.0+).
2. Open the downloaded `.apk` file and follow the installer prompts.
3. Launch SafeRoo Spark

Full setup guide: **[saferoo.app/how-it-works](https://saferoo-spark.app/how-it-works)**.

---

## Compatibility

- Android 8.0 (Oreo) or newer
- ~50 MB free storage
- Most Android phones manufactured 2018 or later

---

## Release notes

Each release page on this repository includes a summary of user-visible
changes for that version. The complete changelog is maintained alongside
the application source.

---

## Support, privacy, terms

- **Get help / contact us:** [saferoo.app/contact](https://saferoo.app/contact)
- **Privacy policy:** [saferoo.app/privacy](https://saferoo.app/privacy)
- **Terms of service:** [saferoo.app/terms](https://saferoo.app/terms)
- **Data safety:** [saferoo.app/features](https://saferoo.app/features)

For bug reports about the app itself, please use the contact form linked
above rather than the Issues tab on this repo — that way we can route
the report to the right team and follow up directly.
