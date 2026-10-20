# 🍃 Tanuyomi（たぬヨミ）- Official Releases

<p align="center">
  <strong>開けば、そこにあなたの書斎がある。</strong><br>
  PCの大容量漫画・書籍・動画・PDFを、同一Wi-Fi内のスマホ・タブレット・PCのブラウザからサクサク鑑賞できる自前ホスト型メディアサーバー
</p>

<p align="center">
  <a href="https://github.com/nullPonta/tanuyomi-release/releases/latest"><img src="https://img.shields.io/github/v/release/nullPonta/tanuyomi-release?include_prereleases&label=Latest%20Release&color=2ea44f" alt="Latest Release"></a>
  <a href="https://nullponta.github.io/tanuyomi-website/"><img src="https://img.shields.io/badge/Website-Live-brightgreen" alt="Official Website"></a>
  <a href="https://ci-en.net/creator/40053"><img src="https://img.shields.io/badge/Ci--en-Official%20Creator-orange" alt="Ci-en"></a>
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-blue" alt="Platform">
  <a href="https://github.com/nullPonta/tanuyomi-release/blob/main/LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg" alt="License: MIT"></a>
</p>

---

## 📌 公式リンク

- 🌐 **公式Webサイト (LP)**: [https://nullponta.github.io/tanuyomi-website/](https://nullponta.github.io/tanuyomi-website/)
- 📦 **最新版ダウンロード (Releases)**: [https://github.com/nullPonta/tanuyomi-release/releases/latest](https://github.com/nullPonta/tanuyomi-release/releases/latest)
- 📜 **全バージョン更新履歴 (Changelog)**: [https://github.com/nullPonta/tanuyomi-release/releases](https://github.com/nullPonta/tanuyomi-release/releases)
- 🍃 **Ci-en 公式ページ（開発日誌・お知らせ）**: [https://ci-en.net/creator/40053](https://ci-en.net/creator/40053)
- 🐛 **不具合報告・機能要望 (Issues)**: [https://github.com/nullPonta/tanuyomi-release/issues](https://github.com/nullPonta/tanuyomi-release/issues)

---

## 📖 Tanuyomi（たぬヨミ）とは？

Tanuyomi は、PC や自宅サーバーに保存してある自炊漫画・書籍（ZIP / CBZ / PDF）や動画ファイルを、同一 Wi-Fi 内のスマートフォン・タブレット・PC のブラウザから超高速・快適に閲覧・ストリーミング再生できる**自前ホスト型のメディアサーバー**です。

面倒なインストール作業や外部データベースの準備は一切不要。ZIP を解凍して実行するだけで、すぐにお手元のコレクションをお気に入りの端末から楽しめます。

### ✨ 主な機能と特徴

- **📖 快適な見開き漫画・書籍ビューワー**:
  - ZIP / CBZ / PDF / 各種画像（WebP, AVIF, BPG, PNG, JPG, GIF等）の直接閲覧に対応（書庫の事前解凍は不要）。
  - 右開き・左開き・見開き合成表示に対応。表紙の単ページ判定や見開きズレ補正を自動処理。
  - スマホのタッチスワイプやPCのキーボードショートカット（`F`で全画面、`R`で90°回転、`L`で一覧ドロワー等）で軽快に操作。
  - サムネイル一覧ドロワーから目的のページへ瞬時にジャンプ。
- **🎬 100コマシーンシーク付き動画プレイヤー**:
  - 動画から100枚のシーンサムネイルを自動生成。シークバーと連動したプレビューで、見たい場面を瞬時に発見。
  - ブラウザ標準フォーマット（MP4 / WebM / MKV 等）の軽快なストリーミング再生。
  - 速度変更（0.5x 〜 2.0x）、全画面再生、キーボード操作に対応。
- **💻 デスクトップGUIコントロールパネル**:
  - サーバーの起動・停止、LAN内アクセス用IPアドレス、ポート番号をグラフィカルに表示。
  - **「スマホ接続用QRコード」** を標準搭載。スマホのカメラでかざすだけで即座に接続できます。
- **📁 Webファイラー＆バックグラウンド処理**:
  - Web画面からフォルダ作成・ファイル名変更・整理が可能。
  - PDFから高画質画像を抽出して扱いやすいZIP書庫へ自動変換。
  - 書庫内画像の一括WebP変換など、容量削減処理をバックグラウンドジョブとして安全に実行。
- **🚀 完全自己完結・ポータブル**:
  - Windows版は FFmpeg / Poppler / libbpg / SQLite を内包しており、追加の外部ツール導入は一切不要。
  - レジストリを変更せず、フォルダ移動やUSBメモリ等での持ち運びも自由です。
- **⚡ 超高速＆省リソース**:
  - .NET 10 + ASP.NET Core Blazor Server + SQLite WAL による超高速レスポンスと省メモリ設計。
- **🔄 アプリ内ワンクリック自動アップデート**:
  - 新バージョンが公開されると、設定画面からワンクリックで最新版へ安全に更新・再起動できます。

---

## 📦 配布パッケージ一覧

お使いの OS・環境に合わせて、[最新リリースページ](https://github.com/nullPonta/tanuyomi-release/releases/latest) よりダウンロードしてください。

| パッケージ名                                | 対象環境                             | 特徴・必要環境                                                                                     |
| :------------------------------------------ | :----------------------------------- | :------------------------------------------------------------------------------------------------- |
| **`tanuyomi-<version>-win-x64.zip`**        | **Windows 10 / 11 (64-bit)**         | **【推奨】** 外部ツール（FFmpeg, Poppler等）を全同梱。解凍するだけで即座に動作する完全ポータブル版 |
| **`tanuyomi-<version>-osx-arm64.tar.gz`**   | **macOS (Apple Silicon: M1〜M4)**    | Homebrew からツールを利用（`brew install ffmpeg poppler`）                                         |
| **`tanuyomi-<version>-linux-x64.tar.gz`**   | **Linux x64 (Ubuntu / Debian等)**    | パッケージマネージャーからツールを利用（`apt install ffmpeg poppler-utils`）                       |
| **`tanuyomi-<version>-linux-arm64.tar.gz`** | **Linux ARM64 (Raspberry Pi 4/5等)** | 省電力な自作NAS・小型サーバー向け                                                                  |

> [!TIP]
> アプリの更新メタデータファイル `version.json` は、アプリ内自動アップデート機能（`AppUpdateService`）が自動参照するためのファイルです。通常の手動インストールではダウンロード不要です。

---

## 🚀 クイックスタート

### 1. ダウンロードと展開
1. [Releases の最新版](https://github.com/nullPonta/tanuyomi-release/releases/latest) から、お使いのOSに合ったアーカイブ（Windowsなら `*-win-x64.zip`）をダウンロードします。
2. 任意の作業フォルダ（例: `C:\Tools\Tanuyomi\` やデスクトップ）に展開します。
   - ※`C:\Program Files\` などの管理者権限が必要なフォルダは避けてください（同フォルダ内の `workingData/` に設定やキャッシュを保存するため）。

### 2. 起動
- **Windows**: 展開したフォルダ内の **`tanuyomi.exe`** をダブルクリックして実行します（GUI コントロールパネルが立ち上がります）。
- **macOS / Linux**: ターミナルで展開ディレクトリに移動し、実行権限を付与して起動します。
  ```bash
  chmod +x ./tanuyomi
  ./tanuyomi
  ```

### 3. PC のブラウザで利用開始
- 自動的にブラウザが立ち上がるか、またはブラウザを開いて `http://localhost:5005` にアクセスします。
- 画面上部の「設定」（または初回起動ダイアログ）から、漫画や動画が保存されているフォルダを**「基準フォルダ」**として追加してください。サムネイルの自動生成が始まり、すぐに鑑賞できます。

### 4. スマホ・タブレットからアクセス
1. スマホやタブレットを、PCと同じ自宅の Wi-Fi（LAN）に接続します。
2. Windows の GUI パネルに表示されている **「スマホ接続用QRコード」** をスマホのカメラで読み取ります（または画面に表示されたローカルURL `http://192.168.x.x:5005` をスマホのブラウザに入力）。
3. 専用アプリのインストールは不要です。Safari や Chrome などの標準ブラウザですぐにライブラリが開きます！

---

## 🔄 アップデート方法

### 方法A: アプリ内自動アップデート（推奨）
1. Tanuyomi の画面右上または「設定」→「保守・詳細」の **「更新を確認」** をクリックします。
2. 新バージョンが検知されたら **「今すぐアップデート」** をクリックします。
3. 自動的に安全なダウンロード・検証・ファイル置換・再起動が行われます。

### 方法B: 手動上書きアップデート
1. 実行中の Tanuyomi を停止します（GUI ウィンドウを閉じるか、Web画面の「設定」→「一般」→「🛑 サーバーを停止」）。
2. 新しいバージョンの ZIP / tar.gz を展開し、既存のフォルダへ上書きコピーします。
   - 設定・お気に入り・読書履歴（`workingData/tanuyomi.db`）やサムネイルキャッシュはそのまま自動で引き継がれます。
3. 再度 `tanuyomi.exe`（Linux/Macは `./tanuyomi`）を起動します。

---

## ⚠️ よくある質問・注意事項 (FAQ)

<details>
<summary><strong>Q. Windows SmartScreen（「WindowsによってPCが保護されました」）が表示されます</strong></summary>

個人開発のオープンソースバイナリのため、高額な商用EVコードサイニング証明書による署名を行っていません。悪意のあるソフトウェアではありませんのでご安心ください。  
**「詳細情報」をクリックし、現れた「実行」ボタンを選択** して起動してください。
</details>

<details>
<summary><strong>Q. スマホやタブレットから接続できません</strong></summary>

以下の点をご確認ください：
1. **Wi-Fi の確認**: PC とスマホが同じルーターの Wi-Fi（LAN）に接続されているか確認してください（ゲストWi-Fi等のプライバシーセパレーター機能が有効な場合は接続できないことがあります）。
2. **Windows ファイアウォール**: 初回起動時に Windows Defender ファイアウォールのダイアログが表示された場合は、「プライベート ネットワーク」にチェックを入れてアクセスを許可してください。
3. **ネットワーク設定**: Tanuyomi の設定画面（`/settings`）で「ネットワーク公開範囲」が「同じネットワーク（LAN）の端末からの接続を許可」になっているかご確認ください。
</details>

<details>
<summary><strong>Q. インターネット経由で外出先からもアクセスできますか？</strong></summary>

Tanuyomi は**家庭内プライベートネットワーク（LAN）での利用を想定**して設計されており、ログイン認証機能を持っていません。  
ルーターのポート開放（ポートマッピング）によるインターネットへの直接公開は**セキュリティ上大変危険ですので絶対に行わないでください**。  
外出先から利用したい場合は、**Tailscale** や **WireGuard** などの安全なメッシュVPNを導入し、VPN経由でアクセスすることを強く推奨します。
</details>

<details>
<summary><strong>Q. macOS / Linux で動画サムネイルや PDF が表示されません</strong></summary>

Windows版と異なり、macOS および Linux 版には FFmpeg や Poppler などの外部バイナリを同梱していません。お使いのシステムのパッケージマネージャーから導入してください。
- **macOS**: `brew install ffmpeg poppler`
- **Ubuntu / Debian**: `sudo apt update && sudo apt install -y ffmpeg poppler-utils`
- **Arch Linux**: `sudo pacman -S ffmpeg poppler`
</details>

---

## 💬 フィードバック・コミュニティ

バグ報告、新機能のご要望、動作確認のご連絡などはお気軽にどうぞ！

- **不具合報告・改善要望**: [GitHub Issues](https://github.com/nullPonta/tanuyomi-release/issues)
- **開発進捗・お問い合わせ**: [Ci-en 公式クリエイターページ](https://ci-en.net/creator/40053)

---

## 📜 ライセンス・クレジット

- **Tanuyomi 本体**: [MIT License](https://github.com/nullPonta/tanuyomi-release/blob/main/LICENSE)
- **同梱・利用サードパーティソフトウェア**:
  - [FFmpeg](https://ffmpeg.org/) (GPL v3+)
  - [Poppler](https://poppler.freedesktop.org/) (GPL v2/v3)
  - [libbpg](https://bellard.org/bpg/) (LGPL v2.1+ / BSD)
  - [SQLite](https://www.sqlite.org/) (Public Domain)

---

<details>
<summary><strong>🌐 English Summary (Click to expand)</strong></summary>

### About Tanuyomi
**Tanuyomi** is a lightweight, high-performance self-hosted media server designed to browse your manga archives (ZIP/CBZ/PDF) and stream videos directly from your PC to smartphones, tablets, and computers within your local Wi-Fi network—all via standard web browsers.

- **Fast & Responsive**: Powered by .NET 10 Blazor Server & SQLite WAL.
- **Portable**: No installation required. Just unzip and run.
- **Feature-Rich**: Double-page spread manga viewer, 100-scene video seek bar, built-in desktop control panel with QR code connection, web filer, and background conversion jobs.
- **Cross-Platform**: Binaries available for Windows (x64), macOS (Apple Silicon), and Linux (x64 / ARM64).

### Download
Download the latest binaries from [GitHub Releases](https://github.com/nullPonta/tanuyomi-release/releases/latest).

### Quick Start
1. Download and extract the archive for your operating system.
2. Run `tanuyomi.exe` (Windows) or `./tanuyomi` (macOS/Linux).
3. Open `http://localhost:5005` in your browser and register your media folder under "Settings".
4. To connect from your mobile device, make sure it's on the same Wi-Fi and simply scan the QR code displayed in the desktop control panel.

</details>
