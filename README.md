Mouse follows Focus, Confirmed working on Debian 12 with X11, GNOME with Tiling Shell extension.

Do-it-yourself directional focus + cursor-centering (GNOME on X11)
1) Install tools
```
sudo apt update
sudo apt install wmctrl xdotool
```
(wmctrl activates a specific window; xdotool queries geometry and moves the pointer.)


2) Drop in one script that handles all 4 directions

```
cp ./focus-dir ~/.local/bin/focus-dir
chmod +x ~/.local/bin/focus-dir
```

3) Bind your keys in GNOME Settings → Keyboard → Keyboard Shortcuts → Custom Shortcuts

Add these four commands and set the shortcuts to your Ctrl+J/K/L/;:

    Focus Left + center

~/.local/bin/focus-dir left

Focus Down + center

~/.local/bin/focus-dir down

Focus Up + center

~/.local/bin/focus-dir up

Focus Right + center

~/.local/bin/focus-dir right

That’s it. Because the pointer jump is inside the command you invoke with your keybinding, it only happens on Ctrl+J/K/L/; — not when you switch windows with the mouse.