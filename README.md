<div align="center">

![WallpaperJS — Your desktop. Your code.](banner.svg)

# WallpaperJS

**Your desktop, written in HTML · CSS · JavaScript.**

Turn your own web creations into a living desktop.

[![Release](https://img.shields.io/badge/release-v0.1.3_preview-b7a4ef?style=flat-square)](https://github.com/aidevksh/WallpaperJS-Releases/releases/tag/v0.1.3)
![Platforms](https://img.shields.io/badge/platforms-Windows%20%7C%20macOS-20232b?style=flat-square)
[![License](https://img.shields.io/badge/license-Apache_2.0-bce3ac?style=flat-square)](LICENSE)

[Download](https://github.com/aidevksh/WallpaperJS-Releases/releases/tag/v0.1.3) · [English](README.md) · [한국어](README.ko.md) · [Report an issue](https://github.com/aidevksh/WallpaperJS-Releases/issues)

</div>

---

## A desktop made by you

Import a local HTML, CSS, and JavaScript project and bring it to your desktop. Manage your projects and displays in a charcoal and lavender interface.

- **WallpaperStore** — browse release wallpapers, download, and apply them inside the app.
- **Familiar web tools** — use your own web projects as wallpapers.
- **More screens, one scene** — apply to multiple displays, or span one continuous scene across a Windows display set.
- **Playback that fits your work** — choose 30 or 60 FPS, and pause when needed.
- **At home in the background** — close the window and keep your wallpaper playing; reopen WallpaperJS to manage it.
- **English and Korean** — follow the system language or choose your own.

## Download

**v0.1.3 · WallpaperStore preview** — choose the installer for your operating system and CPU. The library starts empty; the Store downloads wallpapers on demand.

| Operating system | CPU | Installer |
| --- | --- | --- |
| Windows | Intel / AMD (x64) | [Download .exe](https://github.com/aidevksh/WallpaperJS-Releases/releases/download/v0.1.3/WallpaperJS-0.1.3-windows-x64.exe) |
| Windows | ARM64 | [Download .exe](https://github.com/aidevksh/WallpaperJS-Releases/releases/download/v0.1.3/WallpaperJS-0.1.3-windows-arm64.exe) |
| macOS 14.2+ | Apple Silicon (M-series) | [Download .dmg](https://github.com/aidevksh/WallpaperJS-Releases/releases/download/v0.1.3/WallpaperJS-0.1.3-macos-arm64.dmg) |
| macOS 14.2+ | Intel (x64) | [Download .dmg](https://github.com/aidevksh/WallpaperJS-Releases/releases/download/v0.1.3/WallpaperJS-0.1.3-macos-x64.dmg) |

[SHA-256 checksums](https://github.com/aidevksh/WallpaperJS-Releases/releases/download/v0.1.3/SHA256SUMS.txt) · [Release notes](https://github.com/aidevksh/WallpaperJS-Releases/releases/tag/v0.1.3)

v0.1.3 adds an in-app Store backed by the latest [WallpaperStore release](https://github.com/aidevksh/WallpaperStore/releases/latest). Browse thumbnails and choose **Download & apply**, or download to your library for later. Apply and remove buttons now sit directly below the display selection. Imported project thumbnails appear in the library.

### Installation

**Windows:** run the `.exe` and choose an installation location. These builds are not code-signed, so Windows may show a SmartScreen warning.

**macOS:** open the `.dmg` and drag WallpaperJS into Applications. These builds do not have Developer ID signing or Apple notarization, so Gatekeeper may block launch. Verify the download source, then review the blocked-app notice in **System Settings → Privacy & Security**. Managed devices may restrict launch.

Before upgrading, reopen the existing app and choose **Stop playback and quit** so its background controller and renderer exit. Install the update, then reopen WallpaperJS; imported projects and saved assignments remain.

## Your first wallpaper

1. Open **Store** and select a wallpaper.
2. Check your target displays and choose **Download & apply**.
3. For your own HTML or ZIP, use **Import file**; use **Import folder** for HTML/CSS/JavaScript with assets. Select your displays and apply the wallpaper.
4. On Windows, optionally join the selected displays into one continuous scene.

Closing the manager keeps wallpapers running in a separate background process. Reopen WallpaperJS to manage them; choose **Stop playback and quit** to stop them completely. This version has no persistent tray/menu-bar icon. The macOS manager and HTML renderer stay out of the Dock.

## Platforms and known limitations

| Feature | Windows | macOS |
| --- | --- | --- |
| HTML / CSS / JS wallpapers | Supported | Supported |
| WebM video wallpapers | Requires external mpv | Requires external mpv |
| Per-display wallpapers | Supported | Supported |
| One scene spanning several displays | Display sets | Not supported |
| Lock-screen image | Snapshot or separate image | Not supported |
| English / Korean | Supported | Supported |

- Store browsing and downloads require internet access. Release ZIP sizes and available SHA-256 checksums are checked before import. Downloaded wallpapers run locally; a failed download leaves current playback unchanged.
- Windows lock screens support **still images** only; device policy may restrict changes.
- HTML remains live for clocks and animations. The 30/60 FPS setting limits `requestAnimationFrame`, not CSS animations or embedded video. Resuming HTML after a pause reloads the project. WebM follows its encoded frame rate.
- Standalone HTML imports copy that file only; import a folder/ZIP for relative assets. External network access is blocked, so remote weather APIs require a separate networking design.
- WebM playback needs an external mpv installation; mpv is not bundled. On macOS, `brew install mpv` installs it in a supported location. On Windows, put `mpv.exe` on PATH or set `WALLPAPERJS_MPV` to its absolute path. HTML does not require mpv.
- Windows 11 x64 HTML lifecycle and an unpacked application have been verified locally. Native Windows/macOS build runners check packages and Dock visibility; this does not replace physical-device installer tests. macOS Spaces / Mission Control / multiple displays and Windows mixed-DPI display sets still need validation.
- Linux is not supported.

## License

WallpaperJS is distributed under [Apache License 2.0](LICENSE). See [NOTICE](NOTICE) for attribution and the installed package for dependency license notices. Imported wallpapers retain their authors' licenses.

This repository hosts official downloads and distribution documentation. Application source is maintained separately in a private repository.
