# Klipper Smart Drybox

This project details a Klipper-controlled filament drybox that automatically regulates humidity and temperature, with material-specific drying presets.

## Features

- PID-controlled heater for smooth temperature
- Humidity monitoring and fan control
- Material presets: PLA, PETG, Nylon
- Auto-drying loop and status reporting
- Mainsail dashboard integration

## Hardware

- Heater: Generic 3950 thermistor / drybox heater
- Temperature sensors: drybox center, humidity thermistor
- Fan: 12V PWM fan
- Optional: ESP32 or Pi for extended monitoring

## Installation

1. Copy `configs/drybox.cfg` to your Klipper config folder.
2. Include macros in your START_PRINT / END_PRINT scripts.
3. Restart Klipper: `FIRMWARE_RESTART`.
4. Start drying: `DRY_PLA`, `DRY_PETG`, or `DRY_NYLON`.
5. Stop drying: `DRY_STOP`.
6. Check status: `DRY_STATUS`.

## Notes

- PLA target temperature: 45°C
- PETG target temperature: 50°C
- Nylon target temperature: 60°C
- Humidity loop runs every 10 seconds
- Status updates every 60 seconds

## Screenshots

![Drybox wiring](docs/wiring_diagram.png)
![Dashboard](docs/airflow_setup.png)
