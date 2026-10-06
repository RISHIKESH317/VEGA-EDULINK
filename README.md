# VEGA-EDULINK: VEGA ARIES V2 & V3 Student Learning & Development Kit

A dedicated web-based learning, development, and programming platform for **VEGA RISC-V microcontrollers**, supporting VEGA ARIES V2, V3 series, and other supported VEGA boards. The platform combines learning resources, documentation, coding, compilation, firmware generation, hardware programming, serial monitoring, and hands-on experimentation.

## Overview

VEGA-EDULINK is designed to provide students with a complete environment for learning and developing applications using **VEGA RISC-V microcontrollers**.

A key feature of the platform is that the **VEGA RISC-V toolchain is integrated directly into the website**, allowing source code to be compiled and firmware to be generated within the VEGA-EDULINK environment.

By using the integrated VEGA toolchain and the corresponding board configuration, the platform can support compilation and firmware generation for **VEGA ARIES V2, V3 series, and other supported VEGA boards**.

The platform integrates:

- VEGA RISC-V learning resources and documentation
- Web-based IDE for C/C++ development
- Integrated VEGA RISC-V toolchain
- Backend compilation and firmware generation
- Integrated Serial Monitor for real-time serial output and debugging
- Direct cable-based programming
- Wireless OTA (Over-The-Air) programming
- ESP32-S3 based wireless programming gateway
- Wi-Fi Manager for network configuration
- VEGA ARIES V2 trainer kits for practical experiments
- GPIO and peripheral interfacing
- Communication protocol experiments
- Custom hardware integration for VEGA ARIES V2
- Support for VEGA ARIES V2, V3 series, and other supported VEGA boards

### Project Workflow

**Learn → Code → Compile → Generate Firmware → Program → Monitor → Experiment**

---

# Project Overview

The complete project integrates the **VEGA-EDULINK Web IDE, integrated VEGA toolchain, Serial Monitor, ESP32-S3 wireless programming gateway, VEGA ARIES V2 hardware, trainer kits, and custom carrier PCB**.

The website provides the common development environment and integrated VEGA toolchain, while the current trainer kit, custom carrier PCB, and OTA programming gateway are demonstrated using the VEGA ARIES V2.

**Project Resources:**

- [View Overall Project Setup](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/project_overview.jpeg)
- [View OTA Connection](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/OTA-Connection.jpeg)
- [View A3 Documentation](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/A3_DOCUMENTATION)
- [View Trainer Kits](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/TRAINER_KITS)
- [View Custom Carrier PCB](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/CARRIER_PCB.jpeg)

---

# Key Features

## 1. Web-Based Development Platform

The Web IDE provides a dedicated environment for developing applications for VEGA RISC-V microcontrollers.

The **VEGA RISC-V toolchain is integrated into the website itself**, eliminating the need for users to separately configure the compiler toolchain for the supported VEGA targets.

The development flow is:

**C/C++ Source Code → Build → Compile → Link → Generate `firmware.bin` → Program VEGA Board**

The backend build environment uses the integrated VEGA RISC-V toolchain to process the source code and generate the firmware binary required for the selected VEGA board.

The Web IDE also includes an **integrated Serial Monitor** for viewing real-time serial output during program execution and debugging.

## 2. VEGA ARIES V2 & V3 Support

VEGA-EDULINK is designed to support the **VEGA ARIES V2, V3 series, and other supported VEGA RISC-V boards**.

The integrated VEGA toolchain allows the Web IDE to compile source code according to the selected VEGA target and generate the corresponding firmware.

This provides a common development environment where students can learn, develop, compile, and generate firmware for different VEGA boards without changing to a separate development platform.

## 3. VEGA ARIES V2 Student Learning Kit

The trainer kits provide a practical platform for experimenting with the VEGA ARIES V2 microcontroller.

They support experiments involving:

- GPIO
- LEDs and switches
- Sensors and actuators
- Display interfacing
- UART communication
- I²C communication
- SPI communication
- Other peripheral experiments

The kits connect the concepts learned through the web platform with real hardware experiments.

## 4. Custom VEGA ARIES V2 Hardware

As part of the project, a custom schematic symbol and PCB footprint for the **VEGA ARIES V2** were created and integrated into the hardware design.

A custom carrier PCB was developed to provide the required interfaces and connections for the VEGA ARIES V2 and project peripherals.

---

# Project Documentation

The project was documented through three A3 sheets covering the overall system, GPIO trainer kit, and communication-protocol development kit.

