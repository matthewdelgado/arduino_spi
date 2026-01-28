# MCP4131 SPI Digital Potentiometer Example

This project demonstrates how to control an **MCP4131 digital potentiometer** using an **Arduino** and the SPI interface.  
It writes wiper values to the potentiometer and reads the corresponding analog input from pin `A0`.

## Overview

The MCP4131 is a **single-channel 7-bit digital potentiometer** controlled via SPI.  
This example code sweeps the wiper from 0 to 128 (full range), updates the potentiometer, and reads an analog input to observe the voltage response.

---

## Hardware Required

- Arduino (Uno, Mega, or compatible)
- MCP4131 digital potentiometer
- Breadboard and jumper wires
- Optional: resistor or voltage divider for testing

---

## Circuit Connections

| MCP4131 Pin | Arduino Pin |
|-------------|-------------|
| CS / SS     | 10          |
| SCK         | 13          |
| SDI / MOSI  | 11          |
| VDD         | 5V          |
| VSS / GND   | GND         |
| PW0 / PW1   | Optional analog output for testing |

Make sure **pin 10** on the Arduino is configured as the **SS (Slave Select)** pin in your code.

---

## Installation

1. Connect your Arduino to your computer via USB.
2. Open the Arduino IDE.
3. Copy the code into a new sketch.
4. Select your board and port under **Tools → Board** and **Tools → Port**.
5. Click **Upload**.

---

## Usage

After uploading:

1. Open the **Serial Monitor** in the Arduino IDE (baud rate 9600).
2. The wiper will increment from 0 to 128.
3. Each new wiper value will be written to the MCP4131.
4. Analog readings from pin `A0` will be printed every second.
