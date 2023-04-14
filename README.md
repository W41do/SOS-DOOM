# **SOS DOOM**

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

Použili jsme
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

rm -rfv /usr/share/locale
rm -rfv /usr/lib/modules/.../kernel/fs

proxy - ok
gdm - ok
event - ok + clean.sh (nn)
history - ok + pridat do clean.sh
gpg NOOOOOOOOOOOOOOO
krb5 - ok
ldap - ok
lua - ok
libm - ok
cursor - ok
pam - to work or not to work
api - ok
sss - ok
alloc - ok
c++ - ok
ss2 - ok
bcc - ok
trace - ok
browser - ok
cpu - ok



OVA UWUUUUUUU


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




usr/libexec/vi az na konci delete...
```