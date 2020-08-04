# kde-plasmoids-workaround

Workaround to the following bug: https://bugs.kde.org/show_bug.cgi?id=360478

Whenever the display resolution is modified, the plasmoids (KDE Desktop Widgets) do not keep their initial size and position.

This workaround allows to save the config files of these plasmoids for each common display resolution you use (`save_kde_plasmoids_config`).
You can then easily restore one of them (`load_kde_plasmoids_config`).

# Resolution Log-in Screen
You may want to add the following line in `/usr/share/sddm/scripts/Xsetup` to control the resolution of the log-in screen
```
#!/bin/sh
# Xsetup - run as root before the login dialog appears
xrandr --output HDMI-2 --mode 3440x1440 -r 100
```