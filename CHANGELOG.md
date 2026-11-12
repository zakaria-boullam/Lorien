# Changelog — Zakaria Board

All notable changes to Zakaria Board are documented here.
Zakaria Board is a fork of [Lorien](https://github.com/mbrlabs/Lorien) (MIT).
Lorien's own history is kept in [docs/changelog.md](docs/changelog.md).

Format: [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).
"Tested" lines state exactly what was verified and on which platform/hardware.

## [Unreleased]

### Added
- `CHANGELOG.md`, `ROADMAP.md`, `THIRD_PARTY_LICENSES.md` (project documentation).

### Baseline
- Forked from `mbrlabs/Lorien` at commit `17e3222` (2025-09-22, version 0.7.0-beta1).
- Engine pinned to **Godot 4.3 stable**.
- No source code changes yet.

### Tested
- 2026-11-12, Windows 11, Godot 4.3-stable (official build, SHA-512 verified), by Claude:
  - Project imports with no errors (110 assets).
  - App launches headless and windowed (GL Compatibility) and reaches the 144 FPS cap.
  - One harmless upstream startup error: `get_viewport_rect` called before the node is in the tree (`UI/Menubar.gd:106`).
  - Not tested: drawing, saving/reopening, mouse or pen input (requires manual interaction).
- Pending: manual baseline test on Windows (mouse + XP-Pen) by Zakaria.
