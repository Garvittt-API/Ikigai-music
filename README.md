<div align="center">

<img src="crates/kopuz/assets/logo-512.png" alt="Ikigai Logo" width="120" />

# Ikigai

**Your music, your way.**

A modern, blazing-fast music player built with Rust and Dioxus.

[![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey?style=for-the-badge)]()
[![Downloads](https://img.shields.io/github/downloads/Garvittt-API/Ikigai-player/total?style=for-the-badge&color=green)](https://github.com/Garvittt-API/Ikigai-player/releases)

<br/>

[Installation](#installation) • [Features](#features) • [Screenshots](#screenshots) • [Download](#download)

</div>

---

<br/>

<div align="center">

### What is Ikigai?

*Ikigai* (生き甲斐) — a Japanese concept meaning "a reason for being."

Your music player should be exactly that: **a reason to enjoy your music.**

No bloat. No ads. Just your library, beautifully organized and lightning fast.

</div>

<br/>

---

## Download

<div align="center">

| Platform | Link |
|----------|------|
| **Windows** | [Download Installer (27 MB)](https://github.com/Garvittt-API/Ikigai-player/releases/latest) |
| **Linux** | `cargo install ikigai-player` • [AUR](https://aur.archlinux.org/packages/ikigai-player-bin) • [Flatpak](#flatpak) |
| **macOS** | `cargo install ikigai-player` |

</div>

<br/>

---

## Features

<table>
<tr>
<td width="50%" valign="top">

### Core
- **Multiple Backends** — Local files, Jellyfin, Subsonic/Navidrome, YouTube Music, SoundCloud
- **Smart Library** — Auto-scan, organize by artist/album/genre
- **Playlists** — Create, manage, and sync with your server
- **Favorites** — Star tracks locally or sync with Jellyfin/Subsonic
- **Lyrics** — Real-time synced & plain lyrics with auto-scroll
- **Scrobbling** — ListenBrainz support

</td>
<td width="50%" valign="top">

### Experience
- **Custom Themes** — Full color variable control, build your own
- **Mini Player** — Compact overlay for quick access
- **System Tray** — Minimize to tray, keeps playing in background
- **Discord RPC** — Show what you're listening to
- **Equalizer** — 10-band with presets
- **Crossfade** — Smooth track transitions

</td>
</tr>
<tr>
<td width="50%" valign="top">

### Power
- **yt-dlp Integration** — Download from YouTube and 1000+ sites
- **Genre Browsing** — Explore your library by genre
- **Quick Search** — Jump to anything instantly
- **Custom Fonts** — Bring your own interface font
- **Listening Logs** — Track play counts locally
- **Performance Tracing** — Built-in profiler

</td>
<td width="50%" valign="top">

### Polish
- **Native Integration** — MPRIS (Linux), Now Playing (macOS), SMTC (Windows)
- **File-Type Badges** — See format at a glance (MP3, FLAC, WAV)
- **Auto-Cleanup** — Removes missing tracks on rescan
- **Reduce Animations** — Accessibility-first
- **30+ Languages** — Full i18n support
- **Smooth Navigation** — Scroll positions preserved

</td>
</tr>
</table>

<br/>

---

## Screenshots

<div align="center">

> *Screenshots coming soon. Run `just serve` to try it yourself!*

</div>

<br/>

---

## Quick Start

### Windows

Download the installer from [Releases](https://github.com/Garvittt-API/Ikigai-player/releases/latest), run `IkigaiPlayer-Setup.exe`, and follow the wizard.

### Linux / macOS

```bash
# Install from crates.io
cargo install ikigai-player

# Or build from source
git clone https://github.com/Garvittt-API/Ikigai-player.git
cd Ikigai-player
cargo build --release
```

### Run in Development

```bash
# Requires: Rust, Dioxus CLI, Node.js
npm install
just serve
```

<br/>

---

## Tech Stack

<div align="center">

| Layer | Technology |
|-------|-----------|
| Language | [Rust](https://www.rust-lang.org/) |
| UI Framework | [Dioxus](https://dioxuslabs.com/) |
| Audio | [Symphonia](https://github.com/pdeljanov/symphonia) + [Cpal](https://github.com/RustAudio/cpal) |
| Metadata | [Lofty](https://github.com/Serial-Dev/lofty-rs) |
| Database | [SQLite](https://www.sqlite.org/) / [sqlx](https://github.com/launchbadge/sqlx) |
| Styling | [TailwindCSS](https://tailwindcss.com/) |

</div>

<br/>

---

## Building

### Prerequisites

- [Rust](https://rustup.rs/) (stable)
- [Dioxus CLI](https://dioxuslabs.com/docs/0.6/guide/engetting_started/installation.html)
- [Node.js](https://nodejs.org/) (for Tailwind)
- Platform libraries (see [CONTRIBUTING.md](CONTRIBUTING.md))

### Build Commands

```bash
just serve          # Dev server with hot reload
just build          # Release build
cargo clippy --workspace --all-targets -- -D warnings   # Lint
cargo fmt --all     # Format
cargo test --workspace   # Test
```

<br/>

---

## Project Structure

```
Ikigai-player/
├── crates/
│   ├── kopuz/          # App binary & entry point
│   ├── components/     # Reusable UI components
│   ├── pages/          # Page-level views
│   ├── player/         # Audio engine
│   ├── db/             # SQLite backend
│   ├── server/         # Media source backends
│   ├── hooks/          # Dioxus data hooks
│   ├── config/         # App configuration
│   ├── reader/         # Domain models & scanner
│   ├── i18n/           # Internationalization
│   ├── utils/          # Shared utilities
│   ├── radio/          # Internet radio
│   ├── scrobble/       # ListenBrainz scrobbling
│   └── discord-presence/  # Discord RPC
├── android-src/        # Android media session
├── packaging/          # Flatpak, AUR, Nix
└── scripts/            # Build & codegen helpers
```

<br/>

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

```bash
# Quick setup
git clone https://github.com/Garvittt-API/Ikigai-player.git
cd Ikigai-player
nix develop    # or install deps manually
just serve
```

<br/>

---

## License

This project is licensed under the [MIT License](LICENSE).

<br/>

---

<div align="center">

**Built with care using Rust + Dioxus**

[![Star History Chart](https://api.star-history.com/svg?repos=Garvittt-API/Ikigai-player&type=Date)](https://star-history.com/#Garvittt-API/Ikigai-player&Date)

</div>
