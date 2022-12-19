
## Install Gnome Platform/SDK

 * flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
 * flatpak install org.gnome.Platform//43
 * flatpak install org.gnome.Sdk//43

## Build the package

 * Pay and download Simplify3D-5.0.0-linux-x64-installer.zip from the official
   site and put the zip together with the json file.
 * flatpak-builder --repo=mys3drepo simp1 simplify3d.json

## Add local repo

 * flatpak --user remote-add --no-gpg-verify mys3drepo mys3drepo

## Install the package

 * flatpak --user install mys3drepo com.ucrobotics.Simplify3D

## Update the package

 * flatpak --user update com.ucrobotics.Simplify3D

## Run the package

 * flatpak run com.ucrobotics.Simplify3D

 Note: you can also run it from the desktop launcher. We do provide a desktop
 file.
