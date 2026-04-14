# VoxWzrd Releases

Public distribution artifacts for **VoxWzrd** — a meeting assistant for macOS and iOS that records, transcribes, and summarizes meetings with on-device or cloud AI.

The app source lives in a private repository. This repo exists solely to host signed, notarized release binaries so they can be fetched by Homebrew and direct download without authentication.

## Install

### Homebrew (recommended)

```
brew install --cask brndnsvr/tap/voxwzrd
```

This installs the latest notarized build of VoxWzrd.app into `/Applications/`. The cask lives in [brndnsvr/homebrew-tap](https://github.com/brndnsvr/homebrew-tap).

### Direct download

Grab the latest `.dmg` from the [Releases page](https://github.com/brndnsvr/VoxWzrd-releases/releases/latest), open it, and drag `VoxWzrd.app` to Applications.

### iOS

iOS builds ship via TestFlight, not this repo.

## Verifying a download

Each release's notes include the SHA256 checksum of the DMG. To verify:

```
shasum -a 256 VoxWzrd-v*.dmg
```

The output must match the `SHA256:` line in the release notes.

All DMGs are:
- Code-signed with a Developer ID Application certificate (Team `CMFBMNG959`, Brandon Seaver)
- Notarized by Apple
- Stapled, so Gatekeeper validates offline

## Uninstall

```
brew uninstall --cask brndnsvr/tap/voxwzrd
```

Or drag `VoxWzrd.app` to the Trash. To also clear app data and preferences, add `--zap`:

```
brew uninstall --zap --cask brndnsvr/tap/voxwzrd
```

## Questions, issues, feedback

File issues in this repo. Source access is by invitation.
