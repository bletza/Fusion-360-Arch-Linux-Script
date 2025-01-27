# Install Fusion 360 on Arch Linux

# IMPORTANT

The script was modified to support multiple program installs and the project was moved to [wiener](https://github.com/kndndrj/wiener).
To install Fusion 360, go to the mentioned repository and follow the instructions there!
The specific install command is the following:
```sh
./wiener.sh fusion360 install
```

# DEPRECATED

A script for installing Fusion 360 on Arch Linux through WINE.

The script automatically downloads and installs the program on your system and
it also installs any prerequisites first, so you don't have to worry about
them.

## Requirements
Before installing, please make sure to have the appropriate graphics drivers
installed. Reffer to
[Lutris](https://github.com/lutris/docs/blob/master/InstallingDrivers.md#arch--manjaro--other-arch-derivatives)
and [Arch](https://wiki.archlinux.org/title/Xorg#Driver_installation) wikis.

## Download
To download the script, open a new terminal window, navigate to a folder in
which you want to save the script (e.g. `cd ~/Downloads`) and copy the
following code snippet to the terminal:
```sh
curl -Lo fusion360_install.sh https://raw.githubusercontent.com/Kndndrj/Fusion-360-Arch-Linux-Script/main/fusion360_install.sh; \
chmod +x fusion360_install.sh
```
That should have created a new file called `fusion360_install.sh`.

Alternatively you can just clone the git repository.

## Usage
#### Simple Install
For a simple installation, just run:
```sh
./fusion360_install.sh install
```
#### Custom Install Directory
If you want to specify your own install directory and a directory to store
downloads to, run:
```sh
./fusion360_install.sh install -p "your/install/directory" -t "your/downloads/directory"
```
#### Installation Failed
If the installation process was interrupted or you have any other problems
during install, try using `install-clean` instead of `install`. For example:
```sh
./fusion360_install.sh install-clean -p "your/install/directory" ...
```
#### Uninstalling
To uninstall, simply run:
```sh
./fusion360_install.sh uninstall
```
And follow the on-screen instructions.
#### Special Cases
If you have any other needs, read "help". You find it by running:
```sh
./fusion360_install.sh -h
```

## Problems
#### Can't find a ".desktop" file
First check in ~/.local/share/applications/wine/Programs/Autodesk/. Wine should
have put the file there. If that is not the case, a backup start script has
been placed in installation directory named "fusion360". If you are having
trouble with this app launcher, just open the file with a text editor and
follow the instructions there.
#### Stuck loading after launch and the work area is all messed up
The first launch of the application is usually laggy on the sign in screen, be
patient and it will work!
Set your Graphics mode to OpenGL (User icon >> Preferences >> General >>
Graphics driver) and restart the program.
#### Error popup: we ran into a serious problem
You might have installed or updated the graphics drivers without doing a
reboot. So try rebooting before doing anything else. If even that doesn't fix
the problem, try doing a clean install.

## Other
If you have any other questions or comments, feel free to post them into the
[Issues](https://github.com/Kndndrj/Fusion-360-Arch-Linux-Script/issues)
section.
