net4801-linux
=============

Linux-based router/firewall configuration for the net4801 board from Soekris Engineering, Inc.

Clone the repository and the buildroot submodule:
```
git clone git@github.com:tjeastman/net4801-linux.git
cd net4801-linux
git submodule init
git submodule update
```

Build the system for the net4801 board:
```
make net4801_defconfig
make
```

The file `images/bzImage` contains the kernel along with an initramfs containing all necessary software and configuration.
