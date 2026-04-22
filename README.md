# VCU — Vehicle Control Unit

![PCB](https://img.shields.io/badge/PCB-Custom-blue)
![CAN](https://img.shields.io/badge/Comm-CAN%20%7C%20UART-teal)
![Status](https://img.shields.io/badge/Status-Active-green)

The **VCU (Vehicle Control Unit)** is a custom-designed PCB built for embedded vehicle systems. 
It integrates motor control, multi-protocol communication, real-time data logging, and wireless 
telemetry into a single compact board — purpose-built for electric vehicle applications where 
reliability and real-time performance are critical.

## Features

- **Motor Control** — Drive and regulation of motor output with configurable control logic
- **CAN Bus** — Robust vehicle network communication via CAN protocol
- **UART** — Serial communication for peripherals, debugging, and configuration
- **Data Logging** — Onboard logging of sensor and system data for post-analysis
- **Telemetry** — Real-time wireless data transmission via ESP32 for live monitoring and diagnostics
- **Remote Shutdown Circuit** — Remotely activated shutdown that cuts current to the AIRs (Accumulator 
  Isolation Relays), compliant with EV5.6, including pre-charge circuitry management

## Microcontrollers

The VCU uses a dual-MCU architecture:

| MCU | Role |
|-----|------|
| **Teensy** | Real-time motor control, CAN communication, and data logging |
| **ESP32** | Wireless telemetry, remote shutdown signalling, and UART interfacing |

## Hardware

| Parameter | Details |
|-----------|---------|
| Form factor | Custom PCB |
| MCUs | Teensy + ESP32 |
| Communication | CAN bus, UART |
| Telemetry | Wi-Fi / Bluetooth via ESP32 |
| Safety | Remote shutdown circuit — cuts AIR drive current (EV5.6 compliant) |
| HV Management | Pre-charge circuitry for safe accumulator connection |

## Safety — Shutdown & Pre-charge

The VCU implements a **remotely activated shutdown circuit** in accordance with **EV5.6**. 
When triggered, it cuts the current driving the Accumulator Isolation Relays (AIRs), 
disconnecting the high-voltage accumulator from the powertrain.

Pre-charge circuitry is also managed by the VCU to safely ramp up bus voltage before 
the main AIRs close, protecting inverter capacitors and downstream HV components from 
inrush current damage.

## Getting Started

PCB design files, schematics, and BOM are available in the `/hardware` directory. 
Firmware for both the Teensy and ESP32 can be found in `/firmware`.
