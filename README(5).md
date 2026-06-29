# FSAE Vehicle Data Acquisition System

A student-built embedded electronics project for acquiring, validating, and logging **Formula SAE vehicle powertrain and vehicle-dynamics data** during real track testing.

The system integrates analog sensors, digital sensors, power-stage monitoring, current sensing, an AVR-based microcontroller, Raspberry Pi data storage, Python CSV logging, KiCad PCB design, and MATLAB-based signal/model validation. The objective was to create a low-cost and customizable data acquisition platform that could support design validation, driver evaluation, fault detection, and vehicle performance tuning.

## Project Snapshot

| Category | Details |
|---|---|
| Project domain | FSAE data acquisition, embedded electronics, automotive sensing |
| Controller | ATmega328-based development board |
| Storage/logger | Raspberry Pi connected over serial/USB |
| PCB tool | KiCad |
| Validation tools | MATLAB, Python, bench testing, vehicle testing |
| Sampling behavior | 67 Hz per parameter, repeated every 15 ms with 1 ms inter-transfer delay |
| Serial baud rate | 9600 baud |
| Vehicle testing | 115 km of on-vehicle testing |
| Logged data sets | 76 driver/track combinations |
| Main outputs | CSV logs, sensor validation data, track-response plots, driver/FDR analysis |

## System Visual Overview

![DAQ system block diagram](images/01_daq_system_block_diagram.png)

The system was organized around sensor acquisition, power protection, current sensing, analog multiplexing, microcontroller conversion, and external data storage. The design was built to collect both **powertrain parameters** and **vehicle-dynamics parameters** while keeping the electronics modular and serviceable.

## Main Features

- Integrated damper travel, wheel speed, IMU, throttle position, coolant temperature, engine RPM, battery voltage, brake pressure, fan current, fuel pump current, ECU current, and auxiliary current channels.
- Designed a centralized DAQ board with regulated 12 V, 5 V, and 3.3 V supply support.
- Used differential op-amp current sensing to monitor sensor and actuator current consumption.
- Used analog multiplexers to expand available ADC channels while avoiding the delay and complexity of an external ADC.
- Implemented firmware safety checks for battery voltage, sensor pull-down state, and current range validation.
- Logged data to CSV using Raspberry Pi and Python over serial communication.
- Validated the data acquisition system through bench-level checks and 115 km of vehicle testing.

## Repository Structure

```text
FSAE-Vehicle-Data-Acquisition-System/
├── README.md
├── README_01_system_architecture.md
├── README_02_sensor_selection_and_signal_conditioning.md
├── README_03_firmware_and_logging_pipeline.md
├── README_04_pcb_design_and_power_integrity.md
├── README_05_testing_results_and_validation.md
├── README_06_student_experience.md
├── README_07_git_upload_guide.md
└── images/
    ├── 01_daq_system_block_diagram.png
    ├── 02_current_sensor_opamp_design.png
    ├── 03_current_sensor_configuration_table.png
    ├── 04_battery_voltage_buffer.png
    ├── 05_firmware_execution_flow.png
    ├── 06_damper_accel_rpm_track_data.png
    ├── 07_engine_temperature_fan_current.png
    ├── 08_final_drive_ratio_iteration.png
    └── 09_pcb_render_daq_system.png
```

## Documentation Map

| File | Purpose |
|---|---|
| `README_01_system_architecture.md` | Explains the complete DAQ architecture and vehicle-level integration. |
| `README_02_sensor_selection_and_signal_conditioning.md` | Documents sensors, current sensing, op-amp design, multiplexing, and signal scaling. |
| `README_03_firmware_and_logging_pipeline.md` | Explains firmware logic, safety checks, serial communication, and Python CSV logging. |
| `README_04_pcb_design_and_power_integrity.md` | Covers PCB design, power rails, protection, track-width planning, and layout methodology. |
| `README_05_testing_results_and_validation.md` | Summarizes vehicle testing, accuracy, track data, and result interpretation. |
| `README_06_student_experience.md` | Presents the project as a student engineering experience and resume-ready summary. |
| `README_07_git_upload_guide.md` | Gives upload steps for GitHub. |

## Resume Summary

**FSAE Vehicle Data Acquisition System — Embedded C, Python, KiCad, MATLAB**

Designed and implemented a custom electronic data acquisition system for an FSAE vehicle using an ATmega328-based controller, Raspberry Pi logging, analog multiplexing, op-amp current sensing, and KiCad PCB design. Integrated powertrain and vehicle-dynamics sensors, implemented firmware safety checks and serial communication, automated CSV logging using Python, and validated the system over 115 km of track testing across 76 driver/track combinations.
