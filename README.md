# omarchy-wallpaper-bank

Full wallpaper collection for [CornillieJ/omarchy](https://github.com/CornillieJ/omarchy), kept in its own repo so cloning the dotfiles repo stays fast (same pattern as [JaKooLit/Wallpaper-Bank](https://github.com/JaKooLit/Wallpaper-Bank) for Hyprland-Dots).

The main omarchy repo keeps only 5 curated wallpapers per theme in `config/omarchy/backgrounds/<theme>/` (enforced by a `.gitignore` allowlist there). This repo holds everything else.

## Layout

```
wallpapers/<theme-name>/*.jpg|png|webp
```

One folder per Omarchy theme name, matching `~/.config/omarchy/backgrounds/<theme>/` — the user-override location Omarchy's background switcher reads, alongside each theme's own shipped `backgrounds/`.

Filenames hint at where an image came from, not that it matters for use:

- `<theme>-<id>.jpg` — sourced from Wallhaven, `<id>` is that image's Wallhaven id
- `kool-0-<name>` / `kool-1-<name>` — from [JaKooLit/Wallpaper-Bank](https://github.com/JaKooLit/Wallpaper-Bank), distributed to every theme; `kool-0-` sorts first (filename-matched to that theme), `kool-1-` after (the general pool). The two `kool-1-0000-separator-black*.png` files are pure-black markers at that boundary, not real wallpapers.

## Using it

```bash
git clone https://github.com/CornillieJ/omarchy-wallpaper-bank.git ~/Projects/omarchy-wallpaper-bank
cp -r ~/Projects/omarchy-wallpaper-bank/wallpapers/* ~/.config/omarchy/backgrounds/
omarchy-theme-bg-cache   # refresh the switcher's thumbnail cache
```

Cloning to exactly `~/Projects/omarchy-wallpaper-bank` matters: that's the path `omarchy`'s `sync.sh` looks for and pushes to automatically from then on (see its README, [Wallpapers](https://github.com/CornillieJ/omarchy#wallpapers)) — a different path means keeping this repo in sync by hand.
