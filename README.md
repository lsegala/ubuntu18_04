# MacBuntu

Link: https://www.noobslab.com/2018/08/macbuntu-1804-transformation-pack-ready.html
Youtube: https://www.youtube.com/watch?v=AHzGYG2XvMI

## Script

```
$ sudo add-apt-repository ppa:noobslab/macbuntu
$ sudo apt-get update
$ sudo apt-get install slingscold
$ sudo apt-get install albert
$ sudo apt-get install plank
$ sudo apt-get install macbuntu-os-icons-v1804
$ sudo apt-get install macbuntu-os-ithemes-v1804
$ sudo apt-get install macbuntu-os-plank-theme-v1804
$ sudo apt-get install gnome-tweak-tool
$ wget -O mac-fonts.zip http://drive.noobslab.com/data/Mac/macfonts.zip
$ sudo unzip mac-fonts.zip -d /usr/share/fonts; rm mac-fonts.zip
$ sudo fc-cache -f -v
```

## Plank Config

```
$ sudo killall plank
$ cd ~/.config/plank/dock1/launchers
$ echo [PlankDockItemPreferences]\
$ file:///usr/share/applications/slingscold.desktop > slingscold.dockitem
$ plank
```

# Touchpad

## Script

```
$ sudo apt update && sudo apt upgrade
$ sudo apt install build-essential git pkg-config libmtdev-dev mtdev-tools xserver-xorg-dev xutils-dev
$ sudo apt-get install libinput-tools
$ git clone https://github.com/bulletmark/libinput-gestures.git
$ cd libinput-gestures/
$ sudo make install
$ sudo gpasswd -a $USER input
$ sudo apt install xdotool wmctrl libinput-tools
```

## Config

```
echo gesture swipe up 3	xdotool key super\
gesture swipe down 3	xdotool key super\
gesture swipe left 3	xdotool key ctrl+alt+Up\
gesture swipe right 3	xdotool key ctrl+alt+Down > ~/.config/libinput-gestures.conf
libinput-gestures-setup autostart
```

# Keyboard

/etc/default/keyboard
```
XKBLAYOUT=us
BACKSPACE=guess
XKBVARIANT=altgr-intl
```
