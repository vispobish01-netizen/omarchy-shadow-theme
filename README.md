# Shadow

> A near-monochrome, ultra-dark, muted-sage theme for Omarchy.

![Shadow Preview](preview.png)

Shadow delivers a deep, distraction-free environment built around pitch-black `#050506` surfaces paired with calm, muted-sage accents (`#d8d3bf`), subtle borders, and balanced typography. Designed for prolonged focus and visual calm, every color in the palette is tuned for high contrast and legibility (exceeding WCAG AA contrast standards across body and UI chrome).

---

## Color Palette

| Token | Hex | Preview | Contrast on `#050506` | Description |
| :--- | :--- | :---: | :---: | :--- |
| `background` | `#050506` | ![](https://via.placeholder.com/15/050506/000000?text=+) | — | Base desktop and window background |
| `dark_background` | `#030304` | ![](https://via.placeholder.com/15/030304/000000?text=+) | — | Unfocused surfaces & deep containers |
| `darker_background` | `#020202` | ![](https://via.placeholder.com/15/020202/000000?text=+) | — | Scrims and backdrop overlays |
| `lighter_background` | `#14161a` | ![](https://via.placeholder.com/15/14161a/000000?text=+) | — | Elevated cards and hover fills |
| `foreground` | `#c2c6cc` | ![](https://via.placeholder.com/15/c2c6cc/000000?text=+) | **11.9:1** | Primary body text |
| `dark_foreground` | `#7c828c` | ![](https://via.placeholder.com/15/7c828c/000000?text=+) | **5.3:1** | Secondary text and metadata |
| `light_foreground` | `#a5aab2` | ![](https://via.placeholder.com/15/a5aab2/000000?text=+) | **8.7:1** | Subtle headers and active labels |
| `bright_foreground` | `#ebe7d8` | ![](https://via.placeholder.com/15/ebe7d8/000000?text=+) | **16.5:1** | Primary titles and bright highlights |
| `accent` | `#d8d3bf` | ![](https://via.placeholder.com/15/d8d3bf/000000?text=+) | **13.6:1** | Muted sage focus and active indicator |
| `selection` | `#24272e` | ![](https://via.placeholder.com/15/24272e/000000?text=+) | — | Selection highlight surface |
| `muted` | `#717883` | ![](https://via.placeholder.com/15/717883/000000?text=+) | **4.6:1** | Inactive borders & muted elements |

### Accent & Syntax Colors

| Color | Normal | Bright | Normal Hex | Bright Hex |
| :--- | :---: | :---: | :--- | :--- |
| **Red** | ![](https://via.placeholder.com/15/c46363/000000?text=+) | ![](https://via.placeholder.com/15/db8080/000000?text=+) | `#c46363` | `#db8080` |
| **Orange** | ![](https://via.placeholder.com/15/c48a5a/000000?text=+) | ![](https://via.placeholder.com/15/dda573/000000?text=+) | `#c48a5a` | `#dda573` |
| **Yellow** | ![](https://via.placeholder.com/15/c7a85d/000000?text=+) | ![](https://via.placeholder.com/15/dec178/000000?text=+) | `#c7a85d` | `#dec178` |
| **Green** | ![](https://via.placeholder.com/15/76a382/000000?text=+) | ![](https://via.placeholder.com/15/93bf9e/000000?text=+) | `#76a382` | `#93bf9e` |
| **Cyan** | ![](https://via.placeholder.com/15/74a5ab/000000?text=+) | ![](https://via.placeholder.com/15/91c2c8/000000?text=+) | `#74a5ab` | `#91c2c8` |
| **Blue** | ![](https://via.placeholder.com/15/6e92bd/000000?text=+) | ![](https://via.placeholder.com/15/8eb0d9/000000?text=+) | `#6e92bd` | `#8eb0d9` |
| **Magenta** | ![](https://via.placeholder.com/15/a28ab5/000000?text=+) | ![](https://via.placeholder.com/15/bda6cf/000000?text=+) | `#a28ab5` | `#bda6cf` |
| **Brown** | ![](https://via.placeholder.com/15/856a47/000000?text=+) | ![](https://via.placeholder.com/15/af8b5d/000000?text=+) | `#856a47` | `#af8b5d` |

---

## Wallpapers

Shadow includes three high-resolution 4K wallpapers and live video loops:

| `shadow-bowed` | `shadow-fall` | `shadow-orchid` |
| :---: | :---: | :---: |
| [![Shadow Bowed](backgrounds/shadow-bowed.webp)](backgrounds/shadow-bowed.webp) | [![Shadow Fall](backgrounds/shadow-fall.webp)](backgrounds/shadow-fall.webp) | [![Shadow Orchid](backgrounds/shadow-orchid.webp)](backgrounds/shadow-orchid.webp) |

Each wallpaper is accompanied by seamless ambient looping animations in `backgrounds/` and boot intro transitions in `backgrounds/intros/`.

---

## Installation

### Official Registry

Once listed in the official [Omarchy Theme Registry](https://themes.omarchy.org):

```bash
omarchy theme install shadow
```

### Direct from GitHub

You can install directly from this repository at any time:

```bash
omarchy theme install https://github.com/vispobish01-netizen/omarchy-shadow-theme
```

To apply the theme:

```bash
omarchy theme set shadow
```

---

## Credits & License

- **Theme Design:** vispobish & contributors
- **Icon Suite:** Pairs natively with [Yaru](https://github.com/ubuntu/yaru) (`Yaru-sage`)
- **License:** [MIT License](LICENSE)
