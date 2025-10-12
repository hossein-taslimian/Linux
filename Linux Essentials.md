# Linux Essentials
![Linux_logo](/Workspace/Linux/linux-logo.png)


* ## History & Intoduction

"Linux" in an open-source operating system that is based on the Unix model. "Unix" is a family of multitasking, multi-user computer operating systems that derive from the original AT&T Unix, whose development started in 1969 at the Bell Labs research center by Ken Thompson, Dennis Ritchie, and others. Initially intended for use inside the Bell System, AT&T licensed Unix to outside parties in the late 1970s.


### Linux Distribution
| Distro         |                                                                                    |
| -------------- | ---------------------------------------------------------------------------------- |
| Slackware Base | Slackware Linux, Slax, ConnochaetOS                                                |
| Debian Base    | Debian, Knoppix, Kubuntu, Xubuntu, Ubuntu, Linux Mint, Raspberry Pi OS, Kali Linux |
| Red Hat Base   | Red Hat Enterprise Linux, Mandrive, Fedora, CentOS, Rocky Linux                    |
| Jurix Base     | Astaro, openSUSE                                                                   |
| Enoch Base     | Ututo, Gentoo Linux, ChromeOS Flex                                                 |


```
LTS: Long-term Support
EOL: End Of Life
GUI: Graphical User Interface
CLI: Command Line Interface
```


### Virtual Machine Software
1. Microsoft Hiper-V
2. Oracle VirtualBox
3. Vmware
4. Parallels Desktop
5. etc...


#### Virtualization:
1. Baremetal (Type1)
2. Hosted (Type2)


### First command
```
whoami------------------username
hostname----------------host name
uname -a----------------kernel info
lsb_release -a----------os info
free -h-----------------ram info
lscpu-------------------cpu info
lsblk-------------------harddisc info
ip a "or" ip -br a------network & ip info
top "or" htop-----------task manager
date--------------------time
echo salam--------------write 'salam'
```










































#### Debian_Install sudo
```
su -
apt install sudo
usermod -aG sudo hossein
id hossein
```
#### No Password
```
nano /etc/sudoers.d/hossein
hossein ALL=(ALL) NOPASSWD:ALL
sudo su -
```
#### IP Check
```
ip -br a         or           ip a
```
#### SSH
```
sudo apt install openssh-server
sudo systemctl enable ssh
sudo systemctl start ssh
sudo systemctl status ssh

________on cmd or .etc
        ssh hossein@192.168.236.186
```



## Install Package

|            | Debian        | Redhat        |
| ---------- | ------------  | ------------- |
| Low Level  | dpkg          | rpm           |
| high level | apt-get/apt   | yum/dnf       |

### Low Level Install
```
Download package website: https://pkgs.org/

Download: wget <package link>
Install: dpkg -i <packagename.deb>
Install with aria2: aria2c <packagename.deb>
```
>When installing a particular **package**, it's generally necessary to install all of its required **dependencies**.

| دستور خاص                       | kari ke anjam midahad                             |
| -------------------------------- | ------------------------------------------------- |
| dpkg -L packagename              | این پکیج در چه مسیرهایی فایل کپی کرده          |
| dpkg -S /usr/share/doc/aria2/... | این مسیر برای چه پکیجی هست                      |
| dpkg -c packagename.deb          | Content_این پکیج در چه مسیرهایی فایل کپی میکند |
| dpkg -r packagename              | این پکیج را پاک کن                               |
| dpkg -P packagename              | این پکیج را پرج کن                               |
| dpkg --help                      | راهنمای این دستور.برای تمام دستورها            |

### High Level Install
