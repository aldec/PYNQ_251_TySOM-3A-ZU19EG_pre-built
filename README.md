# PYNQ_251_TySOM-3A-ZU19EG_pre-built

# Table of Content
1. [How to download](#how_to_download)
1. [TySOM](#tysom_main)

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

## Pre-buil image for PYNQ

This repository contains pre-buit image for PYNQ v.2.5.1 for TySOM-3A-ZU19EG board and can be used to speed up process of building PYNQ.
