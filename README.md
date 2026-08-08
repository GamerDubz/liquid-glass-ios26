# Apple Liquid Glass — iOS 26 Optics & Physics System

[![iOS 26 Spec](https://img.shields.io/badge/Apple_HIG-iOS_26_Liquid_Glass-blue?style=flat-square&logo=apple)](https://developer.apple.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/GitHub-Pages_Deployment-181717?style=flat-square&logo=github)](https://gamerdubz.github.io/liquid-glass-ios26/)

A 1-to-1 web recreation of Apple's **Liquid Glass material system** (iOS 26 / WWDC 2025). Built with zero framework dependencies (Vanilla HTML, CSS & JavaScript), featuring real-time optical refraction, specular glare tracking, dynamic accent tinting, and interruptible physics springs.

---

## 🌟 Key Features

- **5-Layer Optical Material Engine**:
  1. **Frosted Backdrop**: Hardware-accelerated `-webkit-backdrop-filter: blur() saturate()`.
  2. **Translucent Tint Fill**: Spring-driven `hsl(var(--accent-h))` hue wash over content.
  3. **Hairline Rim**: Dual-gradient 1px border mimicking light bending over material edges.
  4. **Specular Top Sheen**: Radial light source and interactive glare tracking cursor position.
  5. **SVG Refraction Lens**: Distorts backdrop elements using SVG `feDisplacementMap` and magnification scale.
- **Physics Motion Engine**:
  - Interruptible spring dynamics carrying velocity on re-target.
  - Floating spring tab bar with dynamic pill positioning (`k=460, c=46`).
  - Drag-to-dismiss sheet with 1:1 touch tracking, progressive rubber-banding, and flick release velocity inheritance.
- **Interactive Portfolio Suite**:
  - **Environment Switcher**: Test material against 5 ambient wallpapers (Aurora, Sunset Glass, Deep Cyber, Emerald Frost, Solar Gold).
  - **Material Optics Inspector**: Live sliders for blur, saturation, specular glare, and refraction.
  - **Developer CSS Exporter**: Instant one-click copy of the production Liquid Glass CSS recipe.
  - **⌘K Command Palette**: Global search, keyboard navigation, and instant theme toggling.
  - **Accessibility**: Full `prefers-reduced-motion` & `prefers-reduced-transparency` compliance.

---

## 🔬 Material Architecture

```
┌─────────────────────────────────────────────────────────────┐
│ 5. SVG Refraction Lens (feDisplacementMap Filter)           │
├─────────────────────────────────────────────────────────────┤
│ 4. Specular Sheen & Glare (Radial Gradient Sheen)           │
├─────────────────────────────────────────────────────────────┤
│ 3. Hairline Rim (1px Dual Gradient Border)                  │
├─────────────────────────────────────────────────────────────┤
│ 2. Translucent Tint Fill & Dynamic Hue Wash                 │
├─────────────────────────────────────────────────────────────┤
│ 1. Frosted Backdrop (blur(22px) saturate(175%))             │
└─────────────────────────────────────────────────────────────┘
```

---

## 🚀 Quick Start

### Local Preview

No build steps required. Simply serve the `public/` directory with any static server:

```bash
# Serve locally using npx
npx serve public -l 3000
```

Open `http://localhost:3000` in your browser.

---

## 🌐 GitHub Pages Hosting

This repository is configured to deploy directly to **GitHub Pages** via GitHub Actions (`.github/workflows/deploy.yml`).

### Enabling GitHub Pages in Repository Settings:
1. Go to your repository on GitHub: `https://github.com/GamerDubz/liquid-glass-ios26`
2. Navigate to **Settings** > **Pages**.
3. Under **Build and deployment** > **Source**, select **GitHub Actions**.
4. Pushing to `main` will automatically trigger a build and publish your site!

---

## 📄 License

Distributed under the MIT License.
