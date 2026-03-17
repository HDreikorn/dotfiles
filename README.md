# dotfiles

> *One prompt to rule them all, one prompt to find them...*

Personal configuration files, managed for portability across machines.

## ✧ Starship — Elvish Forest Theme

A Lothlórien-inspired [Starship](https://starship.rs/) prompt with powerline segments, earthy forest tones, and emoji icons.

### Preview

| Segment | Icon | Color |
|---------|------|-------|
| User | 🧝 | Gold `#C9A96E` |
| Directory | 🌿 | Forest green `#4A7C5C` |
| Git branch | 🌳 | Sage `#A8B8B0` |
| Go version | 🐹 | Amber `#CC9544` |
| Time | 🌙 | Stone `#A89688` |

### Setup

```bash
# Install starship (if not already)
curl -sS https://starship.rs/install.sh | sh

# Symlink the config
ln -sf ~/dotfiles/starship/starship.toml ~/.config/starship.toml
```

### Requirements

- [Starship](https://starship.rs/) prompt
- A [Nerd Font](https://www.nerdfonts.com/) for powerline glyphs ()
- Terminal with emoji support
