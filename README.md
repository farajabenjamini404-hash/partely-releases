Partely Releases

Public distribution repository for official Partely application updates.

Platforms

- **Android:** Signed APK release assets and the stable `android-update.json` manifest.
- **Windows:** MSI release assets and a separate Windows update manifest when the Phase 20 implementation and Phase 22 release contract are finalized.

Distribution rules

- Only officially approved release packages may be published.
- Android APKs must retain the permanent Partely production signing identity.
- Published update metadata must identify the correct platform, application version, download URL and SHA-256 checksum.
- Release assets must be downloadable without a GitHub login.
- A production manifest must not advertise an asset until it has been uploaded and verified.
- Never store application source code, signing keys, passwords, personal access tokens or customer data in this repository.

Android manifest

The planned stable manifest path is `android-update.json` on the `main` branch.

The Android client uses schema version 1, with the application ID `com.partely` and the `stable` release channel. The manifest contains the version code, version name, APK download URL, SHA-256 checksum, release notes and optional-update status.

The initial update policy is optional updates only.

`android-update.example.json`, if present, is documentation and test data. It is not a production update manifest.

## Release publishing

Phase 22 will establish the automated publishing process for approved releases, including package verification, release asset uploads, checksum calculation and manifest publication.

The stable manifest must be updated only after the corresponding release asset is available and verified.
