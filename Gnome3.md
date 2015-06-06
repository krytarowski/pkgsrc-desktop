## Gnome 3 import proposal

I'm working on Gnome3 import to pkgsrc.

> GNOME 3 is an easy and elegant way to use your computer. It is designed to put you in control and bring freedom to everybody. GNOME 3 is developed by the GNOME community, a diverse, international group of contributors that is supported by an independent, non-profit foundation.

[-- Gnome About](https://www.gnome.org/)

#### Gnome packages to be added

No | package in wip | proposed destination | wip version | notes | ready?
---|----------------|----------------------|-------------|-------|-------
1 | wip/accountsservice | sysutils/accountsservice | 0.6.40 | 1 |
2 | wip/yelp-tools | misc/yelp-tools | 3.16.1 | |

#### Gnome packages to be removed

No | package in pkgsrc | notes | ready?
---|-------------------|-------|-------
1 | editors/gedit3 | editors/gedit upgraded to 3.x |
2 | x11/vte029 | x11/vte upgraded to the recent version |


#### Gnome packages to be upgraded

No | package in wip | proposed destination | wip version | pkgsrc version | notes | ready?
---|----------------|----------------------|-------------|----------------|-------|-------
1 | wip/gnome | meta-pkgs/gnome | 3.17 | 2.26.2 | |
2 | wip/alacarte | x11/alacarte |  |  | |
3 | wip/bug-buddy | net/bug-buddy |  |  | |
4 | wip/cheese | graphics/cheese |  |  | |
5 | wip/dasher | editors/dasher |  |  | |
6 | wip/desktop-appplet | misc/desktop-applet |  |  | |
7 | wip/ekiga | net/ekiga |  |  | |
8 | wip/empathy | chat/empathy |  |  | |
9 | wip/eog | chat/eom |  |  | |
10 | wip/epiphany | www/epiphany |  | | |
11 | wip/evolution | mail/evolution | | | |
12 | wip/evolution-data-server | mail/evolution-data-server | | | |
13 | wip/evolution-exchange | mail/evolution-exchange | | | |
14 | wip/evolution-mapi | mail/evolution-mapi | | | |
15 | wip/evolution-webcal | mail/evolution-webcal | | | |
16 | wip/file-roller | archivers/file-roller | | | |
17 | wip/gcalculator | math/gcalculator | | | |
18 | wip/gconf-editor | editors/gconf-editor | | | |
19 | wip/gdm | x11/gdm | | | |
20 | wip/gedit | editors/gedit | | | |
21 | wip/gio-fam | sysutils/gio-fam | | | |
22 | wip/gnome-applets | x11/gnome-applets | | | |
23 | wip/gnome-backgrounds | graphics/gnome-backgrounds | | | |
24 | wip/gnome-control-center | x11/gnome-control-center | | | |
25 | wip/gnome-desktop | x11/gnome-desktop | | | |
26 | wip/gnome-desktop-sharp | x11/gnome-desktop-sharp | | | |
27 | wip/gnome-doc-utils | textproc/gnome-doc-utils | | | |
28 | wip/gnome-games | games/gnome-games | | | |
29 | wip/gnome-icon-theme | graphics/gnome-icon-theme | | | |
30 | wip/gnome-keyring | security/gnome-keyring | | | |
31 | wip/gnome-mag | x11/gnome-mag | | | |
32 | wip/gnome-media | multimedia/gnome-media | | | |
33 | wip/gnome-menus | sysutils/gnome-menus | | | |
34 | wip/gnome-netstatus | net/gnome-netstatus | | | |
35 | wip/gnome-nettool | net/gnome-nettool | | | |
36 | wip/gnome-panel | x11/gnome-panel | | | |
37 | wip/gnome-power-manager | sysutils/gnome-power-manager | | | |
38 | wip/gnome-netstatus | x11/gnome-netstatus | | | |
39 | wip/py-gnome2-desktop | x11/py-gnome2-desktop | | | |
40 | wip/gnome-screensaver | x11/gnome-screensaver | | | |
41 | wip/gnome-session | x11/gnome-session | | | |
42 | wip/gnome-settings-daemon | sysutils/gnome-settings-daemon | | | |
43 | wip/gnome-sharp | x11/gnome-sharp | | | |
44 | wip/gnome-speech | audio/gnome-speech | | | |
45 | wip/gnome-system-monitor | sysutils/gnome-system-monitor | | | |
46 | wip/gnome-system-tools | sysutils/gnome-system-tools | | | |
47 | wip/gnome-terminal | x11/gnome-terminal | | | |
48 | wip/gnome-themes | x11/gnome-themes | | | |
49 | wip/gnome-user-docs | misc/gnome-user-docs | | | |
50 | wip/gnome-user-share | misc/gnome-user-share | | | |
51 | wip/gnome-utils | misc/gnome-utils | | | |
52 | wip/gok | misc/gok | | | |
53 | wip/gst-plugins0.10-base | multimedia/gst-plugins0.10-base | | | |
54 | wip/gst-plugins0.10-good | multimedia/gst-plugins0.10-good | | | |
55 | wip/gst-plugins0.10-pulse | audio/gst-plugins0.10-pulse | | | |
56 | wip/gstreamer0.10 | multimedia/gstreamer0.10 | | | |
57 | wip/gtk2-engines | x11/gtk2-engines | | | |
58 | wip/gtkhtml314 | www/gtkhtml314 | | | |
59 | wip/gtksourceview2 | x11/gtksourceview2 | | | |
60 | wip/gucharmap | fonts/gucharmap | | | |
61 | wip/gvfs | sysutils/gvfs | | | |
62 | wip/hamster-applet | x11/hamster-applet | | | |
63 | wip/libgail-gnome | devel/libgail-gnome | | | |
64 | wip/libgnomekbd | x11/libgnomekbd | | | |
65 | wip/libgnomeprint | print/libgnomeprint | | | |
66 | wip/libgnomeprintui | print/libgnomeprintui | | | |
67 | wip/libgtop | sysutils/libgtop | | | |
68 | wip/libgweather | devel/libgweather | | | |
69 | wip/liboobs | sysutils/liboobs | | | |
70 | wip/libsoup24 | net/libsoup24 | | | |
71 | wip/libwnck | devel/libwnck | | | |
72 | wip/metacity | wm/metacity | | | |
73 | wip/mousetweaks | misc/mousetweaks | | | |
74 | wip/nautilus | sysutils/nautilus | | | |
75 | wip/orca | misc/orca | | | |
76 | wip/py-gtksourceview | x11/py-gtksourceview | | | |
77 | wip/mousetweaks | misc/mousetweaks | | | |
78 | wip/seahorse | security/seahorse | | | |
79 | wip/seahorse-plugins | security/seahorse-plugins | | | |
80 | wip/sound-juicer | audio/sound-juicer | | | |
81 | wip/swfdec-gnome | multimedia/swfdec-gnome | | | |
82 | wip/tomboy | editors/tomboy | | | |
83 | wip/totem | multimedia/totem | | | |
84 | wip/totem-pl-parser | multimedia/totem-pl-parser | | | |
85 | wip/vinagre | net/vinagre | | | |
86 | wip/vino | net/vino | | | |
87 | wip/vte | x11/vte | 0.40.2 | 0.28.1nb16 | |
88 | wip/yelp | misc/yelp | | | |
89 | wip/zenity | x11/zenity | 3.16.2 | 2.32.1nb19 | |


####Ordered notes

1. 2015-06-06 WTMPX / NetBSD patch sent upstream https://bugs.freedesktop.org/show_bug.cgi?id=90882

####Unordered notes

* TODO: Githubify packages https://github.com/GNOME Reported issues with missing tags on the mirror | Update (2015-06-06) GitHub shows all tags on the release page and hides them in the scroll popup menu
* SystemBSD

> 13:06 < ajacoutot> no; systembsd is not going anywhere currently    
> 13:07 < ajacoutot> I'd rather look into loginkit and consolekit2     
> 13:07 < ajacoutot> the other stuff systembsd "would" provide is not mandatory (just nice to have, that's all)     


####What is done

* 2015-06-05 vala unversioned files are shipped again with ``lang/vala``, these files are required to bootstrap packages with ``./autogen.sh`` https://mail-index.netbsd.org/pkgsrc-changes/2015/06/05/msg125392.html

####Screenshots

####How to use

####Platform support

####Links
- [Gnome website](https://www.gnome.org)
- [Gnome and Debian](https://wiki.debian.org/Gnome)
- [Mageia Gnome meta package](https://svnweb.mageia.org/packages/cauldron/task-gnome/current/SPECS/task-gnome.spec?view=markup)
- [ArchLinux wiki notes on Gnome](https://wiki.archlinux.org/index.php/Gnome)
