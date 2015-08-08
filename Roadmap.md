**Roadmap is being moved to [xPUD Roadmap on Google Wave](https://wave.google.com/wave/waveref/googlewave.com/w+5x2tvYO6A). Check it out for latest version**

# Introduction #
**This list is intended for developers only. This is an effort to coordinate the steps needed to be taken in order to release the next stable version of xPUD. Users should post suggestions to [Google Groups](http://groups.google.com/group/pud-linux) and issues to [Google Code issue tracker](http://code.google.com/p/xpud/issues/list).**

_Dear developers, if you are planing to work or already working on some feature - please add your name to it in **bold**._<strike>Strikeout</strike> completed tasks. Do not remove rejected tasks, <strike>strikeout</strike> them and add a comment why it was rejected.

# xPUD Development Roadmap #

## 0.9.3 ##
  * <strike>main menu scrolling (paging) when application icons won't fit on screen</strike>
  * <strike>save settings (video mode, keymap, language) to backup and set them after loading backup after boot</strike>
  * <strike>unified Plate UI settings system accessible by Plate and by scripts (currently using prefs.js, do we need better solution (JSON based conf file) or could we just improve the current one?)</strike> We are keeping config files in text format in ~/.config/plate directory.
  * fix shutdown scripts (stop daemons, hide unwanted warnings...)
  * rewrite update-menus script in Perl (speed improvements)
  * improve keymap setting interface in Plate UI settings (add layout variant selection)
  * keep translations in one file per language (easier to maintain)
  * <strike>create opt packages using mkxpud script</strike>

## 0.9.4 ##
  * connect connman with Plate through DBus Bridge, rewrite connection interface (blocked by connman udhcpc bug and DBus bridge issues)
  * indicate opt-get installation (e.g. show spinner animation while opt is being mounted)
  * <strike>disable install button for installed opt packages</strike>
  * automatically login as a non-root user
  * <strike>move home folder to e.g. /home/xpud (moved ~/ to /root)</strike>
  * <strike>set locale information (LC_ALL)</strike>
  * <strike>set keymaps using setxkbmap (check Xvesa support)</strike>
  * pressing poweroff button should show shutdown dialog (use dbus bridge?)
  * multimedia keys support for most popular netbooks (sleep, volume, battery, wifi toggle)
  * improvements to get\_video script (multiscreen support, on/off, rotation detection, saving settings to config to be loaded on startup (Xvesa))
  * alternative tasklist - application switcher (at least alt+tab between applications)

## 0.9.x ##
  * first boot setup wizard (show detected hardware and offer to download kernel modules for unrecognized devices, setup initial settings - language, keymap, backup directory/device, etc.)
  * <strike>add alternative KDrive X servers (i810, nvidia, etc.)</strike> (obsolete: xPUD is using Xorg now)
  * <strike>Xvesa touchscreen calibration (libts, libts-bin, ts_calibrate || XCalibrate ?)</strike> (obsolete: xPUD is using Xorg now)
  * <strike>add virtual keyboard (xvkbd or matchbox-keyboard)</strike>
  * more ACPI events support for netbooks - sleep, lid close detect, wifi on/off etc.
  * improve time/date settings - timezone, am/pm, synchronization
  * custom local file manager (like KFM or ajaXplorer)
  * opt packages with application translations
  * bash script for normal HDD installation to a separate partition
  * improve sound settings - simplify, put playback and recording controls on different tabs
  * easy way to unmount plugged in devices (e.g. right click on an icon and choose eject)
  * show mounted devices in PCManFM sidebar
  * energy savings and automatic fan speed (e.g. acerfand script for Aspire One)

## 1.0 ##
  * make all text strings in Plate localizeable
  * move all CSS style from templates to .css file, allowing Plate UI themes
  * improved boot menu (use gfx-boot) - fewer startup options, settings available from context menus. Boot options: Cloud (core with browser and flash), Multimedia (core, video player, codecs), Kiosk (address set from context menus), CLI (core, nox), Continue from Last Time (if backup exists).
  * user manual - quick overview of available functionality and settings (post on website)

## post 1.0 ##
  * fully modulized system - core, xvesa/xorg, plate/classic, apps, flash, etc. as separate images, user can mix and match available opt images to easily create their own system