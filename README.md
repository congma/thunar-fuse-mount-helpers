# Thunar User-Custom Action Scripts for <abbr title="Filesystem in Userspace">FUSE</abbr> Mounting #

## OVERVIEW  ##

This directory contains some user-custom action (UCA) scripts for the [Thunar
file manager][thunar].  The scripts make it easier to work with ISO-9660 disk
images.

After installing the scripts, two <abbr="User-Custom Action">UCA</abbr>s will
be added: "Mount ISO Image with FUSE" and "FUSE Unmount".  The former will
appear when right-clicking on a file with `.ISO` extension;  the latter will
appear when right-clicking on a directory.

## INSTALLATION ##

1.  Copy the files `fuse-mount-iso` and `fuse-umount` to a directory
preferably *NOT* in your `$PATH`.  These executable scripts are meant to
work as Thunar UCA rather than stand-alone apps.

2.  Locate the Thunar UCA config file (usually `$HOME/.config/Thunar/uca.xml`)
Then merge the XML files in this directory into that config file.  You need
to substitute the text `$UCA_PATH` in those files by the actual path to the
scripts.

3.  Start Thunar.  You probably need to restart any existing session by
`Thunar -q && Thunar`.

## BUGS ##

*  Installation is manual and cumbersome.
*  Icons are probably too XFCE4- or Fedora-specific.
*  Not smart enough about when these UCA menu-items should show up.  This is
probably a limitation of Thunar.

## PREREQUISITES ##

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
[zenity]: https://wiki.gnome.org/Projects/Zenity "Zenity"
