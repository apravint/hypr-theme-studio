# 🎨 Hypr Theme Studio: Sovereign Theme Switcher & 3D WebGL Palette Studio

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-Linux%20%7C%20Hyprland%20%7C%20Wayland-purple.svg)]()
[![Engine](https://img.shields.io/badge/engine-Three.js%20r128%20%7C%20GTK3%20Cairo-cyan.svg)](https://github.com/mrdoob/three.js/)

**Hypr Theme Studio** is an open-source, zero-restart visual theme switcher and 3D WebGL palette simulator engineered for **Hyprland, Sway, and modern Wayland desktops**. It switches window borders, Waybar gradients, Alacritty colors, GTK themes, and terminal environments simultaneously in <100ms with zero restarts.

---

## ✨ Features

- **43 Curated Palettes**: Tokyo Storm, Cyberpunk Neon, Synthwave 84, Catppuccin Mocha, Dracula, Nord, Rosé Pine, Vesper, Oxocarbon, Aura Dark, Gruvbox, and 30+ more.
- **5 Cairo Live Swatches**: Every card renders 5 live circular Cairo color swatches: Background, Surface, Primary Accent, Secondary Accent, and Foreground Text.
- **Category Filter Pills**: Fast filtering by *All*, *Cyberpunk & Neon*, *Dark & OLED*, *Pastel & Soft*, *Monospaced & Minimal*, and *Retro & Warm* with live count badges.
- **Live Desktop Preview**: Hover or toggle live preview mode to instantly re-tint active Hyprland borders and Waybar acrylic glass without committing.
- **Theme Wallpaper Carousel**: Cycles and previews all bundled backgrounds per theme.
- **Brutalist Sharp Aesthetic**: Engineered with strict square edges (`rounding = 0`) for maximum visual clarity.
- **Interactive 3D WebGL Studio**: Inspect metallic, roughness, and glass transmission shaders in Three.js PBR rendering.

---

## 🏛️ Two Dedicated Modes

```
                               ┌────────────────────────┐
                               │   HYPR THEME STUDIO    │
                               └───────────┬────────────┘
                                           │
                    ┌──────────────────────┴──────────────────────┐
                    ▼                                             ▼
          [GTK3 Preview Grid]                           [3D WebGL Studio]
          Fast 2D theme card selector                   Interactive Three.js PBR
          with 5 live Cairo swatches                    metallic & glass shader sim
```

---

## 🌟 Curated Palettes (43 Total)

1. **Tokyo Storm** (Tokyo Night Storm)
2. **Cyberpunk Neon** (High Contrast Cyberpunk)
3. **Synthwave 84** (Retro 80s Sunset Grid)
4. **Catppuccin Mocha** (Official Catppuccin Mocha)
5. **Dracula** (Dracula Dark Official)
6. **Nord Frost** (Arctic Ice Blue)
7. **Rosé Pine Moon** (Rosé Pine Moon Minimalist)
8. **One Dark Pro** (Atom One Dark)
9. **Kanagawa Wave** (Japanese Wave Woodblock)
10. **Night Owl** (Deep Oceanic Blue)
11. **Oxocarbon** (IBM High-Contrast Tech)
12. **Vesper** (Ultra Minimalist Dark)
13. **Ayu Mirage** (Ayu Glow Mirage)
14. **Material Ocean** (Deep Navy Aquatic)
15. **Aura Dark** (Deep Purple Dark)
16. **Monokai Pro** (Monokai Pro High Contrast)
17. **Solarized Dark** (Solarized Classic)
18. **Ryoku Crimson** (High-Contrast Red Accent)
19. **Gruvbox Dark** (Retro Warm Groove)
20. **Matte Black** (Zero Distraction Stealth)
21. *...and 23 additional community curated themes!*

---

## 🚀 Quick Start

### 1. Installation
```bash
git clone https://github.com/apravint/hypr-theme-studio.git
cd hypr-theme-studio

# Link executable into PATH
mkdir -p ~/.local/bin
ln -sf $(pwd)/bin/hypr-theme-studio ~/.local/bin/
```

### 2. Usage

```bash
# Launch GTK3 Theme Selector Grid with Cairo swatches
hypr-theme-studio

# Launch Interactive 3D WebGL Material Studio
hypr-theme-studio 3d

# List all available themes
hypr-theme-studio list

# Switch to any theme instantly (<100ms, zero restarts)
hypr-theme-studio set tokyo-storm
hypr-theme-studio set cyberpunk-neon
hypr-theme-studio set synthwave-84

# Cycle to next theme
hypr-theme-studio next
```

---

## 📜 License
MIT License. Created by [Pravin](https://github.com/apravint) for [IRAM OS](https://github.com/apravint/iram-os).
