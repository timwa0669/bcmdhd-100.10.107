# Dongle Host Driver for Broadcom/Cypress/Infineon Wi-Fi/BT Combos
Current version is forked from IFX AHD 100.10.107 and adapted for rockchip platform. 

The code base contains IFX AHD and rockchip platform code.
## Supported chips
```
CYW43438_SDIO
BCM43456_SDIO
CYW43455_SDIO
CYW4354_SDIO
CYW4373_SDIO
CYW54591_SDIO
CYW55572_SDIO
CYW54591_PCIE
CYW55572_PCIE
```
## Build flags
Please see Kconfig and Makefile.

e.g.

Rockchip Platform

CYW43455 chip with SDIO interface, oob enabled by default
```
make -j$(grep -c processor /proc/cpuinfo) \
	KDIR=$(your kernel source directory) \
	M=$(pwd) \
	CONFIG_BCMDHD_ROCKCHIP_PLATFORM=y \
	CONFIG_CYW43455_SDIO=y
```
## DT-Bindings configuration (in progress)
See dt-bindings-rockchip-example.md for more information
## Currently to-do list
1. Support more chip (chip_id, rev_id, manufacturer_id)

2. Support mapping firmware/nvram/clm_blob via chip_id only

3. Support compatible="android,bcmdhd_wlan" dt-bindings for rockchip platform (Currently oob irq information is from rockchip wlan-platdata dt-bindings)
