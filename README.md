![Logo](admin/Pine64.png)
ioBroker Pine64-Monitor Adapter
==============

[![NPM version](http://img.shields.io/npm/v/iobroker.rpi2.svg)](https://www.npmjs.com/package/iobroker.rpi2)
[![Downloads](https://img.shields.io/npm/dm/iobroker.rpi2.svg)](https://www.npmjs.com/package/iobroker.rpi2)

[![NPM](https://nodei.co/npm/iobroker.rpi2.png?downloads=true)](https://nodei.co/npm/iobroker.rpi2/)

Pine64-Monitor implementation for integration into ioBroker. It is derived from iobroker.rpi with GPIOs, but not yet tested.

Tested only with armbian - GPIOs not tested

## Important Information
Works only with node >= 0.12

**ioBroker must run under root to may control GPIOs.**

## Installation
After installation you have to configure all required modules via administration page.

After start of iobroker.Pine64, all selected modules generates
an object tree in ioBroker within Pine64.<instance>.<modulename>
e.g. Pine64.0.cpu

Be sure, that python and build-essential are installed:

```
sudo apt-get update
sudo apt-get install -y build-essential python
```

Following Objects are available after selection:

#### **CPU**

- cpu_frequency
- load1
- load5
- load15

#### **Raspberry (vcgencmd is required)**

- cpu_voltage
- mem_arm
- mem_gpu

#### **Memory**

- memory_available
- memory_free
- memory_total

#### **Network (eth0)**
- net_received
- net_send

#### **SDCard**
- *sdcard_boot_total* (not supprted by armbian therefore removed)
- *sdcard_boot_used* (not supprted by armbian therefore removed)
- sdcard_root_total
- sdcard_root_used

#### **Swap**
- swap_total
- swap_used

#### **Temperature**
- soc_temp

#### **Uptime**
- uptime

#### **WLAN**
- wifi_received
- wifi_send

## Configuration
On configuration page you can select following modules:

- CPU
- Raspberry
- Memory
- Network
- SDCard
- Swap
- Temperature
- Uptime
- WLAN

## Logfiles / Configuration Settings

## Features

## Todo

## Tested Hardware
 - Odroid C1
 - Raspberry Pi 1

## GPIOs
You can read and control GPIOs too.
All what you need to do is to configure in the settings the GPIOs options (additional tab). 

![GPIOs](img/pi3_gpio.png)

After some ports are enabled following states appear in the object tree:
- Pine64.0.gpio.PORT.state

## Changelog

 
### 0.0.1 (2016-11-16)
 - Initial commit. Alpha Version.

## License

Copyright (c) 2015-2016 husky-koglhof <husky.koglhof@icloud.com>

MIT License
