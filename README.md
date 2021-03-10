# PYNQ_251_TySOM-3A-ZU19EG_pre-built

## Table of Content
1. [How to download](#how_to_download)
2. [TySOM](#tysom_main)
3. [Supported Interface](#tysom_supported_interfaces)
4. [Known issues](#tysom_known_issues)
5. [Pre-buil image for PYNQ](#pre_built_image)
6. [Instruction](#instruction)

<a name="how_to_download"/>

## How to download
This repository contains larg files which are not supported by GitHub by default in that case only the below procedure downloads this repository correctly:
1. Download and install [Git Large File Storage](https://git-lfs.github.com/).
2. Set up Git LFS for your user account.
```
git lfs install
```
3. Clone the repository.
```
git clone <path>
```

**Note: Downloading by _Download ZIP_ does not work correctly.**

<a name="tysom_main"/>

## TySOM

TySOM is a family of development boards for embedded applications that features Xilinx® Zynq™ all programmable module combining FPGA with ARM® Cortex processor. Plethora of included peripherals makes these boards useful in various embedded applications like Automotive, IoT, Industrial automation or embedded HPC.

Aldec provides the following list of boards:
-	[TySOM-3A (Xilinx Zynq UltraScale+ ZU19EG)](https://www.aldec.com/en/products/emulation/tysom_boards/zynq_ultrascale_mpsoc_boards/tysom_3a)

[Link to the TySOM boards page](https://www.aldec.com/en/products/emulation/tysom_boards)

TySOM-3A, TySOM-3, TySOM-2 and TySOM-2A families contain FMC connectors which can be used to extend devices and peripherals not included in TySOM boards. Due to non-proprietary connectors like FMC Daughter Cards can be reused across different hardware platforms.

<a name="tysom_supported_interfaces"/>

## Supported Interface

The following interfaces are supported in the current version:
- Display Port
- USB
- Ethernet
- Wi-Fi
- PMOD (supported by Microblaze controler)
- Switches
- LEDs
- UART
- I2C
- micro SD
- NAND memory
- SPI memory

<a name="tysom_known_issues"/>

## Known issues

HDMI input/output ports are not functional. The problem is under an investigation.

<a name="pre_built_image"/>

## Pre-buil image for PYNQ

This repository contains pre-buit image for PYNQ v.2.5.1 for TySOM-3A-ZU19EG board and can be used to speed up process of building PYNQ.

<a name="instruction"/>

## Instruction

1. Extract the provided archive.
As a result of the operation the user gets TySOM-3A-ZU19EG.img.

2. Flash a micro SD card with using the provided image for the board
Use BalenaEtcher software for a safe flashing or use dd command.
BalenaEtcher software uses GUI and helps to avoid a mistake.
eAn Execution time depends on SD card class. It takes about 30 minutes.

Notes for dd flashing:
dd if=./TySOM-3A-ZU19EG.img of=/dev/sdb

*Attention! Set a proper device in the "of" parameter. The device should be a micro SD card.*

3. Power on the board

4. PYNQ starts with a WebUI. Get an access to the UI:
- Connect an Ethernet cable.
- Log in to the WebUI
http://pynq::9090

or if pynq device is not visible in a user network:

Connect micro USB to the PC. Launch a UART terminal. Check an IP address.

xilinx@localhost:~$ ifconfig
eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
        inet **123.456.7.890**  netmask 255.255.255.0  broadcast 123.456.7.255
        inet6 fe80::20a:35ff:fe3a:200  prefixlen 64  scopeid 0x20<link>
        ether 00:0a:35:3a:02:00  txqueuelen 1000  (Ethernet)
        RX packets 46680  bytes 2945262 (2.9 MB)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 100  bytes 15221 (15.2 KB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
        device interrupt 31

**123.456.7.890:9090**
Load the PYNQ website on a PC - use a PYNQ IP address (in the example **123.456.7.890**) in an Internet browser.

WebUI should appear. Log in with using default password: xilinx
