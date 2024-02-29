# waybar-swayidle

waybar module to manage a swayidle instance (execute a program after pc has been idle for some time, e.g. locking screen or turning off screen).

# Requirements

Requires swayidle.

# Installation

```
git clone https://github.com/raffaem/waybar-swayidle $HOME/.config/waybar/waybar-swayidle
```

Put the following in `$HOME/.config/waybar/config`:

```
"custom/swayidle": {
    "exec": "$HOME/.config/waybar/waybar-swayidle/waybar-swayidle status",
    "interval": "once",
    "signal": 1,
    "return-type": "json",
    "tooltip": true,
    "format": "{}",
    "on-click": "$HOME/.config/waybar/waybar-swayidle/waybar-swayidle toggle"
},
```

Start a swayidle instance at start-up time.

For example, if you use hyprland, you can put the following in your `$HOME/.config/hypr/hyprland.conf`:

```
exec-once = /home/USERNAME/.config/waybar/waybar-swayidle/waybar-swayidle on
```
