# MagicToolbox Bitmapper Lite

**Free bitmap builder for MagicQ execute grids. Windows only.**

Design custom button bitmaps for your MagicQ execute pages — presets, custom colors, shapes, icons, and the famous duck mode. Export ready-to-use PNGs with a visual PDF catalog.

![Main Window — Execute grid with bitmap editor panel](screenshots/main_window.png)

![Color Palette Wizard — auto-generate unique colors for all buttons](screenshots/color_palette_wizard.png)

[![Intro Video — Bitmapper Lite](https://img.youtube.com/vi/3j7hPkbdQhE/0.jpg)](https://youtu.be/3j7hPkbdQhE)

---

## Features

- **11 Built-in Presets** — Glass, Neon, Flat, Gradient, Metallic, Launchpad, LED Dot, Arcade, MagicQ, Console, and Duck
- **Full Customization** — Shape, corner radius, gradient direction, colors (fill, border, label), opacity, icons
- **80 Vector Icons** — Arrows, Position (fan out/in, crossed, spread, converge), Lamp, Color, Beam, Effects, Fixtures, Transport, Numbers 0–9, Symbols, and Media categories
- **Freehand Drawing Tool** — Draw custom icon shapes on a canvas with adjustable brush size and eraser
- **Auto-Fit Text Labels** — Add custom text that automatically shrinks to fit the button — never cropped
- **Color Palette Wizard** — Auto-generate unique color schemes across all your execute buttons with one click
- **Apply Mode** — Click buttons on the grid to apply your bitmap design instantly
- **Visual PDF Catalog** — Every export includes a `bitmap_catalog.pdf` showing each bitmap with its filename, so you know exactly which file to assign in MagicQ
- **Smart Output Folder** — Auto-creates a bitmap folder inside your show's `bitmaps/` directory
- **Fader & Encoder Support** — Not just buttons — design track/knob and base/dial bitmaps too
- **Multi-Page Export** — Style buttons across multiple execute pages, then export everything at once with deduplication
- **Close Warning** — Warns you before closing if you have unexported bitmap styles

## Download & Install (Windows only)

Go to the [**Releases**](../../releases/latest) page and download **`BitmapperLite_Setup_v1.0.6-beta.exe`** (26 MB).

Run the installer and follow the setup wizard. It installs to Program Files with a Start Menu shortcut and optional desktop shortcut.

> **Windows SmartScreen warning:** This app is not yet code-signed, so Windows shows a one-time warning. Click **"More info"** → **"Run anyway"**. This is normal for new unsigned software and is safe to proceed.

## System Requirements

- Windows 10 or 11 (64-bit)
- ~50 MB disk space
- MagicQ show file (.shw) with execute grids

## Quick Start

1. **Open** a MagicQ `.shw` show file (File > Open Show or Ctrl+O)
2. **Select** an execute page from the list on the left
3. **Choose** a preset or customize your bitmap style in the right panel
4. **Apply** — Click "Apply Mode", then click buttons on the grid to apply your design
5. **Export** — Click "Export Bitmaps" to save PNGs + PDF catalog to the output folder
6. **In MagicQ** — Copy the exported PNGs to your `show/bitmaps/` folder, then set each button's bitmap path using the filenames from the PDF catalog

## How It Works

Bitmapper Lite reads your MagicQ show file to display execute grid layouts. You design bitmap styles and apply them to buttons. When you export, it generates optimized 128x128 PNG pairs (idle + active state) that MagicQ automatically rescales to fit any button size.

The PDF catalog (`bitmap_catalog.pdf`) is your visual reference — it shows every exported bitmap with its filename, making it easy to find the right file when setting bitmaps in MagicQ (which has no bitmap preview).

## Tips

- Use the **Color Palette Wizard** (palette icon in toolbar) to quickly generate unique colors for all buttons on a page
- The output folder defaults to `<your show folder>/bitmaps/<showname>/` — MagicQ can load bitmaps directly from there
- Bitmap filenames stay under 40 characters to fit MagicQ's command_text field limit
- Export multiple times — the PDF catalog updates to include all bitmaps in the folder

## Changelog

### v1.0.6-beta (2026-02-23)
- **New: 80 Vector Icons** — Expanded icon library from 43 to 80 icons across 11 categories including new Position, Numbers, Symbols, and Media categories
- **New: Position Icons** — 12 purpose-built icons for position palettes: Fan Out/In (horizontal & vertical), Fan Down, Crossed, All Up/Down/Left/Right, Spread, Converge, and Diagonal Fan
- **New: Freehand Drawing Tool** — Draw custom icon shapes directly on a paint-like canvas with adjustable brush size and eraser — click "Draw..." in the Icon section
- **New: Auto-Fit Text Labels** — Label text on buttons now auto-shrinks to fit the available width instead of being cropped with "..."
- **New: Label Text Field** — Added a dedicated Label section to the editor panel with text input and color picker
- **Fix:** Switching presets no longer clears your icon, drawing, or label — only the Clear button resets them

### v1.0.5-beta (2026-02-22)
- **Fix:** Color Palette Wizard now correctly extracts palette colors — previously all bitmaps rendered white on showfiles where the first fixture type uses a colour wheel instead of CMY/RGB mixing
- **Fix:** Macros on execute grids are now correctly identified and displayed as "M" (Macro) instead of "Lay" (Layout)
- **Fix:** Execute item type mappings corrected for Colour, Beam, and Position palettes
- **New:** Name-based color fallback — palettes with only colour wheel data (no CMY/RGB) now guess the color from the palette name (e.g. "Red", "Congo Blue", "White")

### v1.0.4-beta (2026-02-20)
- Multi-page export with deduplication
- Close warning for unexported bitmap styles
- YouTube intro video added

### v1.0.0-beta (2026-02-19)
- Initial release

## Disclaimer

This software is an independent third-party tool and is **not affiliated with, endorsed by, or associated with ChamSys Ltd** in any way. "MagicQ" is a registered trademark of ChamSys Ltd. All trademarks belong to their respective owners. This software reads user-created MagicQ show files (.shw) in read-only mode and does not contain, modify, or redistribute any ChamSys software or proprietary materials.

## About

Built by **ByFeignasse** for the MagicQ lighting community.

## License

Freeware — free to use for any purpose. See [LICENSE](LICENSE) for details.
