# IoT-Based Home Automation Using ESP32

## Overview
This project implements an IoT-based home automation system using the ESP32 microcontroller to control electrical appliances through Wi-Fi, voice commands, physical push buttons, and an IR remote control.

The system integrates **Sinric Pro** for cloud-based appliance control, allowing users to operate connected devices through a compatible smartphone app and supported voice assistants.

## Features
- **Wi-Fi Control:** Control appliances remotely through Sinric Pro.
- **Voice Control:** Operate appliances using a compatible voice assistant integrated with Sinric Pro.
- **Manual Control:** Switch appliances using physical push buttons.
- **IR Remote Control:** Control appliances using an infrared remote.
- **Multi-Appliance Switching:** Independently control up to four relay channels.
- **ESP32-Based Control:** Process commands and control relay outputs using embedded C++.

## Components Required
- ESP32 development board
- 4-channel relay module
- Four push buttons
- IR receiver module (e.g., VS1838B)
- Compatible IR remote control
- Suitable power supply
- Jumper wires and connecting hardware
- Wi-Fi router or hotspot

## Software and Technologies
- Arduino IDE
- Embedded C++
- ESP32
- Wi-Fi communication
- Sinric Pro IoT platform
- Arduino-IRremote library

## Pin Connections

| Component | ESP32 GPIO |
|---|---|
| Relay 1 — Light | GPIO 16 |
| Relay 2 — Fan | GPIO 17 |
| Relay 3 — Socket | GPIO 18 |
| Relay 4 — Appliance 4 | GPIO 19 |
| Push Button 1 | GPIO 25 |
| Push Button 2 | GPIO 26 |
| Push Button 3 | GPIO 27 |
| Push Button 4 | GPIO 32 |
| IR Receiver OUT | GPIO 23 |

Connect each push button between its assigned GPIO pin and GND. Verify the relay module's logic level and input polarity before connecting it.

## Working Principle
The ESP32 acts as the main controller. It connects to Wi-Fi and communicates with Sinric Pro to receive appliance control commands. The ESP32 processes commands and switches the appropriate relay channel.

Physical push buttons provide local manual control, while the IR receiver decodes commands from an infrared remote. Voice control is available through a compatible voice assistant integrated with Sinric Pro.

## Setup Instructions
1. Install Arduino IDE and the ESP32 board package.
2. Install the required `SinricPro` and `IRremote` libraries.
3. Create an account on the Sinric Pro platform.
4. Create four Switch devices and obtain the App Key, App Secret, and device IDs.
5. Update the Wi-Fi credentials and Sinric Pro configuration in the Arduino sketch.
6. Upload the code to the ESP32.
7. Read the actual IR remote codes using Serial Monitor and update the sketch.
8. Test the buttons, IR remote, mobile app, and voice assistant integration.

## Applications
- Smart homes and residential automation
- Remote appliance switching
- Convenient local and wireless control
- Embedded systems and IoT learning projects

## Safety Precautions
- Never connect AC mains voltage directly to ESP32 GPIO pins.
- Use appropriately rated relays, proper electrical isolation, fuses, and an insulated enclosure.
- Test the system with low-voltage loads before connecting mains-powered appliances.
