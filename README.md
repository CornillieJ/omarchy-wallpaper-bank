# omarchy-wallpaper-bank

Full wallpaper collection for [CornillieJ/omarchy](https://github.com/CornillieJ/omarchy), kept in its own repo so cloning the dotfiles repo stays fast (same pattern as [JaKooLit/Wallpaper-Bank](https://github.com/JaKooLit/Wallpaper-Bank) for Hyprland-Dots).

The main omarchy repo keeps only a handful of curated wallpapers per theme in `config/omarchy/backgrounds/<theme>/`. This repo holds the rest.

## Layout

```
wallpapers/<theme-name>/*.jpg|png
```

One folder per Omarchy theme name, matching `~/.config/omarchy/backgrounds/<theme>/` (the user-override location Omarchy's background switcher reads, alongside each theme's own shipped `backgrounds/`).

## Using it

```bash
git clone https://github.com/CornillieJ/omarchy-wallpaper-bank.git
cp -r omarchy-wallpaper-bank/wallpapers/* ~/.config/omarchy/backgrounds/
```

Kept in sync automatically by the `omarchy` repo's `sync.sh` backup script.
