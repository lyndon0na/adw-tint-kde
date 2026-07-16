# Adwaita Accent Tint for KDE Plasma
A dynamic libadwaita theme for KDE Plasma users that inherits accent colours from Plasma; uses a window geometry that looks consistent with other KDE apps (QT and GTK3); and has improved window decorations that mimic the Breeze theme, all while **tinting the windows with the accent colour**.

This theme uses GTK's `mix()` function against the **official Libadwaita base hex codes**. The result is a 7.5% tint that preserves all native shadows, card depths, and high-contrast elements.

> *Note: This is intended to be used with Plasma's tint windows with accent colour option*

[Demo Video](https://github.com/user-attachments/assets/34e03f30-f587-4099-a23c-2c8b6c73a730)

## Pre-requisite

### Plasma Tint 
Enable the tint windows with accent colour option:

1. Go to *System Settings* > *Colours & Themes* > *Colours*
2. Hover over a preferred colour scheme and click on the pencil icon
3. Go to *Options* and Select *Tint all colours with accent colour* 
4. Use the slider below to control the strength of the tint (Use a lower strength to achieve consistency with the tint in this theme)

## Installation

### 1. Initial setup
Copy the files into your local GTK4 config directory:

1. Open or create `~/.config/gtk-4.0/`.
2. Paste the contents of this repository here.
3. Go to Plasma colour settings and select a colour scheme.
4. Fully close and reopen any GTK4 app to see the changes.

> *Bonus tip: If you want to achieve the effect as shown in the video above, ensure that you select "Accent colour from wallpaper" option from the dropdown menu in Plasma's colour settings.*

### 2. Apply to Flatpak Apps
Because Flatpak applications run in an isolated sandbox, they cannot see your custom CSS by default. You need to grant them read-only access to your config folder.

Run this command in your terminal:
```bash
flatpak override --user --filesystem=xdg-config/gtk-4.0:ro
```
## Credits 
This project is built on the primary efforts of: 

- PakoVM's [Adwaita Accent Tint](https://github.com/pakovm-git/Adwaita-Accent-Tint) project 
- The [Rewaita](https://github.com/swordpuffin/Rewaita) project 
- The KDE Plasma team's efforts to bridge the gap between Plasma and libadwaita
