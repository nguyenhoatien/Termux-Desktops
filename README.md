# Termux Desktops (⛰️ ALPINE)

## 🏁 First steps

We are going to use Termux and Termux X11 in order to have a full Linux Desktop in our Android devices.

- [Termux](https://github.com/termux/termux-app/releases)
- [Termux X11](https://github.com/termux/termux-x11/releases)

First you need to install the following packages in Termux:

```
pkg update
pkg upgrade
pkg install x11-repo
pkg install termux-x11-nightly
pkg install tur-repo
pkg install pulseaudio
pkg install proot-distro
pkg install wget
pkg install git
```

Then install Alpine and login once it finishes:

```
proot-distro install alpine
proot-distro login alpine
```

Update repositories and install needed packages:

```
apk update
apk upgrade

apk add sudo nano dbus-x11 xfce4
```

Create an user and give the sudo privileges:

```
adduser alpine
nano /etc/sudoers

# Add the following line to the sudoers file
alpine All=(ALL:ALL) ALL
```

## Hardware Acceleration in Termux

You need to install the following packages in Termux:

```
pkg install mesa-zink virglrenderer-mesa-zink vulkan-loader-android virglrenderer-android
```

## ⬇️ Download scripts easily

```
wget https://raw.githubusercontent.com/nguyenhoatien/Termux-Desktops/main/startxfce4_alpine.sh
chmod +x startxfce4_alpine.sh
```

Now you can run Alpine with XFCE4 UI:

```
./startxfce4_alpine.sh
```
