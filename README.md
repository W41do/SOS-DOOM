<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://www.youtube.com/watch?v=g9gHC2quF3A">
    <img src="https://raw.githubusercontent.com/W41do/SOS-DOOM/master/assets/doom_256x183.png" alt="Logo" width="256">
  </a>

  <h3 align="center">« DOOM (1993) Original Version  »</h3>

  <p align="center">
    « SOS Edition »
    <br />
    <a href="https://store.steampowered.com/app/2280/DOOM_1993/"><strong>« Game on Steam »</strong></a>
    <br />
    <br />
    <a href="TODO">« TODO »</a> · <a href="TODO">« Documentation »</a> · <a href="TODO">« TODO »</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#application-description">TODO</a>
      <ul>
        <li><a href="#erd-entity-relationship-diagram">TODO</a></li>
          <ul>
            <li><a href="#mysql-workbench-erd">TODO</a></li>
            <li><a href="#postgresql-pgadmin-erd">TODO</a></li>
            <li><a href="#description-of-each-table">TODO</a></li>
            <li><a href="#3rd-normal-form">TODO</a></li>
          </ul>
        <li><a href="#use-case-diagram">TODO</a></li>
        <li><a href="#system-context-diagram">TODO</a></li>
      </ul>
    <li><a href="#non-functional-and-functional-requirements">TODO</a></li>
    </li>
    <li>
      <a href="#ddl-&-dml-scripts">TODO</a>
      <ul>
        <li><a href="#postgresql">TODO</a></li>
         <ul>
            <li><a href="#screenshots-from-the-pgadmin">TODO</a></li>
         </ul>
         <li><a href="#mysql">TODO</a></li>
      </ul>
    </li>
    <li>
     <a href="#license">TODO</a>
    </li>
  </ol>
</details>


<!-- ABOUT THIS GAME -->
## **ABOUT THIS GAME**
----
The demons came and the marines died... except one. You are the last defense against Hell. Prepare for the most intense battle you’ve ever faced. Experience the complete, original version of the game DOOM developed by id Software, and originally released in 1993, DOOM pioneered and popularized the first-person shooter, setting a standard for all FPS games. An enhanced version was released on PC, consoles, and mobile devices in 2019.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### **Minimum system requirements:**
----
**CPU**:
486 processor operating at a minimum of 66MHz or any Pentium /Athlon processors

**RAM**:
8 MB RAM

**OS**:
Windows 95/98/ME/ 2000 operating system or **Linux** ;)

**STO**:
40 MB of uncompressed hard disk space 100MB of free hard drive space for the Windows/Linux swap file (in addition to install space)

**Sound**:
A 100% Windows 95/98/ME/2000-compatible true 16-bit sound card and drivers or let Linux do the magic.

**Recommended peripheral**  : 100% Windows 95/98/ME/2000-compatible mouse and driver
100% Windows 95/98/ME/2000-compatible keyboard or let Linux do the magic.

**NOTE**: A 100% Windows 95/98/ME/2000-compatible computer system (including compatible 32-bit drivers for video card, sound card and input devices) or let Linux do the magic.

> *There are only official system requirements on the site which are released by developers or an official publisher.*

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ABOUT THE PROJECT -->
## **ABOUT THIS PROJECT**
---
### **Assignment and purpose**

The goal of this project was to modify a Linux kernel-based operating system to **minimize its size to the smallest possible**. The minimized system had to be able to **run DOOM**.

The project is based on an artificially created problem. Minimalistic systems can be found in practice. The aim of the project is to deepen knowledge of the structure of operating systems, especially those based on the Linux kernel. Linux-based systems are commonly used on various hardware platforms, from single-board computers and desktops to computing clusters. They are also used in a wide range of devices related to study programs at the faculty. These include mobile devices, sensor units, multimedia devices, network devices (routers, switches), medical devices, and more.

The output of the project is a modified operating system in the form of a virtual machine, which can be run using the Oracle VM VirtualBox (VB) software.

