# PDF Smarter for macOS

Public downloads, release notes and checksums for the native PDF Smarter app. Application source and internal development records are maintained in a separate private repository.

**No application release has been published yet.** The download catalog is being prepared. The current development app includes third-party components whose distribution requirements must be resolved before a public binary is uploaded.

## Downloads

Approved downloads will appear on the [Releases page](https://github.com/Silly4D/pdf-smarter-releases/releases). Ordinary repository source archives are documentation only and do not contain the application.

The current target is Apple Silicon (ARM64), macOS 15 or later. Each release will state its actual compatibility, feature limits, signing/notarization status and SHA-256 checksum. A checksum identifies the downloaded bytes; it does not by itself certify Apple notarization.

## Update checks

Builds with update checking fetch public release metadata from this repository. They show an in-app notice on each launch when a newer compatible published release is available, and provide **Check for Updates…** manually. Startup checks can be disabled in app settings. PDFs and document details are not sent to GitHub. GitHub receives ordinary network request information when an update check runs; PDF processing itself works offline.

The app opens the verified GitHub release page when the user chooses to view an update. It does not silently download, replace or install applications.

Draft releases, prereleases and incomplete or incompatible release assets are not offered as stable updates. Future app releases must include a versioned ARM64 app ZIP, a checksum file and `update.json` matching the release tag. See [RELEASE_FORMAT.md](RELEASE_FORMAT.md).

## Distribution status

Public binary distribution is on hold pending the bundled dependency licensing review. This repository does not imply that the development build is licensed for closed-source public redistribution, Apple notarized, or qualified on every recipient Mac. No license purchase or commercial license claim is made here.
