# xfce4-theme-switcher
A bash program allowing you to save and load complete themes for the xfce desktop environment.

![Alt Text](https://github.com/liamsgotgenes/xfce4-theme-switcher/blob/master/example.gif)

Xfce is a lightweight, customizable desktop environment for Linux and BSD operating systems. It is my personal favorite desktop and I have spent countless hours customizing and tweaking it to my liking. My only complaint has been that there is not a built-in tool to save complete themes and switch between them easily. This is what I am hoping this program will solve.

Xfce4-theme-switcher saves your configuration for:
* xfce4 desktop
* xfce4 panel
* xfwm4 (xfce4's window manager)
* xfce4 terminal
* All system font settings, window decoration layout, cursor themes, icons, DPI and more!

I also included support for [pywal](https://github.com/dylanaraps/pywal/tree/master/pywal) color-scheme themes for the terminal. If you are not familiar with pywal, it allows you to make terminal color-schemes on the fly based on your desktop's background and I highly recommend checking out their github page!

    Usage:
    xfce4-theme-switcher [OPTION]
    xfce4-theme-switcher -l [THEME NAME]
    xfce4-theme-switcher -s [THEME NAME]
    xfce4-theme-switcher -d [THEME NAME]
    
    Options:
    -d		delete a theme given by the theme name
    -l		load a theme given by the theme name
    -n		cycle to the next theme
    -p		cycle to the previous theme
    -s		save the current xfce4 settings as a theme given the theme name
    --list		list all themes
    --help		display this help
    --wal-theme	saves pywal terminal color-scheme must have pywal to use. Only use on saves
    
### Known Bugs
* Loading a theme that does not use pywal while a pywal color-scheme is currently active will result in the open terminals failing to change color. Any terminals opened after the theme is loaded will have the correct color
* On occasion, when loading a theme for the first time, the font may change and stay changed. This can be fixed by reloading the same theme again. I have only noticed this affecting terminal font but may affect other things. I am currently looking into the cause of this, so hopefully it will be fixed soon

### Future Plans
* Fix bugs (duh)
* More useful output
* Better error checking and handling. Right now, there is very little of this.
* Support for commonly used applications (dmenu, rofi...)
