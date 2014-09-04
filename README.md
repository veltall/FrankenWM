FrankenWM
=========

*"monsterwm's bastard child"* or *"not the wm your desktop needs, but the one
it deserves"*

FrankenWM is a dynamic tiling WM (comparable to dwm or Awesome), featuring the
v-stack, b-stack, grid, fibonacci, dualstack, equal and monocle layouts out of
the box. If you want to, you can add gaps between the windows as well.

It was once based on monsterwm but has undergone many greater changes including
adding pieces from other WMs (hence the name) and porting all sorts of stuff
from Xlib to XCB. Many of the original monsterwm patches have been ported as
well.

Installation
------------

First clone this repository to your local machine

    $ git clone https://github.com/sulami/FrankenWM.git

You need xcb and xcb-utils so refer to your distro wiki
to install them. For instance, he packages in Arch Linux 
needed for example would be `libxcb` `xcb-util` `xcb-util-wm`, 
and `xcb-util-keysyms`

Then, copy `config.def.h` as `config.h` 

    $ cd /path/to/FrankenWM
    $ cp config.def.h config.h

and edit to suit your needs.  Build and install.

    $ $EDITOR config.h
    $ make
    $ sudo make clean install



Configuration
-------------

FrankenWM does not support dynamic configuration (re-)loading.
Configuration is done by editing `config.h` before (re-)compiling FrankenWM with 
`sudo make && sudo make clean install`.
If you want an advanced configuration example, you can have a look at [my personal config][config].

  [config]: https://github.com/sulami/dotfiles/blob/master/frankenwm.config.h
  
For a list of keynames available for binding, refer to your X config file:

    $ $EDITOR /usr/include/X11/keysymdef.h
  
Status Bar
----------

FrankenWM does not feature a status bar. Like MonsterWM, it leaves a preconfigured
amount of space for one. Refer to the [monsterwm docs][mwmdocs] for examples 
on how to parse the output to use it in a status bar of choice.

  [mwmdocs]: https://github.com/c00kiemon5ter/monsterwm#panel---statusbar
  
Also refer to the ArchWiki's article on [Bar-aint-recursive][arch-bar] for a
beginner-friendly introduction to configuring stdout status bars.

  [arch-bar]: https://wiki.archlinux.org/index.php/Bar-aint-recursive
  
Usage
-----

I took the time to write a really nice and pretty manpage (`man frankenwm`, or
man ./[frankenwm.1][man] if you want to read it before installing) covering the
tiling modes and all of the default shortcuts.

  [man]: https://github.com/sulami/frankenwm/blob/master/frankenwm.1

Bugs
----

Bugs can be reported here: [FrankenWM issues][bug]

   [bug]: https://github.com/sulami/FrankenWM/issues

Thanks
------

Parts of FrankenWM come from:

 * [c00kiemonster's][cookiemonster] [monsterwm][monsterwm]
 * [cloudef's][cloudef] [monsterwm-xcb][monsterwm-xcb]
 * [venam's][venam] [2bwm][twobwm]


Inspiration from:

 * [suckless'][suckless] [dwm][dwm]
 * [baskerville's][baskerville] [bspwm][bspwm]


  [cookiemonster]: https://github.com/c00kiemon5ter
  [monsterwm]: https://github.com/c00kiemon5ter/monsterwm
  [cloudef]: https://github.com/cloudef
  [monsterwm-xcb]: https://github.com/cloudef/monsterwm-xcb
  [venam]: https://github.com/venam
  [twobwm]: https://github.com/venam/2bwm

  [suckless]: http://suckless.org/
  [dwm]:  http://dwm.suckless.org/
  [baskerville]: https://github.com/baskerville
  [bspwm]: https://github.com/baskerville/bspwm

