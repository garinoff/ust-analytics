# uST Analytics — Strategic Analysis Platform

> **Multilingual strategic analytical report on Unitsky String Technologies (GTI)**
> Languages: 🇷🇺 Russian · 🇬🇧 English · 🇮🇹 Italian · 🇪🇸 Spanish

[![Deploy to GitHub Pages](https://img.shields.io/badge/Deploy-GitHub%20Pages-blue?logo=github)](https://pages.github.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Languages](https://img.shields.io/badge/Languages-RU%20%7C%20EN%20%7C%20IT%20%7C%20ES-teal)](index.html)

---

## 📋 About

**uST Analytics** is a single-page analytical report covering five strategic layers of the
[uST (Unitsky String Technologies)](https://ust.inc) elevated transport system:

| Section | Content |
|---------|---------|
| **00. Situation Overview** | Inflection Point 2026, TRL 9, IP $400B |
| **01. Technology Layer** | Material intensity, Cd=0.06, pre-stress engineering |
| **02. Economic Layer** | CAPEX/OPEX, IRR 20–35%, IDC investment model |
| **03. System Layer** | Global logistics, offshore ports, linear cities (uCity) |
| **04. Geopolitics** | Climate resilience, sanctions bypass, uTerra biointegration |
| **05. Sources & Investment** | Official sources + RSW Systems crowdinvesting |

---

## 🚀 Quick Start

### Option 1 — Open locally
```bash
# Just open index.html in any browser
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

### Option 2 — Local dev server
```bash
# Python (no dependencies)
python -m http.server 8080
# Then open: http://localhost:8080

# Node.js
npx serve .
# Then open: http://localhost:3000
```

### Option 3 — GitHub Pages (production)
See [Deployment](#-deployment) section below.

---

## 📁 Project Structure

```
ust-analytics/
│
├── index.html                  # Main entry point (production-ready, self-contained)
├── llms.txt                    # AI crawler instructions (Perplexity, GPT, Claude)
├── robots.txt                  # Search engine crawler rules
├── sitemap.xml                 # XML sitemap (4 languages × 6 sections)
├── .gitignore
├── README.md
│
├── src/                        # Modular source files (for development)
│   ├── css/
│   │   └── styles.css          # Custom CSS (chart containers, nav, animations)
│   ├── js/
│   │   ├── i18n.js             # Translation strings (RU/EN/IT/ES) ~600 lines
│   │   ├── sectionMeta.js      # Per-section SEO titles + meta descriptions
│   │   └── app.js              # Core logic: navigate(), setLang(), charts
│   ├── sections/
│   │   ├── sidebar.html        # Navigation sidebar component
│   │   ├── dashboard.html      # Section 00: Situation Overview
│   │   ├── tech.html           # Section 01: Technology Layer
│   │   ├── econ.html           # Section 02: Economic Layer
│   │   ├── system.html         # Section 03: System Layer
│   │   ├── geo.html            # Section 04: Geopolitics
│   │   └── sources.html        # Section 05: Sources & Investment
│   └── components/             # (reserved for future shared components)
│
└── assets/
    ├── images/
    │   └── og-preview-source.png   # OG image source
    └── fonts/                      # (reserved for custom fonts)
```

---

## 🛠 Technology Stack

| Technology | Purpose |
|-----------|---------|
| **HTML5** | Structure, semantic markup |
| **Tailwind CSS** (CDN) | Utility-first styling, responsive layout |
| **Chart.js** (CDN) | Bar, Line, Doughnut charts with i18n labels |
| **Vanilla JS** | i18n engine, navigation, chart rendering |
| **Schema.org JSON-LD** | Rich snippets: TechArticle, FAQPage, Organization |
| **Open Graph + Twitter Card** | Social sharing previews |
| **llms.txt** | AI model crawling and citation guidance |

**No build step required.** Zero npm dependencies. Pure static HTML.

---

## 🌍 Multilingual Architecture

Language switching is handled entirely client-side via a JS i18n system:

```javascript
// Switch language
setLang('en');  // RU | EN | IT | ES

// All elements with data-i18n attribute are updated:
// <span data-i18n="nav1_title">01. Technology Layer</span>

// Chart.js labels also re-render on language switch
// Page title + meta description update per section × language (24 combinations)
```

**Translations coverage:**
- 130+ UI strings per language
- 6 section titles + subtitles
- 24 unique SEO titles (6 sections × 4 languages)
- 9 FAQ entries in Schema.org (multilingual)
- All Chart.js: labels, axes, tooltips, footers

---

## 📊 SEO Features

- ✅ Unique `<title>` + `<meta description>` per section × language
- ✅ `hreflang` for 4 languages + `x-default`
- ✅ Open Graph (Facebook, LinkedIn, Telegram, VK)
- ✅ Twitter/X Card (`summary_large_image`)
- ✅ Schema.org JSON-LD: `TechArticle`, `FAQPage` (9 Q&A), `Organization`, `WebSite`, `BreadcrumbList`
- ✅ `canonical` URL
- ✅ `llms.txt` for AI crawler guidance
- ✅ `robots.txt` with AI bot permissions
- ✅ `sitemap.xml` with hreflang annotations
- ✅ `history.replaceState` for anchor-based direct linking
- ✅ `preconnect` + `dns-prefetch` for CDN performance

---

## 🚢 Deployment

### GitHub Pages (Recommended)

1. Push to GitHub:
```bash
git init
git add .
git commit -m "feat: initial uST Analytics deployment"
git remote add origin https://github.com/YOUR_USERNAME/ust-analytics.git
git push -u origin main
```

2. Enable GitHub Pages:
   - Go to **Settings → Pages**
   - Source: **Deploy from branch** → `main` → `/ (root)`
   - Save → your site is live at `https://YOUR_USERNAME.github.io/ust-analytics/`

3. (Optional) Custom domain:
   - Add `CNAME` file with your domain (e.g. `ust-analytics.com`)
   - Configure DNS: CNAME → `YOUR_USERNAME.github.io`

### Netlify / Vercel (Alternative)

```bash
# Netlify CLI
netlify deploy --prod --dir .

# Vercel CLI
vercel --prod
```

Both support drag-and-drop deployment of the root folder.

---

## 💹 Investment

The **Sources & Investment** section includes a referral link to the official
crowdinvestment platform for GTI/uST projects:

🔗 **RSW Systems:** [rsw-systems.com/?r=134624](https://rsw-systems.com/?r=134624)

> ⚠️ Investments carry risk. This is not financial advice.

---

## 📄 License

MIT License — free to use, modify and distribute with attribution.

---

## 🔗 Official Sources

| Resource | URL |
|---------|-----|
| uST Inc. (GTI) | [ust.inc](https://ust.inc) |
| uST Global | [ust.com](https://ust.com) |
| Anatoli Unitsky | [unitsky.engineer](https://unitsky.engineer) |
| RSW Systems | [rsw-systems.com](https://rsw-systems.com/?r=134624) |

---

*Built with ❤️ for infrastructure investors and transport engineers worldwide.*
