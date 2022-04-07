# Enervent Pandion (EDA) Integration to Home Assistant with Modbus

Note: Even the Modbus adapter and connections used here are using low voltage, you need to open Enervent air ventilation unit to attach the adapter into it and there could be more dangerous voltages present. Do not try this unless you really know what you are doing!

## Hardware

A modbus adapter is needed between the Enervent unit and Home Assistant host (i.e. Rasperry pi). It can be connected to Freeway connector inside the Enervent unit with RJ9 connector.

HA/Rasperry pi <-(USB) Modbus adapter (RS485 + RJ9/RJ4P4C)-> Enervent unit

Following hardware is needed:
* USB to RS485 adapter, I used this one (https://www.amazon.de/-/en/gp/aw/d/B083169369/)
* RJ9/RJ4P4C connector into other end of the adapter

## Configuration

This project contains all the configuration needed to get various Envervent MODBUS registers to be used as sensors in HA and also coils as switches.

Sensors:
* Fresh air temperature (°C)
* HRC supply air temperature (°C)
* Supply air temperature (°C)
* Waste air temperature (°C)
* Exhaust air temperature (°C)
* HRC exhaust air temperature (°C)
* Exhaust air humidity (0-100%)
* Exhaust air humidity 48h average (0-100%)
* HRC supply efficiency (0-100%)
* HRC exhaust efficiency (0-100%)
* Set speed (0-100%)
* Set temperature (°C)
* Heater power (W)
* Heater recovery (0-100%)

Switches
* Away (on/off)
* Away long (on/off)
* Overpressure/fire place on (on/off)
* Cooking (on/off)
* Central vacuum cleaner (on/off)
* Max heating (on/off)
* Max cooling (on/off)
* Manual forcing (on/off)
* Summer night cooling (on/off)
* Heater status (on/off)

Control
* HA climate control for set temperature

