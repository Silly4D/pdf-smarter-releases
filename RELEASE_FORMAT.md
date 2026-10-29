# Stable release contract

A stable release uses the tag `vMAJOR.MINOR.PATCH-buildBUILD`, with numeric version components, no prerelease suffix, and a positive app build number. Publish the exact validated app version/build; never retag an older ZIP as a new version.

Required assets:

- `PDF-Smarter-MAJOR.MINOR.PATCH-buildBUILD-macOS-arm64.zip`
- That ZIP's `.sha256` checksum file.
- `update.json` with these fields:

| Field | Required value |
| --- | --- |
| `schema_version` | Integer `1` |
| `version` | Exact numeric `MAJOR.MINOR.PATCH` from the app bundle |
| `build` | Exact positive integer build from the app bundle |
| `minimum_macos` | Numeric minimum macOS version from the app bundle |
| `architecture` | `arm64` |
| `filename` | Exact versioned ZIP filename above |
| `sha256` | SHA-256 of that exact ZIP, 64 lowercase hexadecimal characters |

The release must be published, non-draft and non-prerelease. The ZIP and manifest must be uploaded to this repository's matching release. Missing/inconsistent metadata is not offered as an update. Future incompatible macOS requirements must be accurate.

The app checks GitHub's latest stable release, validates metadata, compares the installed numeric version/build and opens the matching GitHub release page only after a user action. It does not download or install the ZIP automatically. A checksum in metadata is not a claim that the app has downloaded or verified a ZIP, nor a substitute for Apple signing/notarization.

No documentation or placeholder represents a published app release. **Public binary publication is currently on hold pending the dependency distribution review.** Resolve licensing, validate the actual artifact and inspect all outgoing files before publishing.

Never place private source, user PDFs, preferences/history, environment files, credentials, signing identities, test keys or extracted proprietary fonts in this repository or its release assets. Do not copy an entire development workspace here.
