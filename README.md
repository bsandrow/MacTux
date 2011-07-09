MacTux
======

A boot splash for Plymouth (the boot splash program used by Ubuntu, Fedora,
etc) that mimics the Mac boot screen with the Apple logo in the middle (except
in this case it's Tux, the Linux logo). I got the idea from rEFIt, which shows
the same thing when you choose Linux from the boot menu.

Install
-------

On Ubuntu:

    # -- Install the theme
    $ sudo cp -r MacTux /lib/plymouth/themes

    # -- Register it as a possible value for default.plymouth
    $ sudo update-alternatives --install \
        /lib/plymouth/themes/default.plymouth default.plymouth \
        /lib/plymouth/themes/MacTux/MacTux.plymouth 100

    # -- Select it as the default theme
    $ sudo update-alternatives --config default.plymouth

    # -- Update boot image
    $ sudo update-initramfs -u

Roadmap
-------
 - Create a version where the boot splash is the background to scrolling boot
   message text.

Author
------

Brandon Sandrowicz <brandon@sandrowicz.org>
