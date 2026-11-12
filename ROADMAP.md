# Roadmap — Zakaria Board

A digital whiteboard for teaching mathematics (Moroccan 2BAC), built on Lorien and Godot 4.3.
Work proceeds one phase at a time; each phase starts only after approval.

Legend: ✅ done · 🔄 in progress · ⏳ planned

## Phase 0 — Repository audit ✅
Audit of Lorien's architecture, features, risks and licenses.

## Step 0.5 — Setup & baseline 🔄
- ✅ Fork `mbrlabs/Lorien` → `zakaria-boullam/Lorien`, `upstream` remote configured
- ✅ CHANGELOG, ROADMAP, THIRD_PARTY_LICENSES
- ⏳ Baseline verified on Windows with Godot 4.3 (draw, save, reopen; mouse and XP-Pen)

## Phase 1 — UI and background ⏳
- Charcoal canvas `#17191D`, subtle dotted grid
- Minimalist toolbar; pens: white, yellow, cyan, green, pink; adjustable width
- Distraction-free fullscreen teaching mode (extends existing Zen mode)
- Zakaria Board branding; responsive layout
- Remove F12 easter egg

## Phase 2 — Stylus and writing ⏳
- Process every tablet sample (not once per frame); disable accumulated input
- Incremental stroke rendering (remove per-point full rebuild)
- Pressure tuning for XP-Pen; Wintab vs Windows Ink comparison
- Palm/touch handling where the platform allows
- Pen/eraser shortcuts; undo/redo fixes (stroke order after undo)
- Separate mouse and tablet tests

## Phase 2.5 — Document model v2 ⏳
- Pages within a document
- Versioned, validated file format (still opens v1 `.lorien` files)
- Generic canvas-object type for non-stroke items (needed by Phase 3)

## Phase 3 — Mathematics tools ⏳
- Safe expression parser (whitelisted functions only)
- Cartesian axes, configurable graph grid and scales
- y = f(x) plotting: polynomial, rational, trig, exp, log; discontinuities and domains
- Multiple colored functions; points, vectors, lines, circles, constructions
- Optional LaTeX rendering (highest risk — last)

## Phase 4 — Teaching features ⏳
- PNG export, then PDF export
- PDF import if feasible (fallback: image import)
- Keyboard and pen-button shortcuts; hideable toolbar; presentation mode
- Templates: limits, continuity, derivatives, integrals, geometry

## Phase 5 — Quality and distribution ⏳
- Performance for large lessons; automated tests
- Release builds for macOS and Windows; signing/notarization decision
- Installation and tablet configuration docs
- Original brand identity; final third-party license audit

## Known upstream issues to address
- Brush samples cursor once per frame → lost tablet samples (Phase 2)
- Per-point full stroke rebuild + optimizer → O(n²) per stroke (Phase 2)
- Undo of delete does not preserve stroke order (Phase 2)
- Save format unvalidated, RGB only, strokes only (Phase 2.5)
- `InfiniteCanvas.take_screenshot()` uses a Godot 3 API and is unused (Phase 4)
