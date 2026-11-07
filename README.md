<div align="center">

<img src="snap/gui/screention.png" alt="Screention logo" width="128" />

# Screention

**Capture, annotate, read and share screenshots.**

[![screention](https://snapcraft.io/screention/badge.svg)](https://snapcraft.io/screention)
[![Base: core26](https://img.shields.io/badge/Base-core26-2C8C3C?logo=canonical&logoColor=white)](https://snapcraft.io/core26)
![Confinement: strict](https://img.shields.io/badge/Confinement-strict-2C8C3C)
[![Maintainer: sidaliteir](https://img.shields.io/badge/Maintainer-sidaliteir-2C8C3C?logo=snapcraft&logoColor=white)](https://snapcraft.io/publisher/sidaliteir)
![Architectures: amd64](https://img.shields.io/badge/Architectures-amd64-2C8C3C?logo=linux&logoColor=white)

[Getting Started](#getting-started) · [Configure](#configure) · [Limitations](#limitations) · [Build](#build) · [Support](#support) · [License](#license)

Unofficial snap packaging for [Screention](https://screention.gkernel.com), a free screenshot tool with annotation, on-device OCR, QR code reading and share links. The snap repackages the official Linux release; the application's source code is not public.

</div>

---

## Getting Started

<a href="https://snapcraft.io/screention"><img alt="Get it from the Snap Store" src="https://snapcraft.io/en/dark/install.svg" width="180"></a>

```bash
sudo snap install screention
```

Open Screention from your application menu, then press `Ctrl+Alt+A` or choose **Take screenshot** from its tray menu and select part of the screen. See the upstream [user guide](https://screention.gkernel.com/docs) for the editor tools.

## Configure

There are no `snap set` options. Use the application's Settings for shortcuts, OCR languages, uploads and privacy. Screention sends anonymous usage counts by default; turn them off in **Settings > Privacy**.

Settings, the gallery and downloaded OCR languages stay under `~/snap/screention/current`. When saving a screenshot, choose a folder in your home directory to keep it outside the snap.

## Limitations

- Updates come through `snap refresh screention`. Ignore the in-app notice to download a new `.deb`.
- On Wayland, GNOME and KDE capture through the desktop's screenshot portal and may ask for permission. Other Wayland desktops use the included `grim`, which needs a wlroots compositor.
- Launch at login works through snapd's autostart support for the file the application creates.
- Files must be in a normal folder under your home directory. Hidden folders directly under your home directory are not accessible.
- Only amd64 is available, matching the official Linux release.

## Build

```bash
git clone https://github.com/sidalit/screention-snap.git
cd screention-snap
sudo snap install snapcraft --classic
snapcraft pack
```

## Support

- **Installation or snap issues:** [open a packaging issue](https://github.com/sidalit/screention-snap/issues).
- **Application bugs:** use **Messages** in the application or [the upstream releases repository](https://github.com/gkernel247/screention-releases/issues).

## License

Snap packaging: [MIT](LICENSE). Screention itself is proprietary freeware under its [terms](https://screention.gkernel.com/terms-and-conditions).