The operating system for the project was chosen from the following options:

CentOS (Stream) `www.centos.org`,

Fedora `getfedora.org`,

Debian `www.debian.org`,

Ubuntu `ubuntu.com`.

The **current** version of the operating system as of February 01, 2023 was used to solve the project.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### **Solution Approach**
---

#### **Selection of Linux kernel-based operating system**
CentOS Stream 9 proved to be the most suitable choice primarily due to its minimal installation option and user-friendly environment.

 

After installing the operating system, the original source code of Linux DOOM released by ID software in 1997 was downloaded and modified [`https://github.com/id-Software/DOOM`] by re-typing variables and adjusting constants in specific places.

The source code modification and compilation were done following the tutorial from the YouTube channel Gabriel_
`https://www.youtube.com/watch?v=9JgQfQHHhTw`


Shareware (*Shareware is a software marketing concept where an incomplete or time-limited version of a program is released to entice people into buying the full (registered) version.*) was obtained from the website `www.doomworld.com`

> `https://www.doomworld.com/classicdoom/info/shareware.php`





TODO 


Section on running DOOM on a minimal installation of CentOS Stream 9 without GUI.

<p align="right">(<a href="#readme-top">back to top</a>)</p>
















# **DANGER ZONE**
# **DANGER ZONE**
# **DANGER ZONE**
# **DANGER ZONE**
# **DANGER ZONE**

## The content below has not been edited yet and served primarily as a solving procedure for the author.
---
## The content below has not been edited yet and served primarily as a solving procedure for the author.
---
## The content below has not been edited yet and served primarily as a solving procedure for the author.
---
## The content below has not been edited yet and served primarily as a solving procedure for the author.
---
## The content below has not been edited yet and served primarily as a solving procedure for the author.
---

## Clone & Run DOOM on Linux

### **WITH GUI**

