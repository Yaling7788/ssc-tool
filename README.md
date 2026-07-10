<div align="center">

<img src="assets/icon.svg" alt="SSC ASI Tool" width="76" height="76" />

# Supply Chain CYBER Exposure Discovery

### Attack-surface intelligence — mapped, charted, exportable — in a single HTML file.

A zero-install security console for querying, visualizing, and exporting supply-chain
cyber-exposure data, built on SecurityScorecard's Attack Surface Intelligence (ASI) API —
with a **fully offline demo mode** so you can explore every feature without a key.

<br />

**🔗 Live:** [ssc-tool.bodilabs.io](https://ssc-tool.bodilabs.io) &nbsp;·&nbsp; **▶ Launch:** [`app.html`](https://ssc-tool.bodilabs.io/app.html)

[![Version](https://img.shields.io/badge/version-6.0-35e0c4?style=for-the-badge)](#)
[![Single File](https://img.shields.io/badge/single--file-no%20build-38bdf8?style=for-the-badge)](#)
[![Demo Mode](https://img.shields.io/badge/demo%20mode-offline%20ready-0d9488?style=for-the-badge)](#-demo-mode)
[![License](https://img.shields.io/badge/license-MIT-64748b?style=for-the-badge)](LICENSE)

<br />

![JavaScript](https://img.shields.io/badge/JavaScript-ES2020-f7df1e?style=flat-square&logo=javascript&logoColor=black)
![jQuery](https://img.shields.io/badge/jQuery-3.6.4-0769ad?style=flat-square&logo=jquery&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-2.35-3f4f75?style=flat-square&logo=plotly&logoColor=white)
![Leaflet](https://img.shields.io/badge/Leaflet-1.7-199900?style=flat-square&logo=leaflet&logoColor=white)
![DataTables](https://img.shields.io/badge/DataTables-1.13-0f5499?style=flat-square)
![CDN + SRI](https://img.shields.io/badge/CDN-SRI%20pinned-16a34a?style=flat-square)

<br />

<img src="assets/overview-dark.png#gh-dark-mode-only" alt="Dashboard — dark theme" width="880" />
<img src="assets/overview-light.png#gh-light-mode-only" alt="Dashboard — light theme" width="880" />

</div>

---

## ✨ Overview

Point it at an attack-surface query — `os_type:'FortiOS'`, `(and has_ransomware:1 has_cve:1)`,
a whole portfolio of vendors — and it returns a live findings table, eleven ranked charts, and
a geographic threat map, all exportable to CSV/JSON. It runs entirely in the browser from one
HTML file: no server, no build step, nothing to install. The SecurityScorecard API is optional —
without a key it boots into **demo mode** backed by 1,500 deterministic, fictional findings.

## 🎯 Features

| | |
|---|---|
| 🔎 **ASI query builder** | Boolean logic (`and` / `or` / `not`), ranges, negation, and nine one-click threat-signal toggles (CVE, ransomware, breach, infection, MITRE TTP …). |
| 🧩 **Active-filter chips** | Every applied filter becomes a removable chip — click to remove, long-press to invert. |
| 📊 **Eleven ranked charts** | Threat actors, CVEs, products, ports, ASN, ISP, countries, states, cities, attributed domains, MITRE techniques — click any bar to drill in. |
| 🗺️ **Geographic threat map** | Interactive Leaflet map with zoom-scaled, severity-colored markers and light/dark basemaps. |
| 🗂️ **Portfolios & 3rd-party** | Search across vendor portfolios and expand to third-party (AVD) vendor discovery. |
| 📥 **Export everything** | CSV (preview or all findings), JSON, and re-indexed exports by domain, CVE, product, service, port, CPE, library, or org. |
| 🎨 **Dual themes + accent cycling** | A dark ops console and a light analyst report; the heart cycles the accent color. |

## 🧪 Demo Mode

> **No API key? No problem.** The dashboard ships with a self-contained demo engine.

- **Auto-activates** with no key, or when a live request is rejected (HTTP 401/403).
- **1,500 findings** from a seeded PRNG — identical on every load.
- **Full coverage:** search, facets, five portfolios, and third-party vendor detection resolve locally.
- **Offline map:** demo locations carry coordinates, so the map renders with no geocoding calls.

All demo data is fictional — `-demo.com` placeholder domains and reserved documentation/CGNAT IP ranges.

## 🚀 Quick Start

```bash
git clone https://github.com/Yaling7788/ssc-tool.git
cd ssc-tool
open app.html          # macOS  (or just open the live site)
```

Opens straight into demo mode. To use live data, click ⚙️, add your SecurityScorecard API key
(and optionally an OpenCage key for geocoding), and toggle **Demo** off.

## 🏗️ Repository Layout

```text
ssc-tool/
├── index.html      landing / help page  (site root on Cloudflare Pages)
├── app.html        the dashboard        (self-contained single file)
├── _headers        Cloudflare Pages security headers (CSP, HSTS, …)
├── assets/         icon, logo, screenshots
├── README.md
└── LICENSE
```

## 🔐 Security Notes

- **API keys live in browser `localStorage`, unencrypted** — use only on trusted machines; clear
  storage on shared workstations. Keys are sent **only** to `securityscorecard.io` / `opencagedata.com`.
- All CDN scripts/styles are **Subresource-Integrity (SRI) pinned**; a `_headers` **CSP** restricts
  script/connect origins to exactly what the app uses.
- User input is HTML-escaped before rendering; the client-side app has no backend and stores no data
  server-side.

## 📄 License

[MIT](LICENSE) — provided as-is for security research and supply-chain analysis.

<div align="center"><br /><sub>Built for cybersecurity professionals · v6.0</sub></div>
