# 🎵 SoundScope — Real-time Audio Analyzer

A fully browser-based audio analyzer and visualizer. No server, no install, no uploads — runs locally in your browser using the Web Audio API.

**Live at:** `https://YOUR-USERNAME.github.io/audio-analyzer` (after deploy)

---

## ✨ Features

- 🎧 **File Player** — MP3, WAV, OGG, FLAC, AAC, M4A support
- 🎶 **Playlist Queue** — Drop multiple files, manage a full queue
- 🔀 **Shuffle & Loop** — Toggle either mode independently
- ⏩ **Playback Speed** — 0.5× to 2× speed control
- 🎙 **Microphone Input** — Live mic analysis in real-time
- 📊 **Frequency Spectrum** — Real-time FFT bar visualizer
- ⚡ **Live Waveform** — Time-domain waveform with gradient glow
- 〰 **Oscilloscope** — Raw signal with neon glow effect
- 🌀 **Radial Visualizer** — Circular spectrum visualizer
- 🎚 **10-Band EQ** — 32Hz → 16kHz frequency analysis
- 📏 **Live Stats** — BPM, RMS, Peak dB, Peak Frequency, Dynamic Range
- 🔊 **Stereo Meter** — L/R channel level meters with peak hold
- 📷 **Screenshot Export** — Save all visualizers as PNG
- 🌙 **Dark / Light Theme** — Toggle anytime
- ⌨ **Full Keyboard Control** — Space, arrows, N, P, L, X, M, S, T, O

---

## ⌨ Keyboard Shortcuts

| Key | Action |
|---|---|
| `Space` | Play / Pause |
| `← →` | Seek ±10 seconds |
| `↑ ↓` | Volume up / down |
| `N` / `P` | Next / Previous track |
| `L` | Toggle loop |
| `X` | Toggle shuffle |
| `M` | Toggle microphone |
| `S` | Save screenshot |
| `T` | Toggle dark/light theme |
| `O` | Open file picker |
| `?` | Show/hide shortcuts panel |

---

## 🚀 Deploy to GitHub Pages

### Step 1 — Create a GitHub Repo

1. Go to [github.com/new](https://github.com/new)
2. Name it: `audio-analyzer` (or anything you like)
3. Set it to **Public**
4. Do **NOT** check "Initialize with README"
5. Click **Create repository**

### Step 2 — Push Your Code

Open a terminal inside the `audio-analyzer` folder:

```bash
git init
git add .
git commit -m "Initial commit: SoundScope audio analyzer"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/audio-analyzer.git
git push -u origin main
```

> Replace `YOUR-USERNAME` with your GitHub username.

### Step 3 — Enable GitHub Pages

**Option A — GitHub Actions (auto-deploy on every push, already included):**
1. Go to your repo → **Settings** → **Pages**
2. Under Source, select **"GitHub Actions"**
3. Done! Every `git push` to `main` auto-deploys.

**Option B — Simple branch deploy:**
1. Go to **Settings** → **Pages**
2. Source → **"Deploy from a branch"**
3. Branch: `main` · Folder: `/ (root)`
4. Click **Save**

### Step 4 — Visit Your Live App 🎉

```
https://YOUR-USERNAME.github.io/audio-analyzer
```

Deployment takes ~60 seconds. Share the URL with anyone!

---

## 💻 Local Development

### VS Code + Live Server (Recommended)
1. Open the folder in VS Code
2. Install the **Live Server** extension (ritwickdey.liveserver)
3. Right-click `index.html` → **"Open with Live Server"**
4. Opens at `http://127.0.0.1:5500`

### Python
```bash
python3 -m http.server 8080
```

### Node.js
```bash
npx serve .
```

> Opening `index.html` via `file://` may block audio/mic APIs. Use a local server.

---

## 🔄 Updating After Deploy

```bash
git add .
git commit -m "describe your change"
git push
```

GitHub Actions redeploys automatically in ~60 seconds.

---

## 📁 Project Structure

```
audio-analyzer/
├── index.html              ← Entire app (single file, no dependencies)
├── README.md               ← This guide
└── .github/
    └── workflows/
        └── deploy.yml      ← Auto GitHub Pages deployment
```

---

## 🌐 Browser Compatibility

Chrome, Firefox, Safari (iOS 14.5+), Edge — all fully supported.

> Microphone input requires HTTPS or localhost. GitHub Pages and Live Server both qualify.

---

## 📝 Notes

- All processing is **100% in-browser** — no data leaves your device
- BPM estimation is energy-based, works best with music that has a clear beat
- Peak dB shows the highest peak since the current file started playing
- Screenshot exports a composite PNG of all four visualizers stacked
