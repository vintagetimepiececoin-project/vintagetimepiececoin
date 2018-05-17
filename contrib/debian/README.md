
Debian
====================
This directory contains files used to package bitcoind/bitcoin-qt
for Debian-based Linux systems. If you compile bitcoind/bitcoin-qt yourself, there are some useful files here.

To add URI support and clickable links (vintagetimepiececoin:<VintageTimePieceCoin addres>) for the VintageTimePieceCoin Core QT wallet

This can be installed for either all users or the current user

### All users

#### Install desktop shortcut
    cd vintagetimepiececoin
    sudo desktop-file-validate ./contrib/debian/vintagetimepiececoin-qt.desktop # See Note
    sudo cp ./contrib/debian/vintagetimepiececoin-qt.desktop /usr/share/applications/
    sudo update-desktop-database

#### Install icon graphics
    sudo cp share/pixmaps/bitcoincoin128.png /usr/share/pixmaps/

### Current user

#### Install desktop shortcut
    cd vintagetimepiececoin
    sudo desktop-file-validate ./contrib/debian/vintagetimepiececoin-qt.desktop # Check paths in vintagetimepiececoin-qt.desktop match the installation path usually /usr/local/bin
    sudo cp ./contrib/debian/vintagetimepiececoin-qt.desktop ~/.local/share/applications/
    sudo update-desktop-database

#### Install icon graphics
    sudo cp share/pixmaps/bitcoin128.png /usr/share/pixmaps/


**Note:** If you build yourself, you will either need to modify the paths in
the .desktop file or copy vintagetimepiececoin-qt or symlink your vintagetimepiececoin-qt binary to `/usr/local/bin`
and copy the `../../share/pixmaps/bitcoin128.png` to `/usr/share/pixmaps`


KDE
====================
bitcoin-qt.protocol (KDE)