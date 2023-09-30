# Dongle Host Driver for Broadcom/Cypress/Infineon Wi-Fi/BT Combos

Current version is forked from IFX AHD 100.10.107 and adapted for rockchip platform. 

The code base contains IFX AHD and rockchip platform code.

## Supported chips
```
CYW43438
CYW43455
CYW4354
CYW4373
CYW54591_SDIO
CYW54591_PCIE
CYW55572_SDIO
CYW55572_PCIE
```
## Build flags

Please see Kconfig and Makefile.

e.g. for rockchip platform and CYW43455
```
make -j$(grep -c processor /proc/cpuinfo) \
	KLIB=$(your kernel source directory) \
	M=$(pwd) \
	CONFIG_BCMDHD_ROCKCHIP_PLATFORM=y \
	CONFIG_CYW43455=y
```
## Currently working progress

Support more chip (chip_id, rev_id, manufacturer_id)
