# Pressure-Based Motor Control System

This project reads pressure values from an analog sensor (like a pressure transducer), and controls a DC motor using the Adafruit Motor Shield. Based on serial commands, the motor runs forward or backward until a specific pressure threshold is reached.

---

##  What It Does

- Measures pressure in mmHg from an analog sensor.
- Receives user input via the Serial Monitor:
  - `'1'` → Run motor **backward** until pressure is ≤ 0 mmHg
  - `'2'` → Run motor **forward** until pressure is ≥ 100 mmHg
  - `'0'` → Stop the motor immediately
- Displays pressure readings and runtime duration in the Serial Monitor.

---

##  Hardware Needed

-  Arduino Uno (or compatible board)
-  Adafruit Motor Shield (v1)
-  One or two DC motors (connected to M1 and M3)
-  Analog pressure sensor (e.g., MPX5010 or similar) connected to A0
-  Piezoelectric sensor 
-  Jumper wires, breadboard, power supply

---

##  Wiring Overview

| Component          | Arduino Connection     |
|-------------------|------------------------|
| Pressure sensor    | A0 (Analog Input)      |
| Piezo sensor       | A5 (Analog Input, unused) |
| Motor 1            | M1 on Motor Shield     |
| Motor 2 (optional) | M3 on Motor Shield     |

---


##  Calibration Note

const float calibrationOffset = 1.16;
