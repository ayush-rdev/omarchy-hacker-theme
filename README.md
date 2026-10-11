# ⚡ Omarchy Hacker Theme

[![Omarchy](https://img.shields.io/badge/Omarchy-Theme-00FF88?style=for-the-badge&logo=archlinux&logoColor=0A0E0F)](https://omarchy.org)
[![Hyprland](https://img.shields.io/badge/Hyprland-Wayland-38BDF8?style=for-the-badge&logoColor=white)](https://hyprland.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-00E5FF?style=for-the-badge)](LICENSE)

An elite, high-contrast, cyberpunk-inspired dark hacker theme built specifically for **[Omarchy](https://omarchy.org/)** and **Hyprland**. Featuring an obsidian charcoal backdrop (`#0A0E0F`), vibrant phosphor cyber-green accents (`#00FF88`), electric cyan highlights (`#00E5FF`), razor-thin polygonal windows with rotating multi-stop border glow, and a curated gallery of **12 high-resolution 4K/5K wallpapers**.

![Hacker Theme Preview](preview.png)

---

## ⚡ Quick Install

Install directly using the Omarchy CLI:

```bash
omarchy theme install https://github.com/ayush-rdev/omarchy-hacker-theme.git
```

To apply it manually if already downloaded:

```bash
omarchy theme set hacker
```

---

## 🎨 Palette Architecture

Unlike traditional green themes that tint all ANSI colors (breaking diffs and compiler errors), the **Hacker** palette maintains true semantic contrast:

| Role | Color | Hex Code | Purpose |
|---|---|---|---|
| **Background** | ⬛ Dark Charcoal | `#0A0E0F` | Deep obsidian backdrop with minimal eye strain |
| **Accent** | 🟩 Neon Green | `#00FF88` | Primary active accent, cursor glow, focus indicators |
| **Cyan Glow** | 🟦 Electric Cyan | `#00E5FF` | Secondary cyber glow and telemetry highlight |
| **Blue** | 🔷 Ice Blue | `#38BDF8` | Hyprland border gradient stop & process gauges |
| **Foreground** | ⬜ Clean Mint White | `#E1E8E6` | High-readability terminal and UI typography |
| **Red (Error)** | 🟥 Crimson Rose | `#F43F5E` | Alerts, failed tests, deletion diffs, auth errors |
| **Yellow (Warn)** | 🟨 Amber Gold | `#EAB308` | Warnings, branch dirty states, caution indicators |

---

## 🖼️ Curated 4K/5K Wallpaper Gallery

The theme bundles 12 curated wallpapers matching the colorway. Cycle through them anytime with `omarchy theme bg next`:

| # | File | Resolution | Style |
|---|---|---|---|
| 1 | `1-cyberpunk-neon-green.png` | 2560 × 1440 | Cyberpunk neon green anime aesthetic |
| 2 | `2-arch-workstation.jpg` | 3000 × 1686 | Arch Linux battle station & dual-screen terminal |
| 3 | `3-lain-night-terminal.jpg` | 3996 × 2250 | Serial Experiments Lain CRT cyber-deck |
| 4 | `4-cyber-interface.jpg` | 4552 × 2580 | Holographic telemetry HUD interface |
| 5 | `5-matrix-code-rain.png` | 5120 × 2880 (5K) | High-density vertical matrix glyph cascade |
| 6 | `6-matrix-falling-code.jpg` | 3840 × 2160 (4K) | Phosphor green cascading matrix code stream |
| 7 | `7-cyber-shinjuku-night.jpg` | 3840 × 2160 (4K) | Tokyo cyberpunk alleyways soaked in neon glow |
| 8 | `8-cyber-geometric-grid.jpg` | 5000 × 3542 (5K) | Dark vector geometric grid with cyber lines |
| 9 | `9-stealth-mono-rain.jpg` | 3840 × 2160 (4K) | Stealth monochrome dark digital glyphs |
| 10 | `10-neon-green-street.jpg` | 3840 × 2160 (4K) | Rain-soaked cyber street reflecting emerald lights |
| 11 | `11-dark-circuit-nexus.png` | 1920 × 1080 | Minimalist dark motherboard / circuit traces |
| 12 | `12-hacker-command-center.jpg` | 3840 × 2160 (4K) | Atmospheric late-night mainframe workstation |

---

## 🖥️ Recommended Hyprland Look'n'Feel

To achieve the signature polygonal chamfered corners and animated rotating borders, add or verify the following in `~/.config/hypr/looknfeel.lua`:

```lua
hl.config({
  general = {
    gaps_in = 2,
    gaps_out = 4,
    border_size = 1,
  },

  decoration = {
    -- Rigid angular chamfered/cut corners (benzene / cyber polygonal aesthetic)
    rounding = 8,
    rounding_power = 1.0,
  },
})

-- Continuous animated 4-stop rotating cyber gradient
hl.animation({ leaf = "borderangle", enabled = true, speed = 25, bezier = "linear", style = "loop" })
```

---

## ⌨️ Recommended Keybinding

To switch wallpapers on the fly from your keyboard, add this line to `~/.config/hypr/bindings.lua`:

```lua
o.bind("SUPER + W", "Cycle Wallpaper", "omarchy theme bg next")
```

---

## 🪟 Supported Integrations

When installed via Omarchy, template configs are generated automatically for:
- **Terminals**: Foot, Ghostty, Kitty, Alacritty
- **Shell & Bar**: Quickshell (Omarchy Shell bar, launcher, popups, lock screen)
- **Editors**: Neovim (`bjarneo/aether.nvim`), VS Code, Helix
- **System**: Btop, Starship, GTK, Fastfetch

---

## 🗑️ Uninstallation

To remove the theme:

```bash
rm -rf ~/.config/omarchy/themes/hacker
omarchy theme set "Tokyo Night" # or your preferred theme
```

---

## 📄 License

MIT © [ayush-rdev](https://github.com/ayush-rdev)
