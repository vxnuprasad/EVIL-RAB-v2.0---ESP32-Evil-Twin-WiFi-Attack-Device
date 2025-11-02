# EVIL RAB v2.0 - ESP32 Evil Twin WiFi Attack Device

<p align="center">
<a href="#"><img title="Poster" src="Poster.png"></a>
</p>
<p align="center">
<a href="https://github.com/vxnuprasad"><img title="Author" src="https://img.shields.io/badge/Author-Vishnu-yellow.svg?style=for-the-badge&logo=github"></a>
<a href="[https://interncrafters.netlify.app/](https://vxnuprasad.github.io/)"><img title="Website" src="https://img.shields.io/badge/Website-vxnuprasad-green.svg?style=for-the-badge&logo=sites"></a>
</p>

## Disclaimer

This project is strictly for educational and authorized penetration testing purposes only. Wireless jamming devices are illegal in many countries when used without permission and can disrupt critical communications. I assume no responsibility for misuse or damage caused by this device. Use responsibly and legally, in controlled test environments only.

## Introduction

EVIL RAB v2.0 is a compact, ESP32-based evil twin WiFi attack device designed for educational and security research purposes. Featuring support for two types of 0.96 inch OLED displays (4-pin and 7-pin variants), it enables users to learn about and test against one of the most common WiFi attack vectors to better understand and improve wireless security.


## What is an Evil Twin Attack?

An evil twin attack tricks users into connecting to a fake WiFi access point that closely mimics a legitimate network (same SSID). The attacker sets up the rogue access point and uses methods like stronger signal broadcasting and deauthentication of clients on the real network to make victims connect to the fake one. Once connected, the attacker can intercept and manipulate the victim's traffic, capturing sensitive data like login credentials through fake captive portals or direct monitoring. This is a form of a man-in-the-middle attack and poses a significant threat especially in public WiFi environments like cafes, airports, and libraries.


## Required Modules and Hardware

- ESP32 development board (ESP32 devkit v1 board Or ESP WROOM 32 MCU Module recommended)
- 0.96 inch OLED display:
  - 4-pin variant (I2C: GND, VCC, SDA, SCL)
  - 7-pin variant (SPI interface: GND, VCC, D0/SCK, D1/MOSI, RES, DC, CS)
- Jumper wires and breadboard or custom PCB for circuit assembly
- USB connection cable to flash and power the ESP32

## Circuit and Module Details

EVIL RAB v2.0 uses an ESP32 connected to one of the two supported OLED display types.


| ESP32 Pin | OLED 4 Pin | Description       |
| --------- | ---------- | ----------------- |
| GND       | GND        | Ground            |
| 3.3V      | VCC        | Power supply 3.3V |
| GPIO 21   | SDA        | I2C Data Line     |
| GPIO 22   | SCL        | I2C Clock Line    |

| ESP32 Pin | OLED 7 Pin | Description             |
| --------- | ---------- | ----------------------- |
| GND       | GND        | Ground                  |
| 3.3V      | VCC        | Power supply 3.3V       |
| GPIO 18   | D0         | SPI Clock               |
| GPIO 23   | D1         | SPI Master Out Slave In |
| GPIO 16   | RES        | Reset                   |
| GPIO 17   | DC         | Data/Command control    |
| GPIO 5    | CS         | Chip Select             |

### Module Specifications

- **ESP32**: Dual-core WiFi/Bluetooth microcontroller, 3.3V logic
- **0.96 inch OLED (4-pin)**: I2C, 128x64 resolution, pins: VCC, GND, SDA, SCL
- **0.96 inch OLED (7-pin)**: SPI interface, 128x64 resolution, pins: VCC, GND, D0 (SCK), D1 (MOSI), RES, DC, CS

---

## Flash Firmware Directly from Browser

Precompiled firmware binaries are available for easy flashing of EVIL RAB v2.0 Evil Twin attack device on 4-pin and 7-pin OLED displays.

Open this link in a Web Serial API supported browser (Google Chrome, Microsoft Edge):

[https://yourusername.github.io/EvilRAB-v2.0/web-flasher/](https://yourusername.github.io/EvilRAB-v2.0/web-flasher/)

### Available Firmware

- `evil_rab_4pin.bin` — Evil Twin attack firmware for 4-pin OLED display  
- `evil_rab_7pin.bin` — Evil Twin attack firmware for 7-pin OLED display  

### Flashing Instructions

1. Connect your ESP32 device to your computer via USB.  
2. Open the web flasher URL above in Chrome or Edge.  
3. Select the appropriate firmware file based on your OLED display type.  
4. Click "Flash" and wait for the upload to complete.  
5. Your device will reboot with the new firmware.


## Libraries Required

Make sure you have the following Arduino libraries installed:

- ESP_QRCode  
- ArduinoJson  
- NTPClient  
- AsyncWebServer  

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Find Me On:
[![LinkedIn](https://img.shields.io/badge/LinkedIn-VishnuPrasad-blue?style=for-the-badge&logo=LinkedIn)](https://www.linkedin.com/in/vxnuprasad)  
[![Instagram](https://img.shields.io/badge/IG-%40__.v.shnu-red?style=for-the-badge&logo=instagram)](https://www.instagram.com/__.v.shnu/)  

Thank you for using EVIL RAB v2.0 — advancing WiFi security research for a safer world.
