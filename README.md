### SAMA5D27 Guide

A step by step guide to build from source Bulidroot for SAMA5D27-WLSOM1-EK1. 

This entry level guide would be useful for everybody who are making their first steps with Embedded Linux, [Buildroot](https://buildroot.org/) and [Microchip MPUs](https://www.microchip.com/design-centers/32-bit-mpus ). The guide is intended to get you up to speed and finish your project easier and faster.

#### About Buildroot:

[Buildroot](https://buildroot.org/downloads/manual/manual.html) is a tool that simplifies and automates the process of building a complete Linux system for an embedded system, using cross-compilation.
In order to achieve this, Buildroot is able to generate a cross-compilation toolchain, a root filesystem, a Linux kernel image and a bootloader for your target. Buildroot can be used for any combination of these options, independently (you can for example use an existing cross-compilation toolchain, and build only your root filesystem with Buildroot).
Buildroot is useful mainly for people working with embedded systems. Embedded systems often use processors that are not the regular x86 processors everyone is used to having in his PC. They can be PowerPC processors, MIPS processors, ARM processors, etc.
Buildroot supports numerous processors and their variants; it also comes with default configurations for several boards available off-the-shelf. 

#### About SAMA5D27-WLSOM1-EK1:

[ATSAMA5D27-WLSOM1-EK1](https://www.microchip.com/Developmenttools/ProductDetails/DM320117) is ideal for evaluating and prototyping with the SAMA5D27-WLSOM1, Wireless System On Module (SOM) and the SAMA5D27C-LD2G, LPDDR2 System In Package (SIP).
The Evaluation Kit is made up of a baseboard, an ATSAMA5D27-WLSOM1 SOM soldered on the baseboard and an ATSAMA5D27C-LD2G SIP soldered on the SOM.
The ATSAMA5D27-WLSOM1 Module integrates a 2-Gbit LPDDR2SDRAM, a Wi-Fi®/Bluetooth® module, a Secure Element device, a Power Management IC (PMIC), a QSPI memory, a 10/100 Mbps Ethernet PHY. 94 GPIO pins are provided by the SOM for general use in the system.
The baseboard features a wide range of peripherals, as well as a user interface. Connectors and expansion headers allows for easy customization and quick access to leading edge embedded features such as MikroElektronica Click Boards™.

<p align="center">
  <img width="609" height="504" src="https://github.com/kamval/SAMA5D27-WLSOM1-EK1/blob/master/Documents/a5d27_wlsom1_board.png">
</p>
