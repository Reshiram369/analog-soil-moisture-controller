# analog-soil-moisture-controller
NE555 Schmitt-trigger closed-loop soil moisture controller. Breadboard-validated. MIT Manipal ASD Lab, 2025.

# Analog Soil Moisture Controller

Closed-loop irrigation controller built entirely in analog — no microcontroller.

## How it works
Two soil probes form a voltage divider with a 100kΩ potentiometer. 
As soil dries, resistance increases and the divider voltage drops. 
When it falls below Vcc/3 (3V), the NE555 output goes HIGH, 
switching the BC547 transistor which drives the relay and activates the pump.
When soil moisture is restored and voltage rises above 2Vcc/3 (6V), 
the NE555 goes LOW and the pump switches off.

## Components
- NE555 Timer in Schmitt Trigger mode
- BC547 NPN transistor (base current 8.3mA, hFE ≈ 110)
- 1N4007 flyback diode for back-EMF protection
- 100kΩ potentiometer for adjustable threshold
- 9V SPDT relay
- DC water pump

## Status
Completed — April 2025
Simulated in LTspice, built and tested on breadboard.

## Files
- ASD_report.pdf — full project report with circuit diagram, calculations and results
