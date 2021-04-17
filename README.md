net4801-linux
=============

Linux-based router/firewall configuration for the net4801 board from Soekris Engineering, Inc.

## Build

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

## Making Changes

Run `make menuconfig` to access the buildroot configuration system and make changes.
The configuration is saved to the file `.config` by default.
To update the configuration in the repository, copy the file into `configs/`
```
cp .config configs/net4801_defconfig
```
and commit.

It is possible to change the configuration of busybox and linux in a similary way.
The corresponding configuration systems can be accessed with `make busybox-menuconfig` or `make linux-menuconfig`.
These store configurations in `build/busybox-1.33.0/.config` and `build/linux-5.10.25/.config` respectively.
Copy any changes into `board/net4801/` and commit.
