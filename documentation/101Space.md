# 101 Space

## Linux Kernel Introduction

> Objective: Understand the Linux Kernel compilation process and built system  
> Proficiency Level: Basic

### Linux Kernel Compilation

```
root@workstation:~# apt-get update
root@workstation:~# apt-get upgrade
root@workstation:~# apt-get install linux-headers-$(uname -r) kernel-package libncurses5 libncurses5-dev git
```

```sh
user@workstation:~$ git clone git://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git
Cloning into 'linux'...
remote: Counting objects: 5396825, done.
remote: Compressing objects: 100% (2538/2538), done.
remote: Total 5396825 (delta 2876), reused 3072 (delta 2127)
Receiving objects: 100% (5396825/5396825), 984.15 MiB | 6.28 MiB/s, done.
Resolving deltas: 100% (4522724/4522724), done.
Checking connectivity... done.
Checking out files: 100% (59844/59844), done.
user@workstation:~$ 
```

```sh
user@workstation:~$ uname -a
Linux Minnowboard 3.2.0-4-amd64 #1 SMP Debian 3.2.63-2+deb7u2 x86_64 GNU/Linux
```

```sh
user@workstation:~$ cd linux
```

```sh
user@workstation:~/linux$ ls
arch   certs    CREDITS  Documentation  firmware  include  ipc     Kconfig  lib          Makefile  net     samples  security  tools  virt
block  COPYING  crypto   drivers        fs        init     Kbuild  kernel   MAINTAINERS  mm        README  scripts  sound     usr
user@workstation:~/linux$ 
```

```sh
user@workstation:~$ make oldconfig
<You will be asked configuration questions not answered, hit Enter for all of them>
DesignWare Cores SATA support (SATA_DWC) [N/m/?] (NEW)
```

```sh
user@workstation:~$ make
root@workstation:~# make modules_install
root@workstation:~# make install
```

Reboot your workstation and confirm the new version has been installed

```
user@workstation:~$ uname -a
Linux Minnowboard 3.19.0-rc7+ #1 SMP Debian ... x86_64 GNU/Linux
```





