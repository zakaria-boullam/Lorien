# Third-Party Licenses — Zakaria Board

This file lists third-party code and assets used by Zakaria Board.
Status: **draft** — a full audit is scheduled for Phase 5, before any public distribution.

| Component | Used for | License | Obligation | Status |
|---|---|---|---|---|
| [Lorien](https://github.com/mbrlabs/Lorien) © 2021-2025 Marcus Brummer | Base application | MIT | Keep copyright notice and license text (see [LICENSE](LICENSE)) | ✅ Confirmed |
| [Godot Engine](https://godotengine.org) 4.3 | Engine / runtime | MIT (+ bundled third-party libraries) | Ship Godot's license and its third-party notices with builds (https://godotengine.org/license) | ✅ Confirmed |
| [godot-antialiased-line2d](https://github.com/godot-extended-libraries/godot-antialiased-line2d) | Stroke anti-aliasing texture (`lorien/BrushStroke/BrushStrokeTexture.gd`) | MIT | Keep attribution | ✅ Confirmed (per source comment) |
| [Remix Icon](https://remixicon.com/) | UI icons (`lorien/Assets/Icons`) | Apache 2.0 for older versions; newer versions use a custom license | Verify version used, or replace with original icons | ⚠️ To verify |
| Player sprites (`lorien/Assets/Player`) | F12 easter egg | Not stated in repo | Planned for removal in Phase 1 | ⚠️ Unknown |
| UI font ("Open Sans SemiBold" referenced in theme) | UI text | SIL OFL 1.1 if bundled | Verify whether bundled or system font | ⚠️ To verify |

## Design inspiration
Visual principles (dark canvas, dotted grid, minimal toolbar) are inspired by Scrble Ink.
No Scrble Ink code, icons, logos, names or assets are used.
