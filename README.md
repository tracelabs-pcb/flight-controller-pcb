# Flight Controller — FPV Drone

**Status: PCB-Design abgeschlossen — unbestückt**  
**Tool:** KiCad | **Layer:** 4-Layer | **Hersteller-ready:** Ja

---

## Projektbeschreibung

Eigenentwicklung eines Flight Controllers für FPV-Drohnen mit
integriertem 2,4GHz ELRS Empfänger, GPS, Barometer, Magnetometer
und Lidar-Schnittstelle. Vollständig in KiCad entwickelt.

**Besonderheiten:**
- SX1280 2,4GHz ELRS Funk mit TCXO und RF-Matching
- ISM330DHCX 6-DoF IMU (Accel + Gyro, SPI)
- MAX-M8W GPS mit aktiver Antenne (Taoglas AP.25F)
- MS5611 Barometer + LIS2MDL Magnetometer auf I²C
- DSHOT300 ESC-Interface via JST-GH

---

## Hardware

| Komponente | Beschreibung |
|---|---|
| MCU | STM32F405RGT6 (168MHz Cortex-M4, LQFP-64) |
| IMU | ISM330DHCXTR (6-DoF Accel+Gyro, SPI1) |
| Funk | SX1280IMLTRT (2,4GHz ELRS, SPI2, TCXO 52MHz) |
| GPS | MAX-M8W-0 (UART3, aktive Antenne) |
| Barometer | MS5611-01BA03 (I²C, 0x77) |
| Magnetometer | LIS2MDLTR (I²C, 0x1E) |
| ESC-Interface | JST-GH 5-pol (DSHOT300 + Telemetrie UART1) |
| Stackup | Würth BASIC4_ML4_1,59_17, 4-Layer, 1,6mm |

---

## PCB

- 4-Layer: Signal / GND-Plane / Power / Signal
- L2 vollflächige GND-Plane
- RF-Layout SX1280: 50Ω Microstrip, U.FL Antennenanschluss
- Leiterbahnlängen-Matching SPI-Busse

---

## Ausschlüsse

Eigenentwicklung / Portfolioprojekt — kein Serienprodukt,
kein CE/EMV, keine Firmware.

---

## Dateien in diesem Repository

- `/kicad/` — KiCad Projektdateien
- `/screenshots/` — PCB- und Schematic-Ansichten

---

> Entwickelt von [Shawn Schneider](https://tracelabs-pcb.de)  
> — PCB-Design & Lötservice, Wolfsburg
