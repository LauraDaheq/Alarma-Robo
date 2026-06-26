# Anti-Theft Alarm System 🚨

An Arduino-based anti-theft alarm system that uses an **HC-SR04 ultrasonic sensor** to detect nearby objects and trigger an audible alarm.

## Project Description

This project implements a simple anti-theft alarm using an **Arduino Uno** and an **HC-SR04 ultrasonic distance sensor**. The system continuously measures the distance to nearby objects. When an object or person is detected within **10 cm**, a buzzer is activated for **5 seconds** as an alarm.

## Features

- ✅ Real-time distance measurement
- ✅ Motion and proximity detection
- ✅ Automatic alarm activation
- ✅ Audible buzzer alert (1000 Hz)
- ✅ Adjustable detection threshold
- ✅ Easy-to-build circuit

## Components Used

- **Arduino Uno** – Main microcontroller
- **HC-SR04 Ultrasonic Sensor** – Distance measurement
- **Piezo Buzzer** – Audible alarm
- **Breadboard** – Circuit assembly
- **Jumper Wires** – Electrical connections
- **Resistors and Capacitors** – As required

## Pin Configuration

| Component | Arduino Pin |
|-----------|-------------|
| HC-SR04 TRIG | 7 |
| HC-SR04 ECHO | 6 |
| Buzzer | 12 |

## How It Works

1. The ultrasonic sensor sends a **5-microsecond trigger pulse**.
2. It measures the time required for the echo to return.
3. The Arduino calculates the distance using the following equation:

```text
Distance = (Echo Duration / 2) × 0.0343 cm/µs
```

4. If the measured distance is **less than 10 cm**, the Arduino activates the buzzer at **1000 Hz** for **5 seconds**.
5. If the distance is greater than **10 cm**, the buzzer remains off.

## Circuit Diagram

Refer to the images included in this repository for the complete wiring diagram.

## Getting Started

1. Upload the `ALARMAROBO.ino` sketch to your **Arduino Uno**.
2. Assemble the circuit according to the provided schematic.
3. Power the Arduino board.
4. The system will automatically begin monitoring the surrounding area.
5. When an object approaches within **10 cm**, the alarm will sound.

## Technical Specifications

- Detection Threshold: **10 cm**
- Alarm Duration: **5 seconds**
- Buzzer Frequency: **1000 Hz**
- Speed of Sound Used: **343 m/s**
- Distance Formula:

```text
Distance = (Echo Duration / 2) × 0.0343
```

## Applications

- Home security systems
- Door and window intrusion detection
- Restricted area monitoring
- Smart home automation
- Educational embedded systems projects

## Future Improvements

- 📱 Add Bluetooth or Wi-Fi notifications
- 🔴 Include LED indicators for alarm status
- 🔑 Add keypad or RFID arming/disarming
- 📲 Send alerts to a mobile application
- 💾 Store alarm events in EEPROM or an SD card
- 📡 Integrate with IoT platforms

## Notes

- The speed of sound is assumed to be **343 m/s** at approximately **20°C**.
- The HC-SR04 sensor can measure distances from approximately **2 cm to 4 meters**.
- The detection threshold and alarm duration can be easily modified in the Arduino code.
- The buzzer frequency (**1000 Hz**) is fully configurable.

## Technologies

- Arduino Uno
- Arduino IDE
- Embedded Systems
- C/C++
- HC-SR04 Ultrasonic Sensor
- Distance Measurement
- Digital Electronics
- Security Systems
- Real-Time Monitoring
