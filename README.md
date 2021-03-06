# RPI3 Image with native monitor mode and/TFT (3.5) Support

This uses re4son's PI TFT kernel with Nexmon firmware for native monitor mode.

## Instructions

On Ubuntu or Kali download prereqs:
```bash
apt-get install -y git-core gnupg flex bison gperf libesd0-dev build-essential \
zip curl libncurses5-dev zlib1g-dev libncurses5-dev gcc-multilib g++-multilib \
parted kpartx debootstrap pixz qemu-user-static abootimg cgpt vboot-kernel-utils \
vboot-utils bc lzma lzop xz-utils automake autoconf m4 dosfstools rsync u-boot-tools \
schedtool git e2fsprogs device-tree-compiler ccache dos2unix debootstrap
```
Get the latest kernel by running bootstrap.sh
``bash
./bootstrap.sh
```
Then run pi3.sh with version numbr
```bash
./pi3.sh 0.1
```

## Modification

To change the size of LCD screen modify the command line:
```bash
sudo chroot $dir /bin/bash -c "/root/re4son-pi-tft-setup -t 35r -u /root"
```
35r is for a 3.5" LCD (Adafaruit).  For different size screens change 35r to match your screen:

https://github.com/Re4son/Re4son-Pi-TFT-Setup/blob/rpts-4.4/re4son-pi-tft-setup#L102

Then run.

## Sources:

```bash
Steev's Scripts: https://github.com/offensive-security/kali-arm-build-scripts
re4son: https://whitedome.com.au/re4son/sticky-fingers-kali-pi/#Vanilla
re4son's github: https://github.com/re4son/
nexmon: https://github.com/seemoo-lab/bcm-rpi3
```