### A3 Documentation

- [A3 Sheet – Project Overview](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/A3_DOCUMENTATION/overview.jpeg)
- [A3 Sheet – GPIO Trainer Kit](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/A3_DOCUMENTATION/GPIO_kit.jpeg)
- [A3 Sheet – Communication Protocol Kit](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/A3_DOCUMENTATION/PROTOCOL_kit.jpeg)

---

# VEGA ARIES V2 Trainer Kits

The trainer kits provide a hands-on platform for experimenting with GPIO, peripherals, sensors, actuators, and communication protocols using the VEGA ARIES V2.

### Trainer Kits

- [GPIO Trainer Kit](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/TRAINER_KITS/Trainer_kit_1_GPIOS.jpeg)
- [GPIO and Communication Protocol Trainer Kit](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/TRAINER_KITS/Trainer_kit_2_protocols.jpeg)

---

# Custom Carrier PCB

A custom carrier PCB was designed to integrate the **VEGA ARIES V2** into the project hardware and support the required interfaces and connections.

As part of the hardware development, a custom schematic symbol and PCB footprint for the VEGA ARIES V2 were also created.

- [View Custom VEGA ARIES V2 Carrier PCB](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/CARRIER_PCB.jpeg)

---

# Programming Methods

VEGA-EDULINK supports both wired and wireless firmware programming.

## Cable Programming

The firmware generated by the Web IDE can be programmed into the selected VEGA board using a wired programming interface.

**Web IDE → `firmware.bin` → Cable → VEGA Board → Program → Execute**

The exact programming interface and boot configuration depend on the selected VEGA board.

## OTA Programming

For wireless programming, an **ESP32-S3** is used as a wireless programming gateway in the current OTA implementation.

**Web IDE → Wi-Fi → ESP32-S3 → USB/UART → VEGA ARIES V2**

The ESP32-S3 receives the generated firmware binary through Wi-Fi, stores it temporarily in LittleFS, and transfers it to the VEGA ARIES V2 for programming.

### OTA Connection

The OTA programming connection between the Web IDE, ESP32-S3, and VEGA ARIES V2 is shown below.