#### **1/ Terminal Window 1**
> **1.1/** Open terminal and clone this project
> ```
> git clone https://github.com/W41do/SOS-DOOM.git
> ```

> **1.2/** Move to this directory
> ```
> cd SOS-DOOM/DOOM/linuxdoom-1.10/
> ```

> **1.3/** Remake
> ```
> make clean
> ``` 
> ```
> make
> ```

#### **2/ Terminal Window 2**

> **2.1/** Open second terminal and search for `xephyr`
> ```
> yum search xephyr
> ```

> Note: If you don't have yum, you will have to install it with something else based on your OS ;)

> **2.2/** And then install (as root) with this command
> ```
> yum install packagename
> ```
> Where packagename is the package name found with search (should be seen in the left column of search results)

> Run Xephyr
> ```
> sudo Xephyr :9 -ac -screen 960x600x8
> ```
> NOTE: number is 9 is for virtual monitor 9. I assume no one has 9 monitors so 9 is not used and can be used now.

#### **3/ Back to the First Terminal Window**

> Set terminal window output to display 9
> ```
> DISPLAY=:9
> ```

> Run DOOM :P
> ```
> ./linux/linuxxdoom -3
> ```
> NOTE: parameter -3 is for scaling. You are telling doom to scale pixels 3x. Default doom resolution is 320x200. You have set Xephyr monitor for 960x600 == 3x 320x200.

# **DOOM ON LINUX WITHOUT GUI**


# CentOS Stream
### Minimal Install
#### Basic functionality.

protože na linuxu pojede jen doom.

Proces:

Login:
```
CentOS Stream 9
Kernel 5.14.0-295.e19.x86_64 on an x86_64

localhost login: root
Password: student
```
After Fresh Install:
```
du / --exclude=/{proc,sys,dev} -abc | sort -n

...

1161858241      total
```

```
dnf install git
```
```
git clone https://github.com/W41do/SOS-DOOM.git
```
```
dnf remove git
```
```
dnf instal Xephyr
```
```
yum install xorg-x11-xinit.x86_64
```
```
yum install xterm.x86_64
```
```
yum install xorg-x11-server-Xvfb.x86_64
```
```
yum install xorg-x11-server-Xorg.x86_64
```
In first terminal

~~Xvfb :1 -screen 0 960x600x8 &~~

```
startx /usr/bin/xterm -- :1
```
The startx command starts an X11 server and a session manager, and launches an X client application, such as a window manager or a desktop environment. In this case, it is launching the xterm application, which is a simple terminal emulator that provides a command-line interface within an X11 window. The -- :1 option specifies the display number to use for the X11 server, which is :1 in this case. This means that the X11 server will listen on TCP/IP port 6001 for incoming X11 connections.

In summary, the command startx /usr/bin/xterm -- :1 starts an X11 server and launches an X11 terminal emulator application.

```
Xephyr :2 -ac -screen 960x600x8
```
SECOND TERMINAL - CTRL + ALT + F2

Move to the directory where is doom.wad stored.
```
cd SOS-DOOM/DOOM/linuxdoom-1.10
```
Send output do DISPLAY 2
```
DISPLAY=:2
```
```
export DISPLAY=:2
```

```
./linux/linuxxdoom -2
```
SWITCH AGAIN TO FIRST TERMINAL WITH CTRL + ALT + F1

ENJOY




My answer is related to console mode Linux only. So, please be aware of that.

If you are using Linux with no X-Window installed (like usually servers do) than you'll need to edit /etc/default/grub file adding following lines:

GRUB_GFXMODE=1980x1200x32
GRUB_GFXPAYLOAD_LINUX=1980x1200x32

Then update grub config:

sudo update-grub

and reboot your VirtualBox instance.

 sudo grub2-mkconfig -o /boot/grub2/grub.cfg.

 When a nice resolution is found (I’ll use 1280×1024 below) take the following steps to change the resolution:

    Start your VM and log in.
    Open the file /etc/default/grub in your favourite editor.
    Add (or replace) the following lines:
    GRUB_GFXMODE=1280x1024 # width x height required - see below
    GRUB_CMDLINE_LINUX_DEFAULT="nomodeset"
    GRUB_GFXPAYLOAD_LINUX=keep
    1
    2
    3
    	
    GRUB_GFXMODE=1280x1024 # width x height required - see below
    GRUB_CMDLINE_LINUX_DEFAULT="nomodeset"
    GRUB_GFXPAYLOAD_LINUX=keep
    Save the file and exit the editor
    Run the following command to update GRUB
    sudo update-grub
    Restart your VM
    Taadaaa!


# PROCES AUTOMATIZACE

doom original resolution - 320x200

set screen to triple the sizeLS


cvt 960 600 60


doom.sh:
```
#!/bin/sh

# cvt 960 600 60 # to see args for command below
xrandr --newmode "960x600" 45.25 960 992 1088 1216 600 603 609 624 -hsync +vsync
# xrandr --listmonitors # to see --addmode arg below
xrandr --addmode Virtual-1 960x600
xrandr -s 960x600
Xephyr :2 -ac -screen 960x600x8
```


# **SOS DOOM OVA**

## Clone & Run DOOM on Linux

to start: 

1/ login
2/ select option 1 - doom
3/ ctrl alt f2 to open next tty
4/ login
5/ switch back to tty 1 with ctrl alt f1
6/ enjoy


## under 600 mb actions

```
dnf remove e2f sprogs
iproute

delete all python with
find / -name *python* -delete
find / -name *.py -delete
find / -name *pycache* -delete


find / -name *ssl* -exec rm -rf {} +
find / -name *http* -exec rm -rf {} +
find / -name *NetworkManager* -exec rm -rf {} +
find / -name *coreutils* -exec rm -rf {} +
find / -name *zlib* -exec rm -rf {} +
# POLICY
find / -name *olicy* -exec rm -rf {} +
find / -name *librepo* -exec rm -rf {} +
rm -rf /usr/share/zsh
find / -name *curl* -exec rm -rf {} +
find / -name *elfutils* -exec rm -rf {} +
find / -name *libcomps* -exec rm -rf {} +
find / -name *libmodulemd* -exec rm -rf {} +
find / -name *ssh* -exec rm -rf {} +



find / -name *glibc* -exec rm -rf {} +
find / -name *nss* -exec rm -rf {} +
find / -name *libselinux* -exec rm -rf {} +
find / -name *ftp* -exec rm -rf {} +
find / -name *ipv4* -exec rm -rf {} +
find / -name *ipv6* -exec rm -rf {} +






find / -name *route* -exec rm -rf {} +
find / -name *nat* -exec rm -rf {} +
find / -name *tls* -exec rm -rf {} +
find / -name *tcp* -exec rm -rf {} +
find / -name *udp* -exec rm -rf {} +
find / -name *netfilter* -exec rm -rf {} 
rm -rf usr/lib/modules/5.14. ... /kernel/drivers/net
rm -rf usr/lib/modules/5.14. ... /kernel/net
find / -name *network* -exec rm -rf {} +
find / -name *online* -exec rm -rf {} +
find / -name *dns* -exec rm -rf {} +
find / -name *domain* -exec rm -rf {} +
find / -name *dhcp* -exec rm -rf {} +
find / -name *packet* -exec rm -rf {} +




find / -name *gnome* -exec rm -rf {} +
rm -rf /boot/initramfs-{kernel_version}...kdump.img
find / -name *kdump.img -exec rm -rf {} +
rm -rf /boot/System.map...

rm -rf /lib/modules/.../kernel/drivers NO!!!
rm -rf /lib/modules/.../kernel/sound
find / -name *chromium* -exec rm -rf {} +



cd /lib/udev/rules.d/
rm -rf 40-*
rm -rf 70-*


find / -name *scsi* -exec rm -rf {} +
find / -name *sqlite* -exec rm -rf {} +
find / -name *usb* -exec rm -rf {} +
rm -rfv /usr/share/licences/
rm -rfv /usr/share/locale/

OVA

find / -name *amd* -exec rm -rf {} +
find / -name *intel* -exec rm -rf {} +
find / -name *nouveau* -exec rm -rf {} +
find / -name *hw* -exec rm -rf {} +
find / -name *debug* -exec rm -rf {} +

rm -rfv /usr/share/font*
rm -rfv /usr/share/misc
rm -rfv /boot/grub2/locale


rm -rfv /usr/libexec/Xorg.wrap

OVA

proxy - ok jj
gdm - ok jj
event - ok + clean.sh (nn) jj
history - ok + pridat do clean.sh jj
krb5 - ok jj
ldap - ok jj
lua - ok jj
libm - ok jj
cursor - ok jj

api - ok
sss - ok
alloc - ok
c++ - ok
ss2 - ok
bcc - ok
trace - ok
browser - ok
cpu - ok



OVA


samsung
nokia

usr lib .build-id


du sort -n

fedoraproject
usr share metainfo

usr

usr bin

sbin

share

kernel modulz

boot

metadata a co se nepouziva tak smazat

gcc - nemazat!!! nefunguje reboot ani shutdown :D




modules



rules
local?
audit NOO




usr/libexec/vi az na konci delete... ? spis ne


deleting from usr bin

rm -rfv *host*
rm -rfv sg_*
rm -rfv *se*

rm all sg

zkusit:
au* jj
*base* jj
*code* jj
ch NO
col jj
cron jj
pydoc jj
sha jj

putty ?
ip*
script*
show*
info*

print*
ren*
pw*
get*
pi*

all *color*
wa*
gr* NO

OVAAAAAAAAAAAAAAAAAAAAAAAAAA

grep NOOOO




lsi*
lsl*
wh*
dir*
ex ?

fc JJ
fg JJ


dbus
env


gr
kdb
kmod
libinput
locale
lsblk

nl

time




ge* jj
gp* jj
in* jj
up* jj
un* jj
```