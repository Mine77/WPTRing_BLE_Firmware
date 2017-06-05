# WPTRing_BLE_Firmware
This is the BLE Firmaware code for the WPTRing project.
It is supposed to read data from I2C protocol based proximity sensors and send the data to PC or Smartphone over Bluetooth.

## How to complile on MAC
### Things to Download and Install
The SDK for nRF51822: [nRF5-SDK-v12-zip](https://www.nordicsemi.com/eng/Products/Bluetooth-low-energy/nRF51822)

nRF51 Command Line Tools: [nRF5x-Command-Line-Tools-OSX](http://www.nordicsemi.com/eng/Products/Bluetooth-low-energy/nRF51822)

The GCC Compliler: [GNU ARM Embedded Toolchain](https://launchpad.net/gcc-arm-embedded)

The Jlink Driver: [J-Link Software and Documentation pack for MacOSX](https://www.segger.com/downloads/jlink)
### Configuration
Open **..../nRF5_SDK_12.3.0_d7731ad/components/toolchain/gcc/Makefile.posix** 
and configure the GNU installed root:
```
GNU_INSTALL_ROOT := /usr/local/gcc-arm-none-eabi-5_4-2016q3
GNU_VERSION := 6.0.2
GNU_PREFIX := arm-none-eabi
```
### Compile and Flash
According to the Makefile of this project, the project folder need to be placed here: **..../nRF5_SDK_12.3.0_d7731ad/examples/ble_peripheral/wpt_ring**

The Makefile is here: **..../wpt_ring/pca10028/s130/armgcc/Makefile**

The RAM and Flash address settings are done in the WPTRing_gcc_nrf51.ld, in the same folder above
In the Makefile it already provides command for flashing:
```
make erase             //for erasing the flash
make flash_softdevice  // for flashing the softdevice
make flash             // for flashing the program
```
Run these three commands in sequence will acomplish the flashing.
