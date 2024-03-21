# waybar-idle

waybar module to manage a idle daemon (execute a program after pc has been idle for some time, e.g. locking screen or turning off screen).

# Requirements

Requires an idle daemon like swayidle or hypridle.

# Installation

```
git clone https://github.com/raffaem/waybar-idle $HOME/.config/waybar/waybar-idle
```

Put the following in `$HOME/.config/waybar/config`:

```
"custom/swayidle": {
    "exec": "$HOME/.config/waybar/waybar-idle/waybar-idle status",
    "interval": "once",
    "signal": 1,
    "return-type": "json",
    "tooltip": true,
    "format": "{}",
    "on-click": "$HOME/.config/waybar/waybar-idle/waybar-idle toggle"
},
```

Start an idle daemon instance at start-up time.

For example, if you use hyprland, you can put the following in your `$HOME/.config/hypr/hyprland.conf`:

```
exec-once = /home/USERNAME/.config/waybar/waybar-idle/waybar-idle on
```

