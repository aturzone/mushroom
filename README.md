# 🍄 Mushroom — Link Scanner

**Offline link safety scanner for the open-source ecosystem.**

Mushroom analyzes every URL before you navigate to it — using local heuristics only. No data ever leaves your browser.

---

## Features

- **Safety Score (0–100%)** for every link — shown as badge, tooltip, and overlay
- **5 Heuristic Analyzers**: Domain reputation, URL structure, protocol security, content patterns, behavioral analysis
- **Zero Network Requests** — all analysis happens offline using bundled pattern databases
- **3-Layer Navigation Interception** — catches link clicks, address bar, redirects, form submissions
- **Enterprise Config** — export/import JSON configuration files for organization-wide deployment
- **Warning Overlay** — shows detailed score breakdown before you visit a risky link
- **Full-Page Block** — dangerous URLs are blocked with a warning page
- **Scan History** — browse your recent URL scans with scores
- **Cross-Browser** — Chrome, Edge, Firefox, Safari

## What It Detects

| Threat | How |
|--------|-----|
| Phishing URLs | Keyword analysis, brand impersonation, known pattern matching |
| Homograph attacks | Punycode/IDN detection, mixed-script analysis |
| DGA domains | Shannon entropy analysis on domain labels |
| Open redirects | Redirect parameter scanning |
| Malicious downloads | Dangerous file extension detection (.exe, .scr, .bat, etc.) |
| URL obfuscation | Double encoding, base64 params, IP-based URLs |
| Insecure connections | HTTP, FTP, non-standard port detection |
| Data exfiltration | Long query string analysis, suspicious fragments |

## Install

### From Release (Recommended)

1. Go to [Releases](https://github.com/aturzone/mushroom/releases)
2. Download the ZIP for your browser
3. Open `chrome://extensions/` → Enable **Developer mode**
4. Drag the ZIP or click **Load unpacked**

### Build from Source

```bash
git clone https://github.com/aturzone/mushroom
cd mushroom
npm install
npm run build
```

Then load `dist/` as an unpacked extension.

## License

MIT — see [LICENSE](./LICENSE)
