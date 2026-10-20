# 🍃 Tanuyomi v0.1.2-beta

We are pleased to announce the release of **Tanuyomi v0.1.2-beta**!

This release introduces major performance and memory efficiency improvements with **6 key streaming pipeline optimizations** for comic archives and video streaming, unifies the default server port to **`5005`** across all platforms to prevent macOS AirPlay conflicts, adds video seek thumbnail auto-scroll & active frame highlighting, provides an unsaved settings warning dialog, and includes **multilingual README guides (English, Japanese, Simplified Chinese)** with clear language-coded filenames across all release packages.

---

### 🚀 Changelog

#### ⚡ Performance & Streaming Optimizations (The Big 6)
- **Comprehensive Image & Video Pipeline Overhaul**:
  1. **Early HTTP 304 (Not Modified) Bypass**: Directly validates `If-None-Match` (ETag) headers at the endpoint entry point, completely skipping disk I/O, database lookups, and archive decompression when assets are already cached in the browser.
  2. **Elimination of LOH (Large Object Heap) Double Allocations**: Leveraged `ArrayPool<byte>` memory pooling and direct pipeline streaming, substantially lowering Garbage Collection (GC) overhead and memory footprint during page turns.
  3. **O(1) Archive Entry Lookup**: Replaced linear archive scanning with hash-table lookup for ZIP and CBZ archives, eliminating repetitive string allocations and speeding up entry resolution.
  4. **OS Page Cache Delegation & Range/ETag Header Optimization for Video Streaming**: Replaced the legacy 50MB in-memory chunk cache with OS-level filesystem page caching, significantly improving video seek responsiveness while slashing background memory consumption.
  5. **Frontend `fetchpriority="high"` Scheduling**: Fine-tuned image fetch priority and prefetch arbitration on the reader view to eliminate perceived page rendering delay.
  6. **Direct JPEG Streaming for PDF Pages**: Streamlined PDF page rendering by serving JPEGs directly without redundant PNG re-encoding, minimizing CPU overhead and speeding up page display.

#### ✨ Features & UI Improvements
- **🎬 Video Seek Thumbnail Synchronization**: Opening the 100-frame scene seek drawer now automatically scrolls to and visually highlights the currently playing frame with an active border.
- **📁 Video File Extension Badges**: Displayed file extension badges (MP4, MKV, WebM, etc.) on video cards in the library explorer.
- **⚙️ Unsaved Settings Guard**: Added a confirmation dialog when attempting to navigate to another tab with unsaved setting changes to prevent accidental data loss.
- **🖥️ Desktop Control Panel Graceful Shutdown**: Added a "Shutting down..." status indicator in the desktop GUI window to ensure all background processes terminate cleanly.
- **📝 Cleaner Log Output**: Suppressed benign logical drive enumeration warnings on non-Windows platforms and restricted environments.

#### 🌐 Internationalization (i18n)
- **Multilingual READMEs Bundled by Default**:
  - All distribution packages (Windows, macOS, Linux) now include localized documentation with self-descriptive filenames:
    - **`README_EN.txt`**: English guide
    - **`README_JA.txt`**: Japanese guide (日本語)
    - **`README_ZH.txt`**: Simplified Chinese guide (简体中文)
    - **`README.txt`**: Multilingual index & quick start guide

#### 🔧 Configuration
- **Unified Default Port 5005**: Changed the default listening port from 5000 to `5005` across all platforms (Windows, Linux, macOS) to avoid port collision with the native macOS AirPlay Receiver service.

---

### 📦 Distribution Packages

| File Name | Platform / Architecture | Size | SHA256 Checksum |
| :--- | :--- | :--- | :--- |
| **`tanuyomi-0.1.2-beta-win-x64.zip`** | Windows 10 / 11 (64-bit) | ~147.2 MB | `d2b4dd8bdbe36399d4b4ba6fb03eb0b6cdb2b870d3c5927fb2d76eb60818ce4a` |
| **`tanuyomi-0.1.2-beta-osx-arm64.tar.gz`** | macOS (Apple Silicon: M1–M4) | ~78.5 MB | `89855330addd377617b96793a3c142b659c07928e24fcade790c206cde2a3b77` |
| **`tanuyomi-0.1.2-beta-linux-x64.tar.gz`** | Linux x64 (Ubuntu, Debian, etc.) | ~79.1 MB | `528fbc5324d87b8e0fc697e3a17f6cb4f316f64e38a3127b6dd2d7911cbed49f` |
| **`tanuyomi-0.1.2-beta-linux-arm64.tar.gz`** | Linux ARM64 (Raspberry Pi 4/5, etc.) | ~73.8 MB | `1f7487d99706226bc972a7065b5d4bd03aae6f8235b680a609a7b34ceb8ccc7d` |
| **`version.json`** | All Platforms (Update Metadata) | ~1.8 KB | ― |

> [!IMPORTANT]
> **For Releases Upload**:
> Please ensure **`version.json` is attached to this GitHub Release alongside the 4 archive packages**. The in-app updater relies on `version.json` to verify package checksums and determine update availability.

---

### 🔄 Upgrade Instructions

#### Method A: In-App Automatic Update (Recommended)
1. Open Tanuyomi in your browser and navigate to **Settings** → **Maintenance & Advanced** (or click the update badge in the header).
2. Click **Check for Updates**. When `v0.1.2-beta` is detected, click **Update Now**.
3. Tanuyomi will securely download, verify the SHA256 checksum, and apply the update automatically.

#### Method B: Manual Overwrite
1. Stop the running Tanuyomi instance (close the GUI control panel window or click **🛑 Stop Server** at the bottom of the Settings page).
2. Extract the new archive and copy its contents over your existing installation (or extract to a new folder and move your existing `workingData/` directory into it).
   - Your settings, reading progress, and thumbnail cache in `workingData/` will be preserved automatically.
3. Launch `tanuyomi.exe` (or `./tanuyomi` on macOS/Linux).

---

### 💬 Feedback & Bug Reports
If you encounter any issues or have feature suggestions, please feel free to open an issue on [GitHub Issues](https://github.com/nullPonta/tanuyomi-release/issues) or reach out via our official website:

- 🌐 Official Website: https://nullponta.github.io/tanuyomi-website/
