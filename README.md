# Termux-Desktops

## 🏁 First steps

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

Then install Ubuntu and login once it finishes:

```
proot-distro install ubuntu
proot-distro login ubuntu
```

Update repositories and install any package you want:

```
apt update 
apt upgrade

apt install sudo nano adduser -y
```

Create an user and give the sudo privileges:

```
adduser ubuntu
nano /etc/sudoers
```

```
# Add the following line to the file
ubuntu ALL=(ALL:ALL) ALL
```

## ⚙️ Installing Desktops

XFCE4

```
proot-distro login ubuntu --user ubuntu
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
wget https://raw.githubusercontent.com/nguyenhoatien/Termux-Desktops/main/startxfce4_ubuntu.sh
chmod +x startxfce4_ubuntu.sh
```

Now you can run Ubuntu with XFCE4 UI:

```
./startxfce4_ubuntu.sh
```
