# **SOS DOOM**

## Clone & Run DOOM on Linux

### **1/ Terminal Window 1**
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

### **2/ Terminal Window 2**

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
> sudo Xephyr :3 -ac -screen 640x480x8
> ```

### **3/ Back to the First Terminal Window**

> Set terminal window output to display 3
> ```
> DISPLAY=:3
> ```

> Run DOOM :P
> ```
> ./linux/linuxxdoom -2
> ```


# CentOS Stream
### Minimal Install
#### Basic functionality.

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

~~yum install xorg-x11-server-Xvfb.x86_64~~ 
```
yum install xorg-x11-server-Xorg.x86_64
```
In first terminal
```
startx /usr/bin/xterm -- :1
```
```
Xephyr :2 -ac -screen 640x480x8
```
SECOND TERMINAL - CTRL + ALT + F2

```
DISPLAY=:2
```
```
./linux/linuxxdoom -2
```
SWITCH AGAIN TO FIRST TERMINAL WITH CTRL + ALT + F1

ENJOY