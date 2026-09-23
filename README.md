# Ultimate Retro Manager (URM)

A homebrew library manager and Home Menu launcher creator for the Old 3DS. URM turns your GB, GBC, GBA, and NDS ROMs into a browsable, taggable collection — and, for NDS, one tap away from a real Home Menu icon.

<p align="center">
  <a href="https://github.com/MalicousIntents/BizRetroInjector3DS/releases/latest">
    <img alt="Latest release" src="https://img.shields.io/github/v/release/MalicousIntents/BizRetroInjector3DS?include_prereleases">
  </a>
  <img alt="Platform" src="https://img.shields.io/badge/platform-Old%203DS-6b5ca5">
  <img alt="License" src="https://img.shields.io/badge/license-MIT-8bac0f">
</p>

## What it does

- Scans `sdmc:/bmedia/<platform>/` for your GB, GBC, GBA, and NDS ROMs and builds a browsable library
- Lets you tag, favourite, and hide titles across both screens with a citro2d UI
- Creates **NDS forwarder launchers** on your Home Menu in one tap, with batch creation and per-game status tracking, via a user-installed [NTR_Forwarder](https://github.com/citronacide/NTR_Forwarder) pack
- Keeps an atomic on-SD database at `sdmc:/3ds/URM/`
- Built on a portable, dependency-free C17 core, unit-tested on the host (1,700+ assertions), with a zero-warning build

## Honest scope

This is early software — here's what's actually done vs. what's coming:

| | Status |
|---|---|
| GB / GBC / GBA / NDS library browsing, tagging, favourites, hiding | ✅ Working |
| NDS Home Menu forwarder creation (batch) | ✅ Working |
| GB / GBC / GBA Home Menu launcher creation | 🚧 Planned |
| Artwork download | 🚧 Planned |
| Real-hardware validation on an Old 3DS | 🚧 In progress |

## Requirements

- An **Old 3DS** (New 3DS / 2DS support hasn't been validated yet)
- [Luma3DS](https://github.com/LumaTeam/Luma3DS) with sigpatches — the `.cia` build is test-keyset signed, so signature patches are required to install it
- [NTR_Forwarder](https://github.com/citronacide/NTR_Forwarder) installed, to actually launch the NDS forwarders URM creates
- ROMs placed under `sdmc:/bmedia/<platform>/` on your SD card (e.g. `sdmc:/bmedia/nds/`)

## Getting started

1. Install Luma3DS with sigpatches if you haven't already.
2. Install [NTR_Forwarder](https://github.com/citronacide/NTR_Forwarder) — URM's NDS launchers call into it.
3. Copy your ROMs into `sdmc:/bmedia/<platform>/` (one folder per platform: `gb`, `gbc`, `gba`, `nds`).
4. Copy `URM.3dsx` to `/3ds/` on your SD card, or install `URM.cia`.
5. Launch URM from the Homebrew Launcher (`.3dsx`) or the Home Menu (`.cia`).
6. Browse your library, tag or favourite what you want, and create Home Menu launchers for your NDS titles.

## Files in this repo

| File | Description |
|---|---|
| `URM.3dsx` | Homebrew Launcher build |
| `URM.cia` | Installable CIA build (test-keyset signed) |

## Disclaimer

This tool does not include, distribute, or link to any copyrighted ROMs. It only works with ROM files you provide yourself. You are responsible for only using ROMs you've legally dumped from games you own. Use custom firmware at your own risk.

## Contributing

Issues and pull requests are welcome — see the [Issues](https://github.com/MalicousIntents/BizRetroInjector3DS/issues) tab. GB/GBC/GBA launcher creation and artwork downloading are the next big pieces of work if you want to help.

## License

MIT — see [LICENSE](LICENSE) for details. *(Add a `LICENSE` file to the repo if one isn't there yet.)*
