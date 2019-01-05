# Awesome Ubuntu

- [13 Keyboard Shortcut Every Ubuntu 18.04 User Should Know](https://itsfoss.com/ubuntu-shortcuts/)
- [50 Best Ubuntu Apps You Should Be Using Right Now](https://itsfoss.com/best-ubuntu-apps/)

## Apps

- [GNOME Tweaks](https://linuxconfig.org/how-to-install-tweak-tool-on-ubuntu-18-04-bionic-beaver-linux)
- [Guake Terminal](http://guake-project.org)
- [Stacer](https://oguzhaninan.github.io/Stacer-Web/) - Linux System Optimizer & Monitoring.
- [WPS Office](https://www.wps.com/office/linux)
  - [WPS Office Fonts](https://github.com/IamDH4/ttf-wps-fonts)
  
```sh
sudo apt install -y curl gparted git vim
```

## GNOME Shell Extensions

- [Applications Overview Tooltip](https://extensions.gnome.org/extension/1071/applications-overview-tooltip/) - Shows a tooltip over applications icons on applications overview.
- [Caffeine](https://extensions.gnome.org/extension/517/caffeine/) - Disable the screensaver and auto suspend.
- [Clipboard Indicator](https://extensions.gnome.org/extension/779/clipboard-indicator/) - Adds a clipboard indicator to the top panel, and caches clipboard history.
- [CPU Power Manager](https://extensions.gnome.org/extension/945/cpu-power-manager/) - Manage Intel_pstate CPU Frequency scaling driver.
- [EasyScreenCast](https://extensions.gnome.org/extension/690/easyscreencast/) - This extension simplifies the use of the video recording function.
- [Gno-Menu](https://extensions.gnome.org/extension/608/gnomenu/) - Gno-Menu is a traditional styled full featured Gnome-Shell apps menu.
- [GSConnect](https://extensions.gnome.org/extension/1319/gsconnect/) - GSConnect is a complete implementation of KDE Connect especially for GNOME Shell with Nautilus.
- [Internet Radio](https://extensions.gnome.org/extension/836/internet-radio/) - Listen to an Internet Radio Stream.
- [OpenWeather](https://extensions.gnome.org/extension/750/openweather/) - Weather extension.
- [Places Status Indicator](https://extensions.gnome.org/extension/8/places-status-indicator/) - Add a menu for quickly navigating places in the system.
- [Remove Dropdown Arrows](https://extensions.gnome.org/extension/800/remove-dropdown-arrows/) - Removes the dropdown arrows.
- [Removable Drive Menu](https://extensions.gnome.org/extension/7/removable-drive-menu/) - A status menu for accessing and unmounting removable devices.
- [Screenshot Tool](https://extensions.gnome.org/extension/1112/screenshot-tool/) - Conveniently create, copy, store and upload screenshots.
- [Status Area Horizontal Spacing](https://extensions.gnome.org/extension/355/status-area-horizontal-spacing/) - Reduce the horizontal spacing between icons in the top-right status area.
- [System Monitor](https://extensions.gnome.org/extension/120/system-monitor/) - Display system informations in gnome shell status bar.
- [Todo.txt](https://extensions.gnome.org/extension/570/todotxt/) - A Gnome shell interface for todo.txt.
- [VirtualBox applet](https://extensions.gnome.org/extension/1415/virtualbox-applet/) - Provide menu to run VirtualBox machines and switch between running VMs.
- [Workspaces to Dock](https://extensions.gnome.org/extension/427/workspaces-to-dock/) - Transform Gnome Shell's overview workspaces into an intelligent dock.

## zRAM

- https://en.wikipedia.org/wiki/Zram
- https://askubuntu.com/questions/1044976/make-zram-use-lz4-compression-algorithm
- https://lwn.net/Articles/748681/

```sh
sudo apt install -y zram-config
```

Set `lz4` and `swapon -p 100`.
```sh
sudo vi /usr/bin/init-zram-swapping

echo lz4 > /sys/block/zram${DEVNUMBER}/comp_algorithm
echo $mem > /sys/block/zram${DEVNUMBER}/disksize
mkswap /dev/zram${DEVNUMBER}
swapon -p 100 /dev/zram${DEVNUMBER}
```

