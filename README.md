# 🎮 Icons Raw — Custom Neon SVG Badges for GitHub Profiles

> A collection of custom SVG badges with **neon glow effect**, Press Start 2P pixel font, brand colors, and automatic dark/light mode support.

<p align="center">
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/html.svg" height="32" alt="HTML"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/css.svg" height="32" alt="CSS"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/javascript.svg" height="32" alt="JavaScript"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/typescript.svg" height="32" alt="TypeScript"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/react.svg" height="32" alt="React"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/angular.svg" height="32" alt="Angular"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/astro.svg" height="32" alt="Astro"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/bootstrap.svg" height="32" alt="Bootstrap"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/tailwind.svg" height="32" alt="Tailwind"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/jquery.svg" height="32" alt="jQuery"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/cplusplus.svg" height="32" alt="C++"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/java.svg" height="32" alt="Java"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/power_bi.svg" height="32" alt="Power BI"/>
</p>

---

## ✨ Features

- 🌗 **Auto dark/light mode** via `prefers-color-scheme`
- 🎮 **Press Start 2P** pixel font embedded as base64
- 💡 **Neon glow effect** on text and border
- 🎨 **Brand colors** per technology
- 🔲 **Split layout** — icon block | label block
- 📦 **No dependencies** — pure SVG, works anywhere on GitHub

---

## 🚀 Usage

Reference the raw file directly in your README:

```html
<img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/javascript.svg" height="32" alt="JavaScript"/>
```

Combine several in a row:

```html
<p>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/html.svg" height="32" alt="HTML"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/css.svg" height="32" alt="CSS"/>
  <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/javascript.svg" height="32" alt="JavaScript"/>
</p>
```

---

## 📦 Available Badges

### 🌐 Frontend

| Preview | File | Technology |
|:-------:|------|------------|
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/html.svg" height="28"/> | `assets/html.svg` | HTML5 |
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/css.svg" height="28"/> | `assets/css.svg` | CSS3 |
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/javascript.svg" height="28"/> | `assets/javascript.svg` | JavaScript |
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/typescript.svg" height="28"/> | `assets/typescript.svg` | TypeScript |
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/react.svg" height="28"/> | `assets/react.svg` | React |
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/angular.svg" height="28"/> | `assets/angular.svg` | Angular |
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/astro.svg" height="28"/> | `assets/astro.svg` | Astro |
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/bootstrap.svg" height="28"/> | `assets/bootstrap.svg` | Bootstrap |
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/tailwind.svg" height="28"/> | `assets/tailwind.svg` | Tailwind CSS |
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/jquery.svg" height="28"/> | `assets/jquery.svg` | jQuery |

### 💻 Backend & Languages

| Preview | File | Technology |
|:-------:|------|------------|
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/java.svg" height="28"/> | `assets/java.svg` | Java |
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/cplusplus.svg" height="28"/> | `assets/cplusplus.svg` | C++ |

### 📊 Data & Analytics

| Preview | File | Technology |
|:-------:|------|------------|
| <img src="https://raw.githubusercontent.com/sorgazb/Icons_Raw/main/assets/power_bi.svg" height="28"/> | `assets/power_bi.svg` | Microsoft Power BI |

> More badges coming soon!

---

## 🛠️ Create Your Own

Template SVG structure — change `BRANDCOLOR`, `BASE64_LOGO` and `Label`:

```svg
<svg xmlns="http://www.w3.org/2000/svg" width="130" height="32" viewBox="0 0 130 32">
  <defs>
    <style>
      @font-face {
        font-family: 'Press Start 2P';
        src: url('data:font/truetype;base64,BASE64_FONT_HERE') format('truetype');
      }
      .bg      { fill: #0d1117; }
      .border  { fill: none; stroke: BRANDCOLOR; stroke-width: 1.5; }
      .divider { stroke: BRANDCOLOR; stroke-width: 1; opacity: 0.4; }
      .label   { fill: BRANDCOLOR; font-family: 'Press Start 2P', monospace; font-size: 7px; }
      .glow1   { fill: BRANDCOLOR; font-family: 'Press Start 2P', monospace; font-size: 7px; opacity: 0.6; }
      .glow2   { fill: BRANDCOLOR; font-family: 'Press Start 2P', monospace; font-size: 7px; opacity: 0.3; }
      @media (prefers-color-scheme: light) { .bg { fill: #ffffff; } }
    </style>
    <filter id="neon-sm"><feGaussianBlur stdDeviation="1.5" result="b1"/>
      <feMerge><feMergeNode in="b1"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
    <filter id="neon-lg"><feGaussianBlur stdDeviation="3.5" result="b2"/>
      <feMerge><feMergeNode in="b2"/><feMergeNode in="SourceGraphic"/></feMerge></filter>
    <clipPath id="pill"><rect width="130" height="32" rx="6" ry="6"/></clipPath>
  </defs>
  <rect x="0" y="0" width="130" height="32" class="bg" clip-path="url(#pill)"/>
  <rect x="38" y="0" width="92" height="32" fill="BRANDCOLOR" fill-opacity="0.08" clip-path="url(#pill)"/>
  <rect x="0.75" y="0.75" width="128.5" height="30.5" rx="5.5" ry="5.5" class="border" filter="url(#neon-sm)"/>
  <rect x="0.75" y="0.75" width="128.5" height="30.5" rx="5.5" ry="5.5" class="border"/>
  <line x1="38" y1="4" x2="38" y2="28" class="divider"/>
  <image href="data:image/svg+xml;base64,BASE64_LOGO" x="7" y="4" width="24" height="24"/>
  <text x="84" y="20" text-anchor="middle" class="glow2" filter="url(#neon-lg)">Label</text>
  <text x="84" y="20" text-anchor="middle" class="glow1" filter="url(#neon-sm)">Label</text>
  <text x="84" y="20" text-anchor="middle" class="label">Label</text>
</svg>
```

---

## ⭐ Support

If this helped you, consider leaving a **star** — it helps others find this resource!

---

<p align="center">Made with ❤️ for the GitHub community</p>
