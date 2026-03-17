# dotfiles

> *One prompt to rule them all, one prompt to find them...*

Personal configuration files, managed for portability across machines.

## ✧ Starship — Elvish Forest Theme

A Lothlórien-inspired [Starship](https://starship.rs/) prompt with powerline segments, earthy forest tones, and emoji icons.

| Segment | Icon | Color |
|---------|------|-------|
| User | 🧝 | Gold `#C9A96E` |
| Directory | 🌿 | Forest green `#4A7C5C` |
| Git branch | 🌳 | Sage `#A8B8B0` |
| Go version | 🐹 | Amber `#CC9544` |
| Time | 🌙 | Stone `#A89688` |

### Setup

```bash
ln -sf ~/dotfiles/starship/starship.toml ~/.config/starship.toml
```

## 🌲 iTerm2 — Elvish Forest Profile

Full iTerm2 color profile with separate light/dark mode colors, 10% transparency, and CaskaydiaCove Nerd Font.

**Key settings:**
- **Font**: CaskaydiaCove Nerd Font Mono, 12pt (with ligatures)
- **Transparency**: 10%
- **Dark background**: Deep forest green (`#2F4739`)
- **Light background**: Near-white (`#FAFAFA`)
- **Separate light/dark mode colors**: Yes

### Setup

iTerm2 loads profiles automatically from the Dynamic Profiles directory:

```bash
mkdir -p ~/Library/Application\ Support/iTerm2/DynamicProfiles
ln -sf ~/dotfiles/iterm2/elvish-forest.json \
  ~/Library/Application\ Support/iTerm2/DynamicProfiles/elvish-forest.json
```

Then in iTerm2: **Preferences > Profiles** → select "Elvish Forest" → **Other Actions > Set as Default**.

## 🐱 Kitty — Elvish Forest Theme

Same color palette adapted for [Kitty](https://sw.kovidgoyal.net/kitty/) terminal.

**Key settings:**
- **Font**: CaskaydiaCove Nerd Font Mono, 12pt (with ligatures)
- **Background opacity**: 90% (matches iTerm2's 10% transparency)
- **Background**: Deep forest green (`#2F4739`)
- **16 ANSI colors**: Matched to the iTerm2 profile

### Setup

Add one line to your existing `~/.config/kitty/kitty.conf`:

```bash
include ~/dotfiles/kitty/elvish-forest.conf
```

Or symlink the theme switcher:

```bash
mkdir -p ~/.config/kitty
ln -sf ~/dotfiles/kitty/current-theme.conf ~/.config/kitty/current-theme.conf
# Then add to kitty.conf:
# include ~/.config/kitty/current-theme.conf
```

Reload with `ctrl+shift+f5` or restart Kitty.

## Requirements

- [Starship](https://starship.rs/) prompt
- [iTerm2](https://iterm2.com/) and/or [Kitty](https://sw.kovidgoyal.net/kitty/)
- A [Nerd Font](https://www.nerdfonts.com/) (using CaskaydiaCove NF Mono)
- Terminal with emoji support

## New Machine Quick Start

```bash
git clone https://github.com/HDreikorn/dotfiles ~/dotfiles

# Starship
ln -sf ~/dotfiles/starship/starship.toml ~/.config/starship.toml

# iTerm2 (macOS)
mkdir -p ~/Library/Application\ Support/iTerm2/DynamicProfiles
ln -sf ~/dotfiles/iterm2/elvish-forest.json \
  ~/Library/Application\ Support/iTerm2/DynamicProfiles/elvish-forest.json

# Kitty (any platform)
echo 'include ~/dotfiles/kitty/elvish-forest.conf' >> ~/.config/kitty/kitty.conf
```
