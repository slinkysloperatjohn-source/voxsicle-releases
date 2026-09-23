# Voxsicle Releases

This repository distributes official release assets for **Voxsicle**, a local-first macOS studio for synthetic voice production.

Voxsicle combines a persistent Voice Library, local voice generation, long-form rendering, Dialogue Studio, pronunciation controls, production audio, and export tools in one desktop workspace. Voice references, generated audio, scripts, projects, and pronunciation data stay on your Mac.

> This is a release-assets repository. It does not contain the Voxsicle source code.

## Current platform

The current experimental release supports **macOS on Apple Silicon** only (M-series Macs).

Support for Intel Macs, Windows, and Linux is planned for a later release.

## Install Voxsicle

1. Open the latest release and download the `Voxsicle-1.3.9-arm64.dmg` asset.
2. Open the downloaded DMG.
3. Drag **Voxsicle** to the **Applications** folder.
4. Open the app from Applications.

The release app includes its local backend. End users do not need to install Python, pnpm, or any developer tools.

### macOS security notice

Early experimental builds may not yet be notarized by Apple. If macOS warns that it cannot verify the developer, make sure you downloaded the file from this repository's official release assets. Then Control-click the app in Applications, choose **Open**, and confirm the dialog. Do not lower macOS's global security settings.

## Local-first by design

Voxsicle does not use cloud inference, accounts, or telemetry. The desktop app keeps voice recordings, generated audio, scripts, projects, and pronunciation data locally on the device.

Models are never downloaded silently. Open **Models** in Voxsicle and choose **Install model** only for the local engines you want to use. Depending on the selected engine, the initial download can be several gigabytes and may take some time.

## First steps

1. Open **Voices** and create a Voice Profile.
2. Import recordings that you are allowed to use as references.
3. Review the references and optionally choose one as the preferred sample.
4. Open **Models** and explicitly install a local engine.
5. Open **Speak**, select the Voice Profile and an installed engine, then create a render.

Use only voices, recordings, and scripts that you have permission to process. Results depend on the quality of the source material and the selected local model.

## Included asset

| Asset | Purpose |
| --- | --- |
| `Voxsicle-1.3.9-arm64.dmg` | The desktop application installer for Apple Silicon Macs. |

If a SHA-256 checksum file is attached to a release, verify the downloaded asset before opening it:

```bash
shasum -a 256 "Voxsicle-1.3.9-arm64.dmg"
```

## Your local data

On macOS, Voxsicle stores its managed data in:

```text
~/Library/Application Support/Voxsicle/
```

That location can contain Voice Profiles, reference audio, generated takes, exports, model files, backups, and settings. Removing the app from Applications does not automatically remove those files. Use the application's backup and library tools before deleting local data.

## Experimental release notice

Voxsicle is free to use and still evolving. Keep backups of important recordings and exports, and expect first-release limitations while the product and platform support continue to develop.
