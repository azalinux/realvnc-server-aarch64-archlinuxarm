# realvnc-server-aarch64-archlinuxarm64

RealVNC Server for Raspberry Pi4 64bit for vanilla Arch Linux ARM AARCH64

This AUR package will install RealVNC Server aarch64 package on a vanilla install of ArchLinux ARM64 installation on a Raspberry Pi4.

This is been tested on many desktop environments including XFCE, MATE & KDE Plasma, LXQT to name a few.

BEFORE YOU INSTALL THIS PACKAGE:

Make sure you have the package base-devel installed fully. For example, a default install of Arch Linux ARM64 only has some components of base-devel installed by default on a fresh installation so please perform the following command to ensure all prerequists for building the package are met:   
```
$ sudo pacman -S base-devel
```
Installation:

You can use the precompiled package in my Releases page to download & install:

```
$ wget https://github.com/azalinux/realvnc-server-aarch64-archlinuxarm/releases/download/realvnc-server-aarch64-v6.10.1/realvnc-vnc-server-6.10.1-1-aarch64.pkg.tar.xz
$ sudo pacman -U realvnc-vnc-server-6.10.1-1-aarch64.pkg.tar.xz
```

OR to git clone this package to compile manually:

```
$ git clone https://github.com/azalinux/realvnc-server-aarch64-archlinuxarm.git
$ makepkg -si
```

FYI: This should be pre-activated as the source is pre-activated for use with Raspberry Pi's however if it doesn't show a valid license after installation, you will need a vaild realvnc key; to activate run: 
```
$ sudo /usr/bin/vnclicense -add
````
Don't forget to enable & start the systemd service: 
```
$ sudo systemctl enable vncserver-x11-serviced
$ sudo systemctl start vncserver-x11-serviced
```
And thats it! A working 64bit RealVNC server running on ArchLinux ARM64!

**Please note - This free Raspberry Pi edition of RealVnc Server will let clients connect via TCP direct mode rather than UDP direct mode. You need an Enterprise License to connect via UDP!**
