# realvnc-server-aarch64-archlinuxarm

Real VNC Server for Raspberry Pi4 64bit for vanilla Arch Linux AARCH64

This AUR package will install Realvnc Server aarch64 package on a vanilla install of ArchLinux ARM64 installation on a Raspberry Pi4.

This is been tested on many desktop environments including XFCE, MATE & KDE Plasma, LXQT to name a few.

BEFORE YOU INSTALL THIS PACKAGE:

Make sure you have the package base-devel installed fully. For example, a default install of Manjaro Arch ARM64 only has some components of base-devel installed by default on a fresh installation so please perform the following command to ensure all prerequists for building the package are met: pacman -S base-devel

Installation:

git clone this package to compile manually:

git clone https://github.com/azalinux/realvnc-server-aarch64-archlinuxarm.git

makepkg -si

FYI: This should be pre-activated as the source is pre-activated for use with Raspberry Pi's however if it doesn't show a valid license after installation, you will need a vaild realvnc key; to activate run: sudo /usr/bin/vnclicense -add

Don't forget to enable the systemd service: sudo systemctl enable vncserver-x11-serviced.service

And thats it! A working 64bit Real VNC server running on ArchLinux ARM64!
