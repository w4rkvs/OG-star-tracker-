# OG Star Tracker : Wireless Control Hardware (Rev 2.0)

This simple PCB and firmware intends to make it easier to control the OG Star Tracker. If you have any suggestions/ideas about new features or would like to contribute, post in the OG star tracker [discord server](https://discord.com/invite/dyFKm79gKJ) or message me (Discord: jahh#8924).
If you like this work, feel free to connect with me on [Github](https://github.com/jugal2001) or [Linkedin](https://www.linkedin.com/in/jugaljesing/).
### Features:
- Wirelessly Control the tracker from your phone/laptop by connecting to a webpage
- Supports AP (Access Point) and STA (Station) mode
 -- AP  : The ESP32 will create a wifi network which you can connect to
 -- STA : The ESP32 connects to an existing wifi network specified by you, Ex: phone hotspot. (Not fully tested)
- Integrated intervalometer which can control your camera shutter, no need to buy extra hardware. Exposures can be controlled via the webpage
- USB port to power a Dew Heater
- Slewing supported at different speeds.

*If you would like to buy an assembled PCB, contact Ondra Gejdos in the discord server (Creator of the OGST). Alternatively, if you live in India contact me to buy the PCB.*

## Table of Contents
- [PCB](pcb/README.md)
- [Compiling](docs/compiling.md)


## Building guide

One can get the full kit from the the official store at [ogstartech.com](https://ogstartech.com/start) or can build the tracker itself based on the instructions given at [printables](https://www.printables.com/model/348574-og-star-tracker)

## Firmware

The firmware for the PCB is provided in this repository and can be compiled and flashed with the given [instructions](docs/compiling.md).
To control the PCB the tracker will create its own wifi access point with the following default credentials:

```
ssid: OG Star Tracker
password: password123
```

After connection was successful the tracker to actually control it access the ***www.tracker.com** in your browser. The ESP32 provides a webserver for convenient controlling.

## App

If the webserver is not enough there is a app available to improve the accessibility even further.
Check out https://github.com/OndraGejdos/OG-star-tracker-App for more details.