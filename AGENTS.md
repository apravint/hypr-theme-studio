# AGENTS.md - Developer & AI Agent Operations Manual for `hypr-theme-studio` 🤖

This document is the definitive operational guide for autonomous AI coding agents (Antigravity, Claude, Cursor, OpenAI Codex, OpenHands) operating within this repository.

---

## 🎯 1. System Overview & Core Philosophy

**🎨 Hypr Theme Studio: Sovereign Theme Switcher & 3D WebGL Palette Studio**
> Hypr Theme Studio is an open-source, zero-restart visual theme switcher and 3D WebGL palette simulator engineered for Hyprland, Sway, and modern Wayland desktops. It switches window borders, Waybar gradients, Alacritty colors, GTK themes, and terminal environments simultaneously in <100ms with zero restarts. - 43 Curated Palettes: Tokyo Storm, Cyberpunk Neon, Synthwave 84, Catppuccin Mocha, Dracula, Nord, Rosé Pine, Vesper, Oxocarbon, Aura Dark, Gruvbox, and 30+ more. - 5 Cairo Live Swatches: Every card renders 5 live circular Cairo color swatches: Background, Surface, Primary Accent, Secondary Accent, and Foreground Text.

### Key Architectural Capabilities
- **43 Curated Palettes**: Tokyo Storm, Cyberpunk Neon, Synthwave 84, Catppuccin Mocha, Dracula, Nord, Rosé Pine, Vesper, Oxocarbon, Aura Dark, Gruvbox, and 30+ more.
- **5 Cairo Live Swatches**: Every card renders 5 live circular Cairo color swatches: Background, Surface, Primary Accent, Secondary Accent, and Foreground Text.
- **Category Filter Pills**: Fast filtering by *All*, *Cyberpunk & Neon*, *Dark & OLED*, *Pastel & Soft*, *Monospaced & Minimal*, and *Retro & Warm* with live count badges.
- **Live Desktop Preview**: Hover or toggle live preview mode to instantly re-tint active Hyprland borders and Waybar acrylic glass without committing.
- **Theme Wallpaper Carousel**: Cycles and previews all bundled backgrounds per theme.
- **Brutalist Sharp Aesthetic**: Engineered with strict square edges (`rounding = 0`) for maximum visual clarity.

---

## 🏗️ 2. Repository Structure & Directory Map

| Path | Role & Architectural Responsibility |
| :--- | :--- |
| `.github/` | Subsystem directory (.github) |
| `bin/` | Executable CLI scripts and dispatchers |
| `src/` | Primary source package and modules |
| `themes/` | Theme color schemes, styling templates, and wallpapers |
| `webgl-studio/` | Subsystem directory (webgl-studio) |

---

## ⚙️ 3. Executable Verification Pipeline

Before marking any task complete, an AI agent **must** run the following verification steps sequentially:

### Tier 1: POSIX Shell Syntax Validation
```bash
bash -n $(find . -maxdepth 3 -name '*.sh' -not -path '*/.*')
```

### Tier 2: ShellCheck Linting
```bash
shellcheck $(find . -maxdepth 3 -name '*.sh' -not -path '*/.*')
```

### Tier 3: Non-Destructive Simulation / Dry-Run
```bash
./install.sh --dry-run || ./install.sh --help
```

---

## 🛡️ 4. Architectural Invariants & Non-Negotiable Rules

### Strict Invariants ("Never Do" List):
1. **Strict Shell Safety:** Every shell script must declare `set -euo pipefail`. Never use `|| true` on critical installation or backup steps.
2. **Preserve Subshell Exit Codes:** Separate `local` variable declarations from command substitutions (ShellCheck SC2155).
3. **Safe Path Expansion:** Always quote variable expansions (e.g. `"$TARGET_DIR"`) to guard against whitespace and path traversal.

### Security & Environment Variables:
- All API keys and secrets must be loaded strictly from environment variables.
- Never commit `.env`, `.pem`, token files, or private credentials.

---

## 🤖 5. Autonomous Agent Operational Protocol

When dispatched to resolve an issue, implement a feature, or refactor code in this repo:

1. **Phase 1 — Explore & Plan:**
   - Read this `AGENTS.md` and relevant source files.
   - Check existing tests to establish the baseline.
2. **Phase 2 — Act (Surgical Implementation):**
   - Implement changes with minimal blast radius.
   - Adhere to the established code style and existing conventions.
3. **Phase 3 — Verify:**
   - Run the Tier 1, 2, and 3 verification commands listed above.
   - Ensure all existing and new tests pass cleanly.
4. **Phase 4 — Reflect:**
   - Review `git diff` to confirm zero unintended whitespace or collateral changes.
   - Confirm no untracked scratch files remain.

---
*Maintained by Ayyappa Pravin • Engineered for Antigravity, Claude, Cursor & Modern Autonomous AI Agents.*
