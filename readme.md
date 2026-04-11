<img src="https://raw.githubusercontent.com/cybrcore/cybrcore/refs/heads/main/assets/repo-banners/cybr-gtk-banner-top.png"/>

> [!CAUTION]
> This theme is in early stage. Major refactor is in pipeline. Use at your own risk, ideally only if you plan to [contribute](../CONTRIBUTING.md).

# Showcase
<img src="https://raw.githubusercontent.com/cybrcore/cybrcore/refs/heads/main/assets/showcase/cybr-gtk.png"/>

# Steps
## 0. Before you start
- Make sure GTK is installed: `sudo pacman -S gtk-2.0 gtk-3.0`
- See [Installation Guide](https://github.com/cybrcore/cybrdots/blob/main/INSTALL.md) if you're coming from [cybr-hyprland](https://github.com/cybrcore/cybr-hyprland) and haven't set up prerequisites yet

## 1. Download GTK Theme
```sh
# Download only the gtk directory and install the CYBRgtk theme by creating ~/.themes directory and moving theme inside the ~/.themes dir
git clone --depth=1 --filter=blob:none --no-checkout https://github.com/cybrcore/cybr-waybar.git && cd cybr-waybar && git sparse-checkout init --cone && git sparse-checkout set waybar && git checkout main && mv waybar ~/.config/ && cd ~ && rm -rf cybr-waybar
```
↑ Unsure what this does? [Explanation](https://github.com/cybrcore/cybrdots/blob/main/INSTALL.md#How-sparse-checkout-works)  

## 2. Verify installation
```sh
ls -R ~/.themes/oomox-CYBRgtk
```

You should see: `assets/`, `cinnamon/`, `gtk-2.0/`, `gtk-3.0/`, `gtk-3.20/`, `metacity-1/`, `openbox-3/`, `unity/`, `xfwm4/` and `index.theme`

## 3. Apply
### For Hyprland users
Open hyprland.conf:
```sh
$EDITOR ~/.config/hypr/hyprland.conf
```
Add `env = GTK_THEME, oomox-CYBRgtk` into Themes inside ENV section:
```conf
# === THEME ==# #
    ..
# === ENV === #
    # XDG
    ..
    # QT
    ...
    # Tearing
	...
    # Themes
    env = GTK_THEME, oomox-CYBRgtk
```
### For non-Hyprland users (GNOME, XFCE, Cinnamon, etc.)
Apply the theme using your desktop environment’s GTK settings tool.

**Examples**:
- **GNOME**: Use GNOME Tweaks → Appearance → Legacy Applications → Select `oomox-CYBRgtk`  
- **XFCE**: Settings → Appearance → Style → Select `oomox-CYBRgtk`  
- **Cinnamon**: System Settings → Themes → Controls → Select `oomox-CYBRgtk`  

No environment variables are required.

## 4. Restart GTK apps or log out and back in
