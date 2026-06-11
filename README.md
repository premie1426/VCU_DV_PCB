# VCU — Vehicle Control Unit

![PCB](https://img.shields.io/badge/PCB-Custom-blue)
![Comm](https://img.shields.io/badge/Comm-CAN%20%7C%20UART%20%7C%20SPI-teal)

The VCU (Vehicle Control Unit) is a custom-designed PCB built for embedded vehicle systems. 
It integrates motor control, multi-protocol communication, real-time data logging, and wireless 
telemetry into a single compact board.

## Features

- **Motor Control** — Drive and regulation of motor output with configurable control logic
- **CAN Bus** — CAN protocol for communicating with other modules
- **UART** — Serial communication for peripherals, debugging, and configuration
- **SPI** — SPI Interface for Dashboard Display Communication
- **Data Logging** — Onboard logging of sensor and system data for post-analysis
- **Telemetry** — Real-time wireless data transmission via ESP32 for live monitoring and diagnostics
- **Remote Shutdown Circuit** — Remotely activated shutdown that cuts current to the AIRs (Accumulator 
  Isolation Relays), and pre-charge circuitry

## Hardware

| Parameter | Details |
|-----------|---------|
| Form factor | Custom PCB |
| MCUs | Teensy + ESP32 |
| Communication | CAN bus, UART, SPI |
| Telemetry | Wi-Fi / Bluetooth via ESP32 |
| Safety | Remote shutdown circuit — cuts AIR drive current (EV5.6 compliant) |
| PCB layers | 2-layer |
| Board dimensions | 80mm × 84mm |
| Connectors | Erni Maxibridge |
| Data storage | MicroSD on the Teensy 4.1 |

## PCB

<p align="center">
  <img src="Images/PCB.png" alt="VCU PCB Top" width="45%"/>
  &nbsp;&nbsp;
</p>

<p align="center">
  <em>VCU rev1.0</em>
</p>

## 3D View

<p align="center">
  <img src="Images/3D-Front.png" alt="VCU 3D View Top" width="45%"/>
  &nbsp;&nbsp;
  <img src="Images/3D-Back.png" alt="VCU 3D View Bottom" width="45%"/>
</p>

<p align="center">
  <em>VCU rev1.0 — 3D render from Altium</em>
</p>


