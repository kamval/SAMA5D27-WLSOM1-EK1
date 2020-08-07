## SAMA5D27-WLSOM1 BASICS: How to compile a demo and boot from SD card

Buildroot Video Step by Step Guide for SAMA5D27-WLSOM1-EK1 available on [youtube](https://www.youtube.com/) 

#### Software Pre Requirements:
- install etcher, check [ubuntu guide](https://github.com/balena-io/etcher) 
- install minicom
- TTL-232R-3V3, check [TTL/USB-3.3V ](https://store.comet.bg/Catalogue/Product/48646/) 

#### Linux update and version check:
```
sudo apt-get update
sudo apt-get upgrade

lsb_release -a 
```

#### Where to find info. on the web:
- Linux4SAM: [Landing page](https://www.at91.com/linux4sam/bin/view/Linux4SAM)
- Linux4SAM Buildroot: [How to BuildRoot](https://www.at91.com/linux4sam/bin/view/Linux4SAM/BuildRootBuild)
- Buildroot External: [Microchip SAMA5 Buildroot External](https://github.com/linux4sam/buildroot-external-microchip/)

#### Required packets:
```
sudo apt-get install subversion build-essential bison flex gettext \
libncurses5-dev texinfo autoconf automake libtool mercurial git-core \
gperf gawk expat curl cvs libexpat-dev bzr unzip bc python-dev

mkdir microchip
cd microchip
```

#### Git repositories:
```
git clone https://github.com/linux4sam/buildroot-at91.git
git clone https://github.com/linux4sam/buildroot-external-microchip.git

cd buildroot-external-microchip/
git checkout linux4sam_6.0 -b buildroot-external-microchip-linux4sam_6.0

cd ../buildroot-at91/
git checkout linux4sam_6.0 -b buildroot-at91-linux4sam_6.0
```
#### Configure and compile from sources a demo image:
```
BR2_EXTERNAL=../buildroot-external-microchip/ make sama5d27_wlsom1_ek_headless_defconfig
```

#### Change some basic system settings: 

```
make menuconfig

System configuration  --->
        ...
    [sama5d27-wlsom1] System hostname
    [SAMA5D27 Microchip Embedded Demo] System Banner
    [toor] Root password

save
exit

time make
```

#### Where to find ready image:
```
ls -l output/images/
```

#### Burn the image to SD card:
```
etcher-electron
```

Plug the ready SD card in J9 connector.

#### Play with image:
```
sudo minicom -b 115200 -D /dev/ttyS2
```
