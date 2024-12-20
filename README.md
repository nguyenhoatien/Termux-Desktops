# PROOT-DISTRO (🍥 DEBIAN)

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

Then install Debian and login once it finishes:

```
proot-distro install debian
proot-distro login debian
```

Update repositories and install any package you want:

```
apt update 
apt upgrade

apt install sudo nano adduser -y
```

Create an user and give the sudo privileges:

```
adduser debian
nano /etc/sudoers
```

```
# Add the following line to the file
debian ALL=(ALL:ALL) ALL
```

## ⚙️ Installing Desktops

XFCE4

```
proot-distro login debian --user debian
```

```
sudo apt install xfce4
```

## Hardware Acceleration in Termux

You need to install the following packages in Termux:

```
pkg install mesa-zink virglrenderer-mesa-zink vulkan-loader-android virglrenderer-android
```

## ⬇️ Download scripts easily

```
wget https://raw.githubusercontent.com/nguyenhoatien/Termux-Desktops/main/startxfce4_debian.sh
chmod +x startxfce4_debian.sh
```

Now you can run Debian with XFCE4 UI:

```
./startxfce4_debian.sh
```
