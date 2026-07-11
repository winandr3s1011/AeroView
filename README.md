
  ![Platform](https://img.shields.io/badge/platform-Windows%2010%2F11-blue?logo=windows)
  ![Version](https://img.shields.io/badge/version-1.0.0-brightgreen)
  ![License](https://img.shields.io/badge/license-MIT-blue)
  ![Electron](https://img.shields.io/badge/built%20with-Electron%2031-47848F?logo=electron)
  ![Languages](https://img.shields.io/badge/languages-IT%20EN%20ES%20FR%20DE-orange)
</div>

---

## 🪟 What is AeroView?

**AeroView** is a free, lightweight media viewer for Windows that brings back the iconic
**Aero Glass** design from the Windows Vista / Windows 7 era — rebuilt from the ground up
with modern web technology (Electron + Chromium) while adding powerful new features never
available in the original Windows Photo Viewer.

> *"What if Windows 7 Photo Viewer never died — and got a serious upgrade?"*

---

## ✨ Features

### 🖼️ Universal Media Support
- Opens **all major image and video formats** with zero codec installation
- **Smart folder navigation** — open any single file, instantly browse all media in the same folder with arrow keys
- **Drag & drop** files or entire folders onto the window
- **Double-click** any image/video in Windows Explorer to open it directly

### 🎨 Authentic Aero Glass Design
- Frosted glass window with real `backdrop-filter` blur
- Glossy title bar with multi-stop gradient and top shine reflection
- Smooth micro-animations: hover glow, zoom transitions, fade effects
- Custom frameless window with native OS minimize / maximize / close

### 🌗 Light & Dark Themes
| Theme | Description |
|-------|-------------|
| 🌙 **Dark Mode** | Deep navy glass, optimal for night / OLED |
| ☀️ **Light Mode** | Soft azure glass, optimal for bright rooms |

Theme preference saved automatically, restored on next launch.

### 🔍 Image Viewer
| Feature | Detail |
|---------|--------|
| Zoom | Mouse wheel, `+` / `-` keys, toolbar buttons |
| Pan | Click and drag on zoomed images |
| Rotate | 90° clockwise per click, `R` key |
| Fit to Window | `F` key — fills the viewer area |
| Actual Size | 1:1 pixel view |
| Zoom indicator | Live % in status bar |

### 🎬 Built-in Video Player
| Feature | Detail |
|---------|--------|
| Play / Pause | Space bar or click |
| Seek | Click anywhere on progress bar |
| Volume | Slider control |
| Mute | `M` key |
| Speed | 0.25× · 0.5× · 1× · 1.5× · 2× · 4× |
| Fullscreen | `F11` or dedicated button |
| Auto-hide controls | Fade out after 2s of no mouse movement |
| Time display | Current time / total duration |

### 🖥️ Fullscreen Slideshow — Multi-Monitor Support
- Configurable transition interval: **1 to 15 seconds**
- Goes **fullscreen** on the selected monitor automatically
- **Multi-monitor detection** — if more than one display is connected:
  - Displays a monitor picker dialog with resolution info
  - Option: **"Always use this monitor"** — remembers your choice, skips dialog next time
  - Option: **"Always show monitor selection dialog"** — forces the picker every time
- **Settings › Slideshow Monitor** menu — change monitor preference at any time
- Starts from toolbar button or **View** menu

### 🎵 Background Music
| Source | How |
|--------|-----|
| 🎵 Local file | Select any MP3, WAV, FLAC, OGG, AAC from your PC |
| 🟢 Spotify | Paste a Spotify share link → auto-embedded player |
| 🔴 YouTube | Paste a YouTube / YouTube Music URL → embedded mini-player |

Play/Pause control for local audio; web services play in their embedded iframe player.

### 🗂️ Gallery Panel
- Scrollable thumbnail strip (left side) with all folder files
- Click any thumbnail → jump instantly to that file
- Active file highlighted with glowing blue selection ring
- Toggle on/off from View menu

### ℹ️ Information Panel
- Right-side panel showing live metadata:
  - File name, type, size
  - Image resolution (px × px)
  - Video duration
  - Current zoom %
- Toggle on/off from View menu

### 🌐 5-Language Interface
Automatically detected from the OS, changeable at any time without restart:

| 🏳️ Language | Code | Auto-detected from |
|------------|------|--------------------|
| 🇮🇹 Italiano | `it` | `it-IT`, `it-CH` etc. |
| 🇬🇧 English  | `en` | All other locales (default) |
| 🇪🇸 Español  | `es` | `es-*` |
| 🇫🇷 Français | `fr` | `fr-*` |
| 🇩🇪 Deutsch  | `de` | `de-*` |

---

## ⌨️ Keyboard Shortcuts

| Action | Shortcut |
|--------|----------|
| Open File | `Ctrl + O` |
| Previous File | `← Arrow` |
| Next File | `→ Arrow` |
| Zoom In | `=` or `+` |
| Zoom Out | `-` |
| Fit to Window | `F` |
| Rotate | `R` |
| Play / Pause Video | `Space` |
| Mute Video | `M` |
| Video Fullscreen | `F11` |
| Delete File | `Delete` |

---

## 📁 Supported Formats

### 🖼️ Images (12 formats / 14 extensions)

| Format | Extensions | Notes |
|--------|------------|-------|
| JPEG | `.jpg` `.jpeg` `.jfif` | All quality levels |
| PNG | `.png` | With transparency |
| GIF | `.gif` | Static & animated |
| WebP | `.webp` | Modern web format |
| SVG | `.svg` | Vector graphics |
| BMP | `.bmp` | Windows bitmap |
| AVIF | `.avif` | Next-gen image |
| ICO | `.ico` | Windows icon files |
| TIFF | `.tiff` `.tif` | High-quality scans |

### 🎬 Video (9 formats / 12 extensions)

| Format | Extensions | Notes |
|--------|------------|-------|
| MP4 | `.mp4` `.m4v` | Most common format |
| WebM | `.webm` | Web-optimized |
| OGG Video | `.ogg` `.ogv` | Open standard |
| QuickTime | `.mov` | Apple format |
| AVI | `.avi` | Legacy Windows |
| Matroska | `.mkv` | Container format |
| Flash Video | `.flv` | Legacy web video |
| WMV | `.wmv` | Windows Media |
| 3GPP | `.3gp` | Mobile video |

---

## 🪟 File Associations (for Inno Setup / installer)

All extensions to register with AeroView as default viewer:

```
Images:  .jpg  .jpeg  .jfif  .png  .gif  .webp  .bmp  .svg  .avif  .ico  .tiff  .tif
Video:   .mp4  .m4v  .webm  .ogg  .ogv  .mov  .avi  .mkv  .flv  .wmv  .3gp
```

**Total: 23 extensions across 21 formats**

---

## 🛠️ Building from Source

### Prerequisites
- [Node.js](https://nodejs.org/) 18+
- [npm](https://www.npmjs.com/) (comes with Node.js)
- Windows 10/11 64-bit

### Setup
```bash
git clone https://github.com/TUO-USERNAME/aeroview.git
cd aeroview
npm install
```

### Run in development mode
```bash
npx electron . --dev
```

### Build portable .exe
```bash
npx electron-packager . AeroView --platform=win32 --arch=x64 --overwrite --out=dist --icon=icon.ico
```
The output is in `dist\AeroView-win32-x64\AeroView.exe`

---

## 📦 Creating an Installer with Inno Setup

1. Download and install **[Inno Setup 6](https://jrsoftware.org/isinfo.php)**
2. Build the app first (see above)
3. Open `AeroView_Setup.iss` in Inno Setup Compiler
4. Edit the `#define SourceDir` line to match your `dist\AeroView-win32-x64` folder path
5. Click **Build → Compile**
6. The installer will be in `Output\AeroView_Setup_1.0.0.exe`

### What the installer does:
- ✅ Installs AeroView to `Program Files\AeroView`
- ✅ Creates Start Menu shortcut
- ✅ Optional Desktop shortcut
- ✅ Registers **23 file associations** (images + video)
- ✅ Adds **"Open with AeroView"** to right-click context menu in Explorer
- ✅ Notifies Windows of association changes (icons refresh immediately)
- ✅ Supports **Italian, English, Spanish, French, German** installer UI
- ✅ Includes proper **uninstaller** that cleans all registry entries

---

## 💡 Design Inspiration

AeroView was built as a love letter to the **Windows Vista / 7 Aero** design language:

| Aero Feature | How we recreated it |
|---|---|
| Glass transparency | CSS `backdrop-filter: blur()` |
| Glossy buttons | Multi-stop linear-gradient + shine overlay |
| Soft glow & shadows | CSS `box-shadow` with blue hues |
| Blue gradient title bar | 5-stop gradient from `#6ab0ff` to `#1050c0` |
| Smooth animations | CSS transitions + `transform` GPU acceleration |
| Reflections | `::after` pseudo-element with gradient overlay |

The result is an app that feels like it belongs to 2009 — but runs natively on Windows 11,
supports modern formats like AVIF and WebM, and has features the original never had.

---

## 🖥️ System Requirements

| | Minimum | Recommended |
|-|---------|-------------|
| **OS** | Windows 10 64-bit | Windows 11 64-bit |
| **RAM** | 256 MB | 512 MB |
| **Storage** | 300 MB | 500 MB |
| **Display** | 1024×600 | 1920×1080 |
| **GPU** | DirectX 9 | DirectX 11 |

---

## 🗺️ Roadmap

- [ ] Printing support
- [ ] Image editing (crop, brightness, contrast)
- [ ] HEIC / HEIF format support
- [ ] Customizable slideshow transitions (fade, slide, zoom)
- [ ] Thumbnail cache for faster gallery loading
- [ ] Export/Share integration

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

## 🙏 Credits

| Technology | Use |
|---|---|
| [Electron](https://electronjs.org/) | Native Windows app shell |
| [Chromium](https://www.chromium.org/) | Rendering engine |
| [Inter](https://fonts.google.com/specimen/Inter) | UI typography |
| Windows Aero (Microsoft) | Visual design inspiration |

---

<div align="center">
  <sub>Made with ❤️ and nostalgia for the Windows 7 era</sub>
</div>

