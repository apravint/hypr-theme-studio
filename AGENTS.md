# AGENTS.md - Developer & AI Agent Guide for hypr-theme-studio 🤖

## 🎯 Repository Overview
**hypr-theme-studio**: Hypr Theme Studio is an open-source, zero-restart visual theme switcher and 3D WebGL palette simulator engineered for Hyprland, Sway, and modern Wayland desktops. It switches window borders, Waybar gradients, Alacritty colors, GTK themes, and terminal environments simultaneously in <100ms with zero restarts. - 43 Curated Palettes: Tokyo Storm, Cyberpunk Neon, Synthwave 84, Catppuccin Mocha, Dracula, Nord, Rosé Pine, Vesper, Oxocarbon, Aura Dark, Gruvbox, and 30+ more.

---

## 🏗️ Repository Architecture
Key directories and entrypoints: `LICENSE, README.md, bin/, index.html, src/, themes/, webgl-studio/`.

### Tech Stack & Runtime
- **Language:** Python 3.10+ (Type-annotated, modern packaging)
- **Packaging & Tooling:** `pyproject.toml` / `setup.py` / `pip install -e .`

## ⚙️ Executable Verification Commands

Before declaring any coding or refactoring task complete, run verification:

### 1. Fast Syntax & Bytecode Compilation
```bash
python3 -m py_compile $(find . -maxdepth 3 -name '*.py' -not -path '*/.*' -not -path '*/venv/*')
```

### 2. Static Analysis & Linting
```bash
ruff check . || flake8 . || python3 -m py_compile **/*.py
```

### 3. Test Suite Execution
```bash
python3 -m unittest discover -s tests
```

---

## 🛡️ Coding & Safety Guidelines for Autonomous Agents

1. **Documentation Integrity:** Preserve all existing docstrings, header comments, and licensing banners. Never delete context unless specifically instructed.
2. **Zero Hardcoded Secrets:** Never embed API keys, OAuth tokens, personal access tokens, or sensitive credentials in committed files. Read credentials exclusively from environment variables or secure credential paths.
3. **Git Hygiene:**
   - Do not force-push (`git push --force`) or execute destructive resets.
   - Never modify root git configurations or harness infrastructure outside task scope.
   - Keep git diffs atomic, focused, and verified before committing.
4. **Agent Workflow Protocol:**
   - **Plan:** Inspect codebase architecture and dependencies before editing.
   - **Act:** Make minimal, clean, high-precision changes.
   - **Verify:** Run the appropriate verification commands listed above.
   - **Reflect:** Confirm zero regressions and review `git diff`.

---
*Maintained by Ayyappa Pravin • Built for Antigravity, Claude, Cursor & Autonomous AI Agents.*
