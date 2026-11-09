# Void

Near-monochrome, ultra-dark, quiet theme for Omarchy.

![Void preview](preview.png)

## Design Identity

Void delivers a deep, distraction-free environment built around pitch-black `#050506` surfaces, subtle charcoal framing `#1c1e22`, subdued readable foreground text `#b4b8bd`, and delicate pale cream `#d8d3bf` accents:

- **Surface Depth Hierarchy:** Deep `#050506` surfaces paired with `#030304`, `#020202`, and `#0d0e10` tiers for cards, popups, and scrims.
- **Hyprland Borders:** Coordinated dual-stop gradient (`rgba(d8d3bfee) rgba(5b5f66ee) 45deg`) for active windows and subtle `#1c1e22` for inactive windows.
- **ANSI Legacy Parity:** Full 16-color ANSI block (`color0` through `color15`) mapped directly into the Void palette for zero template evaluation warnings across terminal emulators and CLI tools.
- **Ultra-Dark GTK Integration:** Complete `@define-color` mappings in `gtk.css` for GTK 3 & GTK 4 (Libadwaita / Nautilus) to eliminate grey fallbacks.
- **Monochrome Outline Icons:** Native Breeze-Dark icon pairing for crisp, high-contrast monochrome outline folder views.

---

## Prerequisites

Void pairs with KDE's **Breeze Dark** icon suite to provide clean monochrome outline folder and action icons:

```sh
omarchy pkg add breeze-icons
# or: sudo pacman -S breeze-icons
```

---

## Installation

### For Omarchy 4+ (with Omarchy Shell)

Install directly via Omarchy Theme Manager:

```sh
omarchy theme install https://github.com/vispobish01-netizen/omarchy-void-theme.git
```

Apply the theme:

```sh
omarchy theme set void
```

---

## GTK 3 / GTK 4 (Nautilus) Theming

To ensure GTK applications (such as Nautilus / GNOME Files) immediately reflect Void's pitch-black surfaces, install the theme-set automation hook:

1. Create or place `20-gtk-theme.sh` in your theme hooks directory:

```bash
mkdir -p ~/.config/omarchy/hooks/theme-set.d
cat << 'EOF' > ~/.config/omarchy/hooks/theme-set.d/20-gtk-theme.sh
#!/bin/bash
set -euo pipefail

THEME_NAME="${1:-}"
CURRENT_THEME_DIR="${HOME}/.local/state/omarchy/current/theme"
USER_THEME_DIR="${HOME}/.config/omarchy/themes/${THEME_NAME}"
STOCK_THEME_DIR="/usr/share/omarchy/themes/${THEME_NAME}"

GTK_SOURCE=""
if [[ -f "${CURRENT_THEME_DIR}/gtk.css" ]]; then
  GTK_SOURCE="${CURRENT_THEME_DIR}/gtk.css"
elif [[ -n "${THEME_NAME}" && -f "${USER_THEME_DIR}/gtk.css" ]]; then
  GTK_SOURCE="${USER_THEME_DIR}/gtk.css"
elif [[ -n "${THEME_NAME}" && -f "${STOCK_THEME_DIR}/gtk.css" ]]; then
  GTK_SOURCE="${STOCK_THEME_DIR}/gtk.css"
fi

mkdir -p "${HOME}/.config/gtk-3.0" "${HOME}/.config/gtk-4.0"

if [[ -n "${GTK_SOURCE}" && -f "${GTK_SOURCE}" ]]; then
  ln -sf "${GTK_SOURCE}" "${HOME}/.config/gtk-4.0/gtk.css"
  ln -sf "${GTK_SOURCE}" "${HOME}/.config/gtk-3.0/gtk.css"
else
  [[ -L "${HOME}/.config/gtk-4.0/gtk.css" ]] && rm -f "${HOME}/.config/gtk-4.0/gtk.css"
  [[ -L "${HOME}/.config/gtk-3.0/gtk.css" ]] && rm -f "${HOME}/.config/gtk-3.0/gtk.css"
fi
EOF

chmod 755 ~/.config/omarchy/hooks/theme-set.d/20-gtk-theme.sh
```

Whenever `omarchy theme set void` runs, GTK 3 & GTK 4 styles are linked automatically.

---

## Wallpapers

Three bundled 1440p wallpapers in `.webp` format:
- `void-bowed.webp` (default)
- `void-fall.webp`
- `void-orchid.webp`

Switch between them with:

```sh
omarchy theme bg next
```
or through the Omarchy desktop menu under **Style → Background**.

<table>
  <tr>
    <td width="33%"><img src="previews/bowed.jpg" alt="Bowed wallpaper, Void"></td>
    <td width="33%"><img src="previews/fall.jpg" alt="Fall wallpaper, Void"></td>
    <td width="33%"><img src="previews/orchid.jpg" alt="Orchid wallpaper, Void"></td>
  </tr>
  <tr>
    <td align="center">Bowed</td>
    <td align="center">Fall</td>
    <td align="center">Orchid</td>
  </tr>
</table>

---

## Update

To pull the latest palette updates and wallpapers:

```sh
omarchy theme update
omarchy theme set void
```

---

## Removal

Switch to another theme first, then remove Void:

```sh
omarchy theme set catppuccin
omarchy theme remove void
```

---

## License

[MIT](LICENSE) © 2026 Void theme contributors
