# Student Experience and Resume Documentation

This document explains the project as a student engineering experience and gives resume-ready language.

## Project Title

**FSAE Vehicle Data Acquisition System — Embedded C, Python, KiCad, MATLAB**

## Student Project Summary

I developed a custom data acquisition system for a Formula SAE vehicle to collect powertrain, electrical, and vehicle-dynamics data during real vehicle testing. The project involved sensor selection, signal conditioning, current sensing, PCB design, firmware development, serial communication, Python-based CSV logging, and validation through vehicle testing.

The system was designed to support low-cost and customizable data acquisition for a student racing team. Instead of relying on expensive commercial DAQ systems, I built a modular board that could acquire both traditional and custom vehicle parameters.

## What I Built

- Centralized DAQ hardware board
- Sensor signal conditioning circuits
- Differential op-amp current sensing stages
- Battery voltage measurement buffer
- Multiplexer-based ADC expansion
- Embedded C acquisition firmware
- Raspberry Pi Python logger
- CSV data processing workflow
- Track-test validation process

## Technical Skills Demonstrated

| Skill Area | Details |
|---|---|
| Embedded systems | ATmega328 firmware, serial communication, ADC acquisition |
| PCB design | KiCad schematic/layout, track-width planning, power routing |
| Analog circuits | Op-amp current sensing, voltage dividers, buffering, muxed acquisition |
| Automotive electronics | 12 V supply, sensor validation, transient protection, wiring harness interface |
| Python automation | CSV logging, data buffering, post-processing |
| MATLAB validation | Conversion equation verification and signal model checks |
| Vehicle testing | Real data logging during FSAE testing |

## Challenges Faced

### Limited ADC Channels

The controller had fewer analog pins than the number of sensors. I solved this by using 16-channel and 8-channel analog multiplexers.

### Mixed Voltage Levels

Different sensors required 12 V, 5 V, and 3.3 V. I created a power-stage architecture to distribute regulated voltages safely.

### Noisy Automotive Environment

Vehicle systems such as radiator fans, fuel pumps, ECU, and ignition-related loads can create electrical noise. I handled this using current monitoring, buffering, wider current paths, and validation logic.

### Data Reliability

The firmware needed to avoid logging invalid data from disconnected or faulty sensors. I implemented safety checks based on voltage baseline and current consumption.

### Track Testing

The system had to work during high vibration, temperature variation, and fast vehicle maneuvers. It was validated over 115 km of real vehicle operation.

## Resume Bullets

```text
FSAE Vehicle Data Acquisition System — Embedded C, Python, KiCad, MATLAB
• Designed a custom FSAE data acquisition system integrating powertrain, vehicle-dynamics, current, voltage, and thermal sensors.
• Developed embedded C firmware for ATmega328-based acquisition with battery safety checks, sensor fault detection, and muxed ADC sampling.
• Built Python-based Raspberry Pi logger to capture serial data into CSV files at 67 Hz per parameter over a 9600-baud link.
• Designed PCB in KiCad with op-amp current sensing, voltage buffering, analog multiplexing, regulated power rails, and transient protection.
• Validated the system over 115 km of vehicle testing across 76 driver/track combinations with documented sensor error margins.
```

## Short Interview Explanation

This project was a custom embedded electronics and data acquisition platform for an FSAE vehicle. I worked on sensor selection, signal conditioning, current sensing, PCB design, firmware, Python logging, and real vehicle validation. The system collected both powertrain and vehicle-dynamics data such as RPM, damper travel, IMU data, coolant temperature, fan current, fuel pump current, battery voltage, and throttle position. The data was logged to CSV using a Raspberry Pi and validated over 115 km of testing.

## What I Learned

- How to design an embedded DAQ system around real sensor constraints
- How to handle multiple voltage domains in an automotive environment
- How to design current sensing for both mA-level sensors and A-level loads
- How to convert raw ADC values into physical parameters
- How to build a Python logging pipeline for real vehicle data
- How to validate sensor accuracy through bench and vehicle testing
- How DAQ data supports driver training, drivetrain tuning, and vehicle optimization