![OTA Connection](https://github.com/RISHIKESH317/VEGA-EDULINK/blob/main/DOCS/OTA-Connection.jpeg)

---

# Serial Monitor

The VEGA-EDULINK Web IDE includes an integrated **Serial Monitor** for observing serial communication from supported VEGA boards.

It allows users to:

- View real-time serial output
- Monitor program execution
- Debug embedded applications
- Observe messages generated by the VEGA board

This provides a single development environment for writing code, programming the board, and monitoring its execution.

---

# ESP32-S3 Wireless Programming Gateway

The ESP32-S3 provides the wireless connection between the Web IDE and the VEGA ARIES V2 during the current OTA programming implementation.

The gateway performs the following functions:

- Wi-Fi initialization
- Wi-Fi network configuration
- Wi-Fi Manager operation
- Firmware file reception
- Temporary firmware storage using LittleFS
- USB Host communication
- USB-UART communication with VEGA ARIES V2
- Firmware transfer using XMODEM-CRC
- Packet validation and retry handling
- Programming status and error handling

## Wi-Fi Manager

The Wi-Fi Manager allows the ESP32-S3 to be configured with the required Wi-Fi credentials.

When valid credentials are not available, the ESP32-S3 provides a configuration interface where the user can select a network and enter the password.

The configured credentials are stored in LittleFS and used for subsequent connections.

---

# System Architecture

The complete system consists of the following major components:

1. VEGA-EDULINK Web Platform
2. Integrated VEGA RISC-V Toolchain
3. Backend Build Environment
4. Integrated Serial Monitor
5. ESP32-S3 Wireless Programming Gateway
6. VEGA ARIES V2 / V3 and other supported VEGA boards
7. VEGA ARIES V2 Trainer Kits
8. Custom VEGA ARIES V2 Carrier PCB
9. Connected peripherals and communication interfaces

### Overall Development Flow

**Source Code → Web IDE → Integrated VEGA Toolchain → Backend Build → `firmware.bin` → Cable / Wi-Fi → VEGA Board → Flash → Execute → Serial Monitor**

### Current OTA Implementation

**Web IDE → Wi-Fi → ESP32-S3 → USB/UART → VEGA ARIES V2 → Flash → Execute → Serial Monitor**

The ESP32-S3 acts as the bridge between the web-based development environment and the VEGA ARIES V2 hardware during the current OTA implementation.

---

# Algorithms

## Algorithm 1: Source Code to Firmware Generation

1. Open the VEGA-EDULINK Web IDE.
2. Select the required VEGA target board.
3. Enter the C/C++ source code.
4. Click the **BUILD** button to start the firmware generation process.
5. Send the source code from the Web IDE to the backend build environment.
6. Initialize the integrated VEGA RISC-V compiler and required build tools.
7. Compile the source code into the required object files.
8. Link the object files to generate the firmware ELF file.
9. Convert the ELF file into the required `firmware.bin` binary image.
10. Verify the generated firmware binary and report the build result.
11. Display **BUILD SUCCESS** when firmware generation is completed.
12. Provide the generated `firmware.bin` for hardware programming.

The selected VEGA board determines the required board configuration and compilation parameters.

## Algorithm 2: Wireless Firmware Delivery and Programming

1. Initialize the ESP32-S3 Wi-Fi, LittleFS, USB Host, and programming interfaces.
2. Check whether valid Wi-Fi credentials are available.
3. Start the Wi-Fi Manager when valid credentials are unavailable.
4. Connect to the configured Wi-Fi network and store the credentials in LittleFS.
5. Receive the generated `firmware.bin` through the ESP32-S3 web interface.
6. Temporarily store the firmware binary in LittleFS.
7. Initialize the communication interface between the ESP32-S3 and VEGA ARIES V2.
8. Detect the VEGA ARIES V2 and enter the required bootloader programming mode.
9. Transfer the firmware using XMODEM-CRC with packet validation and retry handling.
10. Verify the programming result.
11. Reset the VEGA ARIES V2 and complete the operation.

## Algorithm 3: VEGA ARIES V2 Firmware Programming

The following describes the current VEGA ARIES V2 hardware programming implementation.

1. Check the BOOT_SEL/J12 configuration of the VEGA ARIES V2.
2. Select UART Boot Mode when UART-based programming is required.
3. Initialize UART0 and establish communication with the VEGA bootloader.
4. Transfer the firmware using the XMODEM-CRC protocol.
5. Validate the received firmware packets and handle transfer errors.
6. Select SPI Flash Mode when direct flash programming is required.
7. Initialize SPI3 and access the AT25SF161 SPI Flash.
8. Program the application image into the designated 256 KB application region.
9. Verify the programmed firmware and confirm successful programming.
10. Reset the VEGA ARIES V2 and execute the programmed application.

The programming sequence for V3 series and other VEGA boards depends on their respective bootloader, flash configuration, and programming interface.

---

# Firmware Transfer

The OTA programming process uses the ESP32-S3 to receive and transfer the generated firmware for the current VEGA ARIES V2 OTA implementation.

The basic sequence is:

**`firmware.bin` → Wi-Fi → ESP32-S3 → LittleFS → USB/UART → XMODEM-CRC → VEGA ARIES V2 → Flash → Run**

XMODEM-CRC is used for reliable firmware transfer by providing packet-based transmission, error detection, and retry handling.

---

# Hardware and Software

## Hardware

- VEGA ARIES V2
- VEGA V3 series and other supported VEGA boards
- ESP32-S3
- VEGA ARIES V2 Trainer Kits
- Custom VEGA ARIES V2 carrier PCB
- USB/UART interface
- Sensors, displays, actuators, and other peripherals

## Software

- VEGA-EDULINK Web IDE
- Integrated VEGA RISC-V toolchain
- Integrated Serial Monitor
- C/C++ development environment
- Backend build environment
- ESP32-S3 firmware
- Wi-Fi Manager
- LittleFS
- XMODEM-CRC firmware transfer
- VEGA board programming interface

---

# Repository Structure

```text
vega-aries-v2-development-kit/
│
├── FIRMWARE/
│   └── Firmware source files and programming-related files
│
├── DOCS/
│   │
│   ├── A3_DOCUMENTATION/
│   │   ├── overview.jpeg
│   │   ├── GPIO_kit.jpeg
│   │   └── PROTOCOL_kit.jpeg
│   │
│   ├── TRAINER_KITS/
│   │   ├── Trainer_kit_1_GPIOS.jpeg
│   │   └── Trainer_kit_2_protocols.jpeg
│   │
│   ├── CARRIER_PCB.jpeg
│   ├── OTA-Connection.jpeg
│   └── project_overview.jpeg
│
└── README.md
