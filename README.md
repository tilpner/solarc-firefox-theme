# SolArc Firefox Theme
Based on the awesome [Arc](https://github.com/horst3180/arc-firefox-theme) Firefox theme.

## Requirements
This theme is compatible with Firefox 40+ and Firefox 38 ESR

**Note**: This theme is meant to be used in conjunction with the [SolArc GTK theme](https://github.com/apheleia/solarc-theme), don't use it with other GTK themes or it will look broken.

### Manual building and installation
These instructions are for testers and package maintainers. They also allow to install the theme globally for all users.

You will need `autoconf` and `automake` for the following.

Clone the repository

    git clone https://github.com/horst3180/arc-firefox-theme && cd arc-firefox-theme

Generate the .xpi files (drag and drop these into your Firefox window)

    ./autogen.sh --prefix=/usr
    make mkxpi

Alternatively the theme can be installed globally without using the .xpi files

    ./autogen.sh --prefix=/usr
    sudo make install

Other build options to append to `autogen.sh` are

    --disable-light         disable Arc Light Firefox support
    --disable-darker        disable Arc Darker Firefox support
    --disable-dark          disable Arc Dark Firefox support

Uninstall the theme with

    sudo make uninstall

### Firefox ESR (Debian Stable users see here)
This repo includes separate Firefox ESR compatible branches. The installation process is mostly identical to the manual installation above

    git clone https://github.com/horst3180/arc-firefox-theme && cd arc-firefox-theme
    git checkout firefox-38-esr   # Execute this for Firefox 38 ESR
    git checkout firefox-45-esr   # Execute this for Firefox 45 ESR
    git checkout firefox-52-esr   # Execute this for Firefox 52 ESR
    ./autogen.sh --prefix=/usr
    make mkxpi
