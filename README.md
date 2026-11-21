# 💧 Automatic Water Level Monitoring and Pump Control System Using Arduino

## 📌 Project Overview

The **Automatic Water Level Monitoring and Pump Control System** is an Arduino-based automation project designed to monitor water levels in a tank and automatically control the water pump to prevent overflow and improve water management.

In many households, industries, and agricultural applications, water tanks are filled manually or monitored periodically. This can result in water wastage due to tank overflow, unnecessary pump operation, and inefficient water management.

This project uses a water level sensor connected to an Arduino to continuously monitor the water level. Based on the sensor readings, the system identifies three conditions: LOW, MEDIUM, and HIGH.

Three LEDs indicate the current water level, while a buzzer provides an alert when the tank reaches a high level. A relay module automatically controls the water pump, switching it OFF when the water reaches the high-level threshold.

The system reduces manual monitoring and provides a simple, cost-effective solution for automated water management.

## 🎯 Problem Statement

Manual water tank monitoring can lead to:
- Water wastage due to tank overflow.
- Unnecessary electricity consumption from continuous pump operation.
- Dependence on manual supervision.
- Difficulty in identifying the current water level.
- Inefficient water management in residential, agricultural, and industrial environments.

## 💡 Proposed Solution

The proposed system uses an Arduino-based water level monitoring mechanism with automatic pump control.

The system:
- Continuously measures the water level using an analog water level sensor.
- Categorizes the water level into LOW, MEDIUM, and HIGH.
- Displays the water status using three LEDs.
- Activates a buzzer when the water reaches a high level.
- Automatically switches OFF the water pump using a relay when the tank reaches the high-level threshold.
- Switches the pump ON again when the water level falls below the high-level threshold.

## ⚙️ Hardware Components

| Component | Purpose |
|---|---|
| Arduino Uno | Main microcontroller |
| Water Level Sensor | Detects water level |
| Green LED | Indicates low water level |
| Yellow LED | Indicates medium water level |
| Red LED | Indicates high water level |
| Buzzer | Provides an audible warning |
| Relay Module | Controls the water pump |
| DC Water Pump | Pumps water into the tank |
| Breadboard and Jumper Wires | Circuit connections |

## 🔌 Pin Configuration

| Component | Arduino Pin |
|---|---|
| Water Level Sensor | A0 |
| Green LED | Digital Pin 2 |
| Yellow LED | Digital Pin 3 |
| Red LED | Digital Pin 4 |
| Buzzer | Digital Pin 5 |
| Relay Module | Digital Pin 6 |

## 🔄 Working Principle

1. **Water Level Detection:** The water level sensor continuously detects the amount of water in the tank and sends an analog signal to the Arduino.

2. **Data Processing:** Arduino reads the analog sensor value and compares it with predefined threshold values.

3. **Low-Level Indication:** When the sensor value is below 300, the green LED glows, indicating a low water level. The buzzer remains OFF and the pump continues operating.

4. **Medium-Level Indication:** When the sensor value is between 300 and 699, the yellow LED glows, indicating a medium water level. The pump continues operating.

5. **High-Level Detection:** When the sensor value reaches 700 or above, the red LED glows and the buzzer is activated to indicate that the tank has reached a high water level.

6. **Automatic Pump Control:** The relay switches OFF the water pump when the high-level threshold is reached. When the water level decreases below the threshold, the pump automatically switches ON again.

7. **Serial Monitoring:** The measured water level is continuously displayed through the Arduino Serial Monitor for observation and testing.

## 🚦 Water Level Conditions

| Water Sensor Reading | Water Level | LED Indication | Buzzer | Pump |
|---|---|---|---|---|
| Below 300 | LOW | 🟢 Green | OFF | ON |
| 300–699 | MEDIUM | 🟡 Yellow | OFF | ON |
| 700 and above | HIGH | 🔴 Red | ON | OFF |

**Note:** The threshold values are prototype settings and should be calibrated according to the water level sensor, tank dimensions, and installation conditions.

## 📟 Serial Monitor Output

The Arduino continuously displays the sensor readings in the Serial Monitor.

Example:

```text
Water Level: 150
Water Level: 420
Water Level: 650
Water Level: 750
```

When the sensor reading reaches 700 or above, the system activates the buzzer and switches OFF the pump through the relay.

## 🛠️ Software and Technologies Used

- Arduino IDE
- Embedded C / Arduino Programming
- Analog Sensor Interfacing
- Digital Input and Output
- Relay-Based Automation
- Serial Communication
- Threshold-Based Control Logic

## 🌍 Applications

- Residential overhead water tanks
- Agricultural irrigation systems
- Industrial water storage tanks
- Water supply management systems
- Rainwater harvesting storage units
- Automated water pumping systems
- Commercial buildings and institutions

## 🚀 Innovation and Key Features

- **Automatic Pump Control:** Controls the water pump without requiring manual intervention.
- **Three-Level Monitoring:** Identifies low, medium, and high water levels.
- **Overflow Prevention:** Automatically stops the pump when the high-level threshold is reached.
- **Audio-Visual Alerts:** Uses LEDs and a buzzer to indicate water conditions.
- **Energy Efficiency:** Helps avoid unnecessary pump operation after the tank reaches the high-level threshold.
- **Low-Cost Automation:** Uses affordable electronic components and a simple control mechanism.

## 🔮 Future Enhancements

- Integrate ESP32 or ESP8266 for Wi-Fi-based water level monitoring.
- Connect the system to a Blynk or cloud dashboard.
- Send mobile notifications when the tank reaches critical levels.
- Add multiple tank monitoring capabilities.
- Implement water consumption tracking.
- Add automatic dry-run protection for the pump.
- Introduce hysteresis to prevent frequent relay switching near the threshold.

## 📌 Conclusion

The Automatic Water Level Monitoring and Pump Control System demonstrates how microcontrollers, sensors, and relay-based automation can be used to improve water management. By continuously monitoring water levels and automatically controlling the pump, the system helps prevent tank overflow, reduce water wastage, and minimize manual intervention.

The project provides a simple and cost-effective prototype that can be further developed into an IoT-enabled smart water management system.

## 👩‍💻 Project Category

**Domain:** Internet of Things (IoT) and Automation  
**Platform:** Arduino  
**Application:** Smart Water Management and Automatic Pump Control
