# WPTRing_BLE_Firmware
This is the BLE Firmaware code for the WPTRing project.
It is supposed to read data from I2C protocol based proximity sensors and send the data to PC or Smartphone over Bluetooth.

## How to complile on MAC
### Things to Download
SDK (include Softdevice)
nRF5-SDK-v12-zip: https://www.nordicsemi.com/eng/Products/Bluetooth-low-energy/nRF51822
GCC Compiler
GCC ARM Embedded: https://launchpad.net/gcc-arm-embedded
Jlink Tools
J-Link Software and Documentation pack for MacOSX: https://www.segger.com/downloads/jlink
### 
First the According to the Makefile file, this folder need to be placed in side the SDK folder.
> ...../nRF5_SDK_12.3.0_d7731ad/examples/ble_peripheral/wpt_ring
The Makefile is here:
> ......./wpt_ring/pca10028/s130/armgcc/Makefile
The RAM and Flash address settings are done in the WPTRing_gcc_nrf51.ld, in the same folder above

