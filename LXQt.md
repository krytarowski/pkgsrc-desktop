## LXQt 0.9.0 import proposal

I'm working on LXQt import to pkgsrc.

> LXQt is the Qt port and the upcoming version of LXDE, the Lightweight Desktop Environment. It is the product of the merge between the LXDE-Qt and the Razor-qt projects: A lightweight, modular, blazing-fast and user-friendly desktop environment.
>
> LXQt 0.9.0 is a fast and stable desktop environment already usable on production systems.
It will not get in your way. It will not hang or slow down your system. It is focused on being a Classic Desktop with a modern Look & Feel.

[-- LXQT About](http://lxqt.org/about/)

#### LXQT packages to be added

No | package in wip | proposed destination | packaged version | upstream version | notes | ready?
---|----------------|----------------------|------------------|------------------|-------|--------
1 | wip/liblxqt | x11/liblxqt | 0.9.0 | 0.9.0 | 1 |
2 | wip/liblxqt-mount | | 0.9.0 | 0.9.0 | |
3 | wip/lximage-qt | graphics/lximage-qt | 0.4.0 | 0.4.0 | |
4 | wip/lxmenu-data | | 0.1.4 | 0.1.4 | |
5 | wip/lxqt-about | | 0.9.0 | 0.9.0 | |
6 | wip/lxqt-admin | | 0.9.0 | 0.9.0 | |
7 | wip/lxqt-common | | 0.9.1 | 0.9.1 | |
8 | wip/lxqt-config | | 0.9.0 | 0.9.0 | |
9 | wip/lxqt-globalkeys | | 0.9.0 | 0.9.0 | |
10 | wip/lxqt-notificationd | | 0.9.0 | 0.9.0 | |
11 | wip/lxqt-openssh-askpass | | 0.9.0 | 0.9.0 | |
12 | wip/lxqt-panel | | 0.9.0 | 0.9.0 | 6 |
13 | wip/lxqt-policykit | | 0.9.0 | 0.9.0 | |
14 | wip/lxqt-powermanagement | | 0.9.0 | 0.9.0 | |
15 | wip/lxqt-qtplugin | | 0.9.0 | 0.9.0 | |
16 | wip/lxqt-runner | | 0.9.0 | 0.9.0 | |
17 | wip/lxqt-session | | 0.9.0 | 0.9.0 | |
18 | wip/pcmanfm-qt | | 0.9.0 | 0.9.0 | |
19 | wip/obconf-qt | | 0.1.0 | 0.1.0 | 3,4 |
20 | wip/libfm | | 1.2.3 | 1.2.3 | 2 |
21 | wip/kwindowsystem | | 5.9.0 | 5.10.0 | |
22 | wip/liboobs | sysutils/liboobs | 2.32.0 | 2.32.0 | 7,9 |
23 | wip/libsystat | | 0.3.0 | 0.3.0 | |
24 | wip/kguiaddons | | 5.9.0 | 5.10.0 | |
25 | wip/polkit | | 0.112 | 0.112 | 5 |
26 | wip/polkit-qt5 | | 0.112 | 0.112 | |
27 | wip/lxqt | meta/lxqt | 0.9.0 | 0.9.0 | |
28 | wip/system-tools-backends | sysutils/system-tools-backends | 2.10.2 | 2.10.2 | 8 |


####Notes

1. ``-fPIE`` added by ``${PREFIX}/qt5/lib/cmake/Qt5Core/Qt5CoreConfigExtras.cmake`` for some reason when building this shared library (it does not happen to the other shared libraries built cmake and qt5) XXX Should be fixed in recent qt5-qtbase https://mail-index.netbsd.org/pkgsrc-changes/2015/05/18/msg124684.html
2. Build wrappers misguided by a symlink https://mail-index.netbsd.org/tech-pkg/2015/05/20/msg014845.html a hack has been applied
3. Required fix in wm/openbox https://mail-index.netbsd.org/pkgsrc-bugs/2015/05/23/msg056868.html
4. Cherry-picked upstream patch for the Qt5 compatibility https://github.com/lxde/obconf-qt/commit/49a4067c58711130848cf4a30a0c4eedead405ac
5. Incompatible with lang/spidermonkey, compatible with older wip/spidermonkey185 -- try to make it work with newer version from pkgsrc to prevent from spidermonkey zoo.
6. At the moment it should be supported only on Linux, FreeBSD and NetBSD  https://github.com/lxde/lxqt-panel/commit/547d52452981658ea217aad5680d9d81a42919e7
7. Required also by the MATE desktop
8. Already exists in pkgsrc with version ``2.6.1nb11`` - need to check whether we can upgrade or need two packages
9. Older version in pkgsrc ``2.22.2nb7`` need to check whether we can upgrade; the older version is reused by Gnome2

####Unordered notes

* NetBSD ships with broken xcb, it was fixed in recent -current https://mail-index.netbsd.org/source-changes/2015/05/04/msg065642.html ; -7 is still affected

####What is done

* 2015-04-11 NetBSD compatibility patch (to reuse our OSS (Linux) audio emulator) has been merged in ``lxqt-panel`` https://github.com/lxde/lxqt-panel/commit/547d52452981658ea217aad5680d9d81a42919e7
* 2015-05-26 committed 'Drops hardcoded /etc/xdg paths' https://github.com/lxde/lxqt-common/commit/ee3e66d75b82dc069992c28bfe0bcc0de6e0be37, reported in "lxqt-common hard-codes /etc/xdg/autostart #651 " https://github.com/lxde/lxqt/issues/651
* 2015-05-27 openbox patch needed for ``obconf-qt`` (pango dependency missed in the bl3) has been merged https://mail-index.netbsd.org/pkgsrc-changes/2015/05/27/msg124957.html
* 2015-05-27 qt5 sysconfdir has been set correctly, it fixes issue with inappropriate value of ``qmake -query QT_INSTALL_CONFIGURATION`` used by ``liblxqt`` https://mail-index.netbsd.org/pkgsrc-changes/2015/05/27/msg124962.html
* 2015-05-27 committed 'Removes unused FindInstallConfigPath.cmake (LXQT_ETC_XDG_DIR is set in liblxqt.)' https://github.com/lxde/lxqt-globalkeys/commit/94cbfd9afb5906d2576534d2313c4836d7645e57, reported in "lxqt-common hard-codes /etc/xdg/autostart #651 " https://github.com/lxde/lxqt/issues/651
* 2015-05-28 committed 'Sets env variable XDG_CONFIG_DIRS' https://github.com/lxde/lxqt-common/commit/3b56bf2acb595a8a6776a00858cb9bf9069fab90, reported in "lxqt-common hard-codes /etc/xdg/autostart #651 " https://github.com/lxde/lxqt/issues/651

####Screenshots

![1](http://susepaste.org/images/26026226.png)

####How to use

You need ``NetBSD-current``, ``pkgsrc-current`` and ``pkgsrc-wip``.

Add to your ``.xinitrc`` the following line:

```
startlxqt
```

and use ``startx``.

####Platform support

platform | status
---------|-------
NetBSD/amd64 current | works
DragonflyBSD | unknown
FreeBSD | unknown
OpenBSD | unknown
Linux x86_64 CentOS-7 | qt5 build issues
MacOSX | pointed out that MacOS requires special qt5 version

####Links
- [LXQt website](http://lxqt.org)
- [Build LXDE-Qt From Source](http://wiki.lxde.org/en/Build_LXDE-Qt_From_Source)
- [Mageia LXQt meta package](https://svnweb.mageia.org/packages/cauldron/task-lxqt/current/SPECS/task-lxqt.spec?view=markup)
- [LXQt 0.7 got initial FreeBSD support](http://blog.lxde.org/?p=1111)
- [ArchLinux wiki notes on LXQT](https://wiki.archlinux.org/index.php/LXQt)
