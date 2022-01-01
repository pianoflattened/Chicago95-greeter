# Chicago95-greeter
heavily modified version of [grassmunk's Chicago95 lightdm greeter](https://github.com/grassmunk/Chicago95/tree/master/Lightdm/Chicago95) (which in turn is based on kalmanolah's [paddy greeter](https://github.com/kalmanolah/paddy-greeter/) lol) made explicitly for use with [Chicago95](https://github.com/grassmunk/Chicago95/). very limited functionality-wise it just looks cool

### using
-------------
just reading off grassmunk's readme [here](https://github.com/grassmunk/Chicago95/tree/master/Lightdm/Chicago95)

install lightdm and lightdm-webkit-greeter with whatever package manager you have. on arch this looks something like `pacman -S lightdm lightdm-webkit-greeter` and on ubuntu it's `apt-get install lightdm lightdm-webkit-greeter`

configure lightdm to use lightdm-webkit-greeter by opening up `/etc/lightdm/lightdm.conf` and adding the following to the end of the file:

```
[SeatDefaults]
greeter-session=lightdm-webkit-greeter
user-session=xfce
```

then you have to configure lightdm-webkit-greeter to use Chicago95 by editing `/etc/lightdm/lightdm-webkit-greeter.conf` and setting `webkit-theme` to `Chicago95`:

```
# background = Background file to use, either an image path or a color (e.g. #772953)
# theme-name = GTK+ theme to use
# font-name = Font to use
# xft-antialias = Whether to antialias Xft fonts (true or false)
# xft-dpi = Resolution for Xft in dots per inch (e.g. 96)
# xft-hintstyle = What degree of hinting to use (hintnone, hintslight, hintmedium, or hintfull)
# xft-rgba = Type of subpixel antialiasing (none, rgb, bgr, vrgb or vbgr)
#
[greeter]
webkit-theme=Chicago95
```

then just copy the contents of this repo into `/usr/share/lightdm-webkit/themes`