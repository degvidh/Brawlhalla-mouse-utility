# Invisible Cursor For Brawlhalla

This is a simple guide i decided to make by my own on how to make your
cursor completely invisible in hyprland while keeping full mouse functionality 
for Brawlhalla. 

## Installation procces 

### Step 1. Downalod the invisible cursor theme
Credits to : https://github.com/l-theanine

Download the invisible cursor theme from:
[https://github.com/l-theanine/invisible-cursor-theme](https://github.com/l-theanine/invisible-cursor-theme)

Extract the downloaded ZIP file (it will typically be in your `~/Downloads/` folder).

### Step 2. Install the theme

Create the icons directory and copy the theme:

```
mkdir -p ~/.local/share/icons/
cp -r ~/Downloads/invisible-cursor-theme-main/InvisibleCursor ~/.local/share/icons/
```

### Step 3. Apply the theme 

> [!WARNING]
> Find out your default cursor theme name before switching it
> Or you can just use the default which is : Adwaita
> Set it back by using the same command just the cursor name :D 

Use hyprctl to instantly change your cursor to invisible:
```
hyprctl setcursor InvisibleCursor 24
```

That's it! Your cursor should now be completely invisible while still accepting clicks and movement inputs.

### Reverting the mouse to visible

To revert the mouse to visible you will use the same command
Simply with your mouse theme name or by using default and later 
finding out its name :D 

Use this command :
```
hyprctl setcursor Adwaita 24
```

## Throuble shooting (pew pew)

### If the theme isnt applying what do i do?

Try restarting hyprland with : 
```
hyprctl reload
```

### Normal cursor not coming back?
Try to replace the cursor name with the default one 
like in the next command : 
```
hyprctl setcursor Adwaita 24
```

## Notes 

- The invisible cursor works its great for Brawlhalla specifically for keyboard 
and mouse users like me :D 
- This works with hyprland but should work with x11 wm aswell tho i strongly despise
using this guide for x11
- The theme is completely transparent no visible cursor at all !!!

## Links 

- Invisible Cursor Theme GitHub: https://github.com/l-theanine/invisible-cursor-theme
