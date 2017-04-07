# BLE (Bluetooth Low Energy) Toolkit for LabVIEW

**Bluetooth Low Energy** (BLE, Bluetooth LE, also known as Bluetooth Smart) is a wireless personal area network technology designed and marketed by the [Bluetooth Special Interest Group](https://www.bluetooth.com/) aimed at novel applications in the healthcare, fitness, beacons, security, and home entertainment industries. Compared to [Classic Bluetooth](https://www.bluetooth.com/), BLE is intended to provide considerably reduced power consumption and cost while maintaining a similar communication range. Further details in the [Bluetooth Low Energy Wikipedia entry](https://en.wikipedia.org/wiki/Bluetooth_low_energy).

While [**LabVIEW** supports Classic Bluetooth](http://www.ni.com/white-paper/3260/en/) (on Windows), it does not provide support for **BLE**. To solve this issue, a workaround is to use a BLE USB dongle to handle the communication.  http://digital.ni.com/public.nsf/allkb/4BA51235CFC8519086257F5E005E81D5

The **BLE Toolkit for LabVIEW** is an implementation of the [BGAPI protocol v1.3](http://www.silabs.com/documents/login/reference-manuals/Bluetooth_Smart_Software-BLE-1.3-API-RM.pdf) (by [Silicon Labs](http://www.silabs.com/)). **BGAPI protocol** is a based command and response protocol that allows the Bluetooth
Smart stack (in Silicon Labs BLE devices) to be controlled form an external host and an application over USB/UART.

This Toolbox has been developed and tested with the [BLE USB dongle BLED112](http://www.silabs.com/products/wireless/bluetooth/bluetooth-low-energy-modules/ble121lr-bluetooth-smart-long-range-module1)

## Installation
To install the **BLE Toolkit for LabVIEW**, the **VI Package Manager** by [JKI](http://jki.net/) is needed.
1. Download and install [VI Package Manager](https://vipm.jki.net/get)
2. Download and install the last VI package for the **BLE Toolkit for LabVIEW** from [here](https://github.com/rcassani/BLE-Toolkit-LabVIEW/releases)

## Usage
1. Obtain a BLED112 USB dongle (e.g. in [Digi-Key](https://www.digikey.ca/products/en?keywords=bled112))
2. Install the drivers provided by [Silicon Labs](http://www.silabs.com/documents/login/software/BLED112-Signed-Win-Drv.zip)
3. Verify the COM number for the dongle in **Windows Device Manager**
5. Open the `ble_scan_devices.vi` example located in:
`<Labview>\examples\BLE\Examples\ble_scan_devices.vi`
6. Select the COM port corresponding to the **BLED112 USB dongle**
7. Run the VI

![alt text](https://cloud.githubusercontent.com/assets/8238803/24782597/343490fc-1b15-11e7-8e10-7b7dde23230d.png "ble_scan_devices.vi Front Panel")
`ble_scan_devices.vi` Front Panel

## Examples
Three examples are provided with the **BLE Toolkit for LabVIEW**. These
examples are located in: `<LabVIEW>\examples\BLE\Examples\ble_scan_devices.vi`

1. `ble_scan_devices.vi`  
  Discover and connect to BLE devices

2. `ble_read_write_characteristics.vi`  
  Read and Write a Characteristic value, providing the **UUID** for **Service** and **Characteristic**

3. `ble_read_hr_monitor.vi`
  Acquire Heart Rate data stream, for devices with Heart Rate Profile

## Creating VI Package file
Alternatively, the files in this repository can be used to build the VI Package for the **BLE Toolkit for LabVIEW**.
