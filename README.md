# Invisible Cursor For Brawlhalla

A simple guide on how to make your cursor completely invisible in Hyprland while keeping full mouse functionality for Brawlhalla.

## Installation Process

### Step 1. Download the Invisible Cursor Theme

Credits to: l-theanine

Download the invisible cursor theme from:
https://github.com/l-theanine/invisible-cursor-theme

Extract the downloaded ZIP file (it will typically be in your ~/Downloads/ folder).

### Step 2. Install the Theme

Create the icons directory and copy the theme:

mkdir -p ~/.local/share/icons/
cp -r ~/Downloads/invisible-cursor-theme-main/InvisibleCursor ~/.local/share/icons/

### Step 3. Apply the Theme System-Wide (Optional)

Find out your default cursor theme name before switching it. The default is usually: Adwaita.

Use hyprctl to instantly change your cursor to invisible:

hyprctl setcursor InvisibleCursor 24

That's it! Your cursor should now be completely invisible while still accepting clicks and movement inputs.

### Step 4. Apply the Theme for Brawlhalla (The Real Solution)

Since Brawlhalla runs through XWayland, hyprctl setcursor won't work for the game. Instead, you need to set the cursor theme using environment variables.

For Steam Launch Options:

Right-click Brawlhalla in Steam → Properties → Launch Options, and add:

XCURSOR_THEME=InvisibleCursor XCURSOR_SIZE=24 %command%

This will make Brawlhalla use the invisible cursor while your system keeps its normal cursor.

### Step 5. Reverting the Mouse to Visible

To revert the mouse to visible, use the same command with your default theme name:

hyprctl setcursor Adwaita 24

If you used the Steam launch option, just remove it from the launch options and the cursor will go back to normal.

## Troubleshooting

### The theme isn't applying?
Try restarting Hyprland:

hyprctl reload

### Normal cursor not coming back?
Replace the cursor name with your default one:

hyprctl setcursor Adwaita 24

### Brawlhalla still shows the normal cursor?
Make sure you added the XCURSOR_THEME variables to your Steam launch options exactly as shown above.

## Notes

- The invisible cursor works great for Brawlhalla, especially for keyboard and mouse users
- This works with Hyprland and XWayland apps
- The theme is completely transparent - no visible cursor at all!
- Using XCURSOR_THEME in launch options is the most reliable way to get it working in games

## Links

Invisible Cursor Theme GitHub: https://github.com/l-theanine/invisible-cursor-theme
Hyprland Wiki - Cursors: https://wiki.hyprland.org/Configuring/Variables/#cursor
