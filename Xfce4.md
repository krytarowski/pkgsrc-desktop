####packages to be updated

package  | pkgsrc version | upstream version 
---------|----------------|----------------
audio/xfce4-mixer | 4.6.1nb21 | 4.11.0
audio/xfce4-xmms-plugin | 0.5.1 | 0.5.3
devel/xfce4-dev-tools | 4.6.0 | 4.12.0
devel/xfce4-conf | 4.6.1nb22 | 4.12.0
editors/xfce4-mousepad | 0.2.16 | 0.4.0
graphics/ristretto |0.0.22nb27 | 0.8.0
meta-pkgs/xfce4 | 4.6.1nb32 | 4.12.0
meta-pkgs/xfce4-extras | 4.6.1nb31 | 4.12.0
misc/xfce4-weather-plugin | 0.6.2 | 0.8.5
multimedia/xfce4-mpc-plugin| 0.3.2 | 0.4.4
net/xfce4-wavelan-plugin| 0.5.4 | 0.5.11
sysutils/xfce4-appfinder| 4.6.1nb23 | 4.12.0
sysutils/xfce4-battery-plugin| 0.5.11nb23 | 1.0.5
sysutils/xfce4-cpugraph-plugin| 0.3.0 | 1.0.5
sysutils/xfce4-diskperf-plugin| 2.1.0nb21 | 2.5.4
sysutils/xfce4-fsguard-plugin| 0.4.0nb21 | 1.0.1
sysutils/xfce4-genmon-plugin| 3.1nb21 | 3.4
sysutils/xfce4-netload-plugin| 0.4.0nb21 | 1.2.4
sysutils/xfce4-quicklauncher-plugin|1.9.4nb21 | 1.9.4
sysutils/xfce4-systemload-plugin|0.4.2nb21 | 1.1.2
sysutils/xfce4-thunar| 1.0.1nb23 | 1.6.6
sysutils/xfce4-xarchiver| 0.5.2nb22 | 0.5.4
sysutils/xfce4-xkb-plugin| 0.4.3nb21 | 0.7.0
textproc/xfce4-dict-plugin|0.2.1nb21 | 0.3.0
time/xfce4-datetime-plugin| 0.6.1nb20 | 0.6.2
time/xfce4-orage|0.6.1nb23|4.10.0
time/xfce4-timer-plugin|0.5.1nb21|1.6.0
wm/xfce4-wm|4.6.1nb21 | 4.12.2
wm/xfce4-wm-themes|4.6.0 | 4.10.0
x11/libxfce4gui|4.6.1nb21 | 4.10.0
x11/libxfce4util|4.6.1nb17 | 4.12.1
x11/xfce4-clipman-plugin|0.8.0nb21 | 1.2.6
x11/xfce4-desktop|4.6.1nb23 | 4.12.1
x11/xfce4-exo|0.3.101nb26 | 0.10.4
x11/xfce4-eyes-plugin|4.4.0nb21|4.4.3
x11/xfce4-gtk2-engine|2.6.0nb19|3.2.0
x11/xfce4-notes-plugin|1.6.0nb21|1.1.7
x11/xfce4-panel|4.6.2nb22 | 4.12.0
x11/xfce4-places-plugin|1.0.0nb24|1.6.0
x11/xfce4-session|4.6.1nb21|4.12.1
x11/xfce4-settings|4.6.5nb23|4.12.0
x11/xfce4-terminal|0.4.2nb21|0.6.3

##packages to be addded

port|comment|version
----|-----------|--------
x11/libxfce4ui | Xfce widget library | 4.12.1
x11/xfce4-garcon | Xfce menu library | 0.4.0
mail/xfce4-mailwatch-plugin | Xfce mail checker plugin for the panel | 1.2.0
sysutils/xfce4-mount-plugin | Xfce mount/umount utility for the panel | 0.6.7
x11/xfce4-notifyd | Xfce notify daemon | 0.2.4
x11/xfce4-screenshooter | Xfce screenshot application | 1.8.2 
sysutils/xfce4-taskmanager | Xfce task manager | 1.1.0
archivers/xfce4-thunar-archive | Thunar archive plugin | 0.3.1
multimedia/xfce4-thunar-media-tags | Thunar media tags plugin | 0.2.1
sysutils/xfce4-thunar-vcs | Thunar vcs integration plugin | 0.1.4
x11/xfce4-tumbler | D-Bus thumbnailing service | 0.1.31
x11/xfce4-whiskermenu-plugin | Alternate application launcher for Xfce | 1.5.0
sysutils/xfce4-verve-plugin | Xfce command line plugin | 1.0.1

##packages not in meta packages

- xfce4-whiskermenu-plugin : depends on cmake
- xfce4-thunar-vcs : depends on svn|git
- xfce4-dev-tools : users don't need it

####packages to be renamed 


port | new name | reason
-----|----------|-------
devel/xfconf | devel/xfce4-conf | clarity

####packages to be removed 

port | version | reason
-----|---------|--------
print/xfce4-print| 4.6.1nb25 | no longer maintained
x11/libxfce4menu| 4.6.1nb18 | replaced by xfce4-garcon
x11/xfce4-screenshooter-plugin| 1.0.0nb21 | replaced by xfce4-screenshooter
x11/xfce4-utils | 4.6.1nb23 | replaced by xfce4-dev-tools
sysutils/xfce4-volman | 0.2.0bn25 | linux only; needs gudev
multimedia/xfmedia | 0.9.2nb25 | no longer maintained

####supported platforms 

platform | priority | status
---------|----------|-------
NetBSD amd64 current | highest | works
NetBSD i386 current | highest | works
NetBSD evbarm current | highest | works
SmartOS | high | mostly working, needs more testing
FreeBSD | high | keyboard settings not working?
DragonFlyBSD | high | Works, install hal from pkgng.
OS X | mid | works, no session support
OpenBSD | low | untested
Linux | low | untested

####how to test

From source:

- clone [edgebsd-pkgsrc.git](http://git.edgebsd.org/gitweb/?p=edgebsd-pkgsrc.git;a=summary)
- switch to the `yrmt-xfce412-rel` branch
- install meta-pkgs/xfce4 and meta-pkgs/xfce4-extras

From packages:

- Use one of the repos linked below

####todo

- update xfce4-session to 4.12.2 (need NetBSD hibernate command)

- get genmon to work (just crashes at startup)

- submit patches upstream

- more panel plugins: [http://archive.xfce.org/src/panel-plugins/](http://archive.xfce.org/src/panel-plugin)

- more xfce applications: [http://archive.xfce.org/src/apps/](http://archive.xfce.org/src/apps/)

####Links 

- [NetBSD i386 packages by @ebijun](http://ftp.netbsd.org/pub/NetBSD/misc/jun/XFCE4.12/i386-7.99.9/)

- [xfce](http://xfce.org/)

- [a tour of xfce 4.12](http://www.xfce.org/download/changelogs/4.12)

- [xfce wiki](https://wiki.xfce.org/)
