# Solar-Water-Mine-Pump-Dewatering
 Smart Hybrid Dewatering & Monitoring System for Open-Pit Copper Mining
A Low-Cost, High-Efficiency IoT + Renewable Energy Mining Innovation
 Project Overview

This project presents an innovative, low-cost, and energy-efficient hybrid system designed for open-pit mining dewatering and environmental monitoring.
It integrates solar power, micro-hydro generation, hydrogen fuel concept prototype, LoRa communication, environmental sensors, and autonomous control using ESP32.

The system is designed for use in HCL (Hindustan Copper Limited) open-pit mines, where reliable dewatering, dust reduction, and real-time monitoring are critical.

Key Features
 1. Smart Dewatering System
Ultrasonic sensor measures water level in the pit.
ESP32 controls pump operation automatically.
INA219 monitors pump voltage, current, and power.
Flow-rate calculation included using ultrasonic/Venturi methods.

 2. Hybrid Renewable Power System

Solar panel + DC pump as primary power source.

Micro-hydro generator (10 W concept prototype) using sump outflow.

Hydrogen-from-water mini fuel cell model for innovation & energy backup demonstration.

 3. Dust Mitigation Enhancement

Uses Anti-Soiling Coating (ASC) concept on solar panels.

Improved energy yield in dusty open-pit environments.

 4. Real-Time Mine Monitoring

Dual LDR-based solar tracking for maximum energy capture.

LoRa (SX1278) long-range communication for sending field data to base station.

Connected sensors:

Ultrasonic (water depth)

INA219 (electrical monitoring)

LDRs (sun-tracking)

Servo motor (panel rotation)

 5. Open-Pit 3D Printed Model

A physical 3D-printed miniature open-pit mine demonstrates:

Dewatering pump setup

Solar plant placement

Drainage channels

Monitoring station
Perfect for academic display, project expo, and innovation competitions.

 Hardware Used
Component	Purpose
ESP32 Dev Module	Main controller, Wi-Fi/LoRa communication
SX1278 LoRa Module	Long-range wireless communication
INA219 Sensor	Voltage, current & power measurements
Ultrasonic Sensor	Water depth sensing
SG90 Servo Motor	Solar tracking
Dual LDRs	Light intensity comparison
Motor Driver (L298N / L9110)	Pump motor control
Micro Hydro Generator (10 W prototype)	Extra power harvesting
Hydrogen Fuel Cell (demo type)	Innovation backup system
Solar Panel (5–20 W)	Primary energy source
 ESP32 Wiring Summary

LoRa: SCK-18, MISO-19, MOSI-23, NSS-5, DIO0-26, RST-14

INA219: SDA-21, SCL-22

Servo: GPIO 13

LDR1: VP pin, LDR2: VN pin

Ultrasonic: Trigger & Echo to free GPIOs

Pump Motor Driver: IN1-14, IN2-12

 Flow Rate Calculation (Simple Version)

The system calculates flow rate using the formula:

Flow Rate (Q) = (Area × Velocity)
Velocity = Distance / Time (Ultrasonic pulses)


A dedicated flow-rate-only code is provided in the project folder.

 Innovation Highlights
 Micro Hydro + Solar Hybrid

Uses sump discharge water to rotate a small turbine → charges a small battery → powers sensors.

 Hydrogen Demo Prototype

Splits water using simple electrolysis → stores small amount of hydrogen gas → fuels a micro fuel cell (low-power demonstration concept).

 Anti-Soiling Coating (ASC)

Real-world, low-cost coating that improves solar efficiency in dusty mining environments.

 LoRa-Based Remote Monitoring

Allows mine supervisors to receive data hundreds of meters away even without internet.

 Data Transmitted Over LoRa

Water level

Flow rate

Pump status

Solar voltage/current/power

Light intensity (from LDRs)

Battery level

Fault/debug messages

 System Architecture
Solar Panel → Charge → ESP32 → Sensors → LoRa → Base Station  
                    ↓  
                Micro Hydro  
                    ↓  
              Hydrogen Prototype  


A multi-source hybrid energy model for robust operation in remote mining locations.

 Project Objectives

Improve dewatering efficiency in open-pit mines

Reduce manual labor & energy consumption

Demonstrate renewable hybrid solutions

Provide long-range monitoring using LoRa

Introduce innovative concepts for academic excellence

 Repository Structure
/src
   ├── main.ino
   ├── flow-rate.ino
   ├── lora-receiver.ino

/models
   ├── 3D_open_pit.stl

/docs
   ├── wiring_diagram.png
   ├── system_architecture.png

README.md

 Conclusion

This project provides a unique, reliable, low-cost, and innovative solution for open-pit mining dewatering and monitoring.
It integrates IoT, renewable hybrid power, 3D modeling, LoRa communication, and environmental engineering concepts into one complete system suitable for exhibitions, competitions, and real mining applications.
