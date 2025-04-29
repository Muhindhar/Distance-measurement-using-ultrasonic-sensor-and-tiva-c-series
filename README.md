# 🧭 Ultrasonic Distance Measurement using Tiva C (TM4C123G)

This project demonstrates how to use the **HC-SR04 ultrasonic sensor** with the **Tiva C Series LaunchPad (TM4C123G)** to measure distances in real time and display them via UART (serial communication).

---

## 📌 Features
- Real-time distance measurement using HC-SR04
- UART-based serial output for live data monitoring
- Compatible with Keil uVision and TivaWare libraries
- Voltage-safe connection for ECHO pin using resistor divider

---

## ⚙️ Hardware Used
| Component | Description |
|----------|-------------|
| TM4C123G LaunchPad | Main microcontroller board |
| HC-SR04 | Ultrasonic distance sensor |
| 1 kΩ Resistor | For voltage divider |
| 2 kΩ Resistor | For voltage divider |
| Jumper Wires | For connections |
| Breadboard | For prototyping |

---

## 🔌 Wiring Diagram

![Ultrasonic Sensor to Tiva C Wiring](Schematics/ultrasonic_sensor_tivac_wiring.png)

| HC-SR04 Pin | Tiva C Pin | Description |
|-------------|------------|-------------|
| VCC         | 5V         | Power Supply |
| GND         | GND        | Ground |
| TRIG        | PE4        | Trigger Output |
| ECHO        | PE5        | Echo Input (via voltage divider) |

> **Note:** ECHO pin outputs 5V, but TM4C123G supports 3.3V logic. Use a voltage divider (2kΩ + 1kΩ) to step down safely.

---

## 🖥️ Output Example (UART Serial Monitor)
```bash
Distance: 22 cm
Distance: 23 cm
Distance: 21 cm
