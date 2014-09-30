# Thunar User-Custom Action Scripts for <abbr title="Filesystem in Userspace">FUSE</abbr> Mounting #

## OVERVIEW  ##

This directory contains some user-custom action (UCA) scripts for the [Thunar
file manager][thunar].  The scripts make it easier to work with <abbr
title="Filesystem in Userspace">FUSE</abbr>.

## INSTALLATION ##

1.  Copy the shell scripts to a directory preferably *NOT* in your `$PATH`.
These executable scripts are meant to work as Thunar UCA rather than
stand-alone apps.

2.  Locate the Thunar UCA config file (usually `$HOME/.config/Thunar/uca.xml`)
Then merge the XML files in this directory into that config file.  You need to
substitute the text `$UCA_PATH` in those files by the actual path to the
scripts.

3.  Start Thunar.  You probably need to restart any existing session by `Thunar
-q && Thunar`.

## HELPER SCRIPTS ##

### `fuse-mount-iso` ###

This script mounts an ISO 9660 disk image to the mount point selected in the
dialog box.  Default mount point: `$HOME/media`.

#### Script Prerequisites ####

*  The [FuseISO][fuseiso] package.

### `fuse-mount-zip ###

Similar to [`fuse-mount-iso`](#fuse-mount-iso), but for Zip archives.  The
mounted filesystem will be writeable.

#### Script Prerequisites ####

*  The [fuse-zip][fusezip] package.

### `fuse-umount` ###

This script unmounts a FUSE mount point.

## BUGS ##

*  Installation is manual and cumbersome.
*  Icons are probably too XFCE4- or Fedora-specific.
*  Not smart enough about when these UCA menu-items should show up.  This is
probably a limitation of Thunar.

## PREREQUISITES ##

All scripts require the following packages:

*  Thunar file manager.  Custom actions are enabled by the [`thunar-uca`][uca]
plugin.
*  [FUSE][fuse] and [FuseISO][fuseiso].
*  [Zenity][zenity] for GUI dialog boxes.

## COPYRIGHT ##

Public domain.


[thunar]: http://docs.xfce.org/xfce/thunar/start "Thunar File Manager"
[uca]: http://docs.xfce.org/xfce/thunar/custom-actions "Custom Actions"
[fuse]: http://fuse.sourceforge.net/ "FUSE: Filesystem in Userspace"
[fuseiso]: http://sourceforge.net/projects/fuseiso/ "FuseISO"
[fusezip]: https://code.google.com/p/fuse-zip/ "fuse-zip"
[zenity]: https://wiki.gnome.org/Projects/Zenity "Zenity"
