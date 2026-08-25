# Invisible Cursor For Brawlhalla

A simple guide on how to make your cursor completely invisible in Brawlhalla while keeping full mouse functionality.

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

### Step 3. Apply the Theme for Brawlhalla

Since Brawlhalla runs through XWayland, you need to set the cursor theme using environment variables in Steam's launch options.

**For Steam Launch Options:**

Right-click Brawlhalla in Steam → Properties → Launch Options, and add:

XCURSOR_THEME=InvisibleCursor XCURSOR_SIZE=24 %command%

That's it! Brawlhalla will now use the invisible cursor while your system keeps its normal cursor.

### Step 4. Reverting the Mouse to Visible

To revert the cursor back to normal, simply remove the launch options from Steam:

Right-click Brawlhalla in Steam → Properties → Launch Options, and delete:

XCURSOR_THEME=InvisibleCursor XCURSOR_SIZE=24 %command%

The cursor will go back to normal the next time you launch the game.

## Troubleshooting

### Brawlhalla still shows the normal cursor?
Make sure you added the XCURSOR_THEME variables to your Steam launch options exactly as shown above:

XCURSOR_THEME=InvisibleCursor XCURSOR_SIZE=24 %command%

### The theme isn't installing?
Make sure you copied the theme to the correct location:

ls ~/.local/share/icons/InvisibleCursor

### Command not found?
Make sure the theme is properly installed in ~/.local/share/icons/

## Notes

- This guide is specifically for Brawlhalla on Hyprland
- The invisible cursor works great for keyboard and mouse users
- The theme is completely transparent - no visible cursor at all!
- Your system cursor stays normal, only Brawlhalla gets the invisible cursor
- Using XCURSOR_THEME in launch options is the most reliable way to get it working

## Links

Invisible Cursor Theme GitHub: https://github.com/l-theanine/invisible-cursor-theme
