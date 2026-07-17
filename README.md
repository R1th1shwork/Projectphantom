# Project Phantom 🚀

[![Platform](https://img.shields.io/badge/Platform-AtomRC%20Dolphin-orange.svg)](#-hardware-architecture)
[![Firmware](https://img.shields.io/badge/Firmware-iNAV%20Fixed--Wing-blue.svg)](https://inavflight.com/)
[![Co-Processor](https://img.shields.io/badge/Co--Processor-Arduino%20Uno%20R4-green.svg)](#-compute--avionics)

Project Phantom is an autonomous, fixed-wing environmental monitoring Unmanned Aerial Vehicle (UAV). Built on the **AtomRC Dolphin** airframe, the platform is engineered for real-time atmospheric data logging, micro-climate tracking, and localized air pollution mapping across changing flight paths and altitudes. 

By integrating a custom co-processor architecture with a dedicated navigation flight controller, it provides a highly reliable, dynamic data-collection alternative to traditional fixed environmental networks.

---

## 📅 Development & Engineering Phases

### 🔹 Phase 1: Digital Concept Modeling (Blender)
* **Layout Mapping:** Core internal component layout, structural distributions, and advanced actuator placements are digitally prototyped inside Blender.
* **Weight Distribution:** Internal battery placement options and component orientations are mapped to ensure optimal balance and weight distribution before physical assembly.

### 🔹 Phase 2: Functional Prototyping & Bench Testing
* **Electronics Tray Validation:** The sensor aggregation package is built and wired using an Arduino platform, operating alongside primary flight computing hardware to validate real-time data logging pipelines.
* **3D Print Tolerances:** Physical 3D prints consist of small-scale functional vectoring test configurations and enclosure mechanisms to run physical clearance checks before scaling up fabrication.
* **Airframe Preparation:** The AtomRC Dolphin delta-wing airframe is undergoing iNAV firmware initialization, servo centering, and control surface matching to prepare for future flight envelopes.

---

## 📊 Real-World Flight Validation Logs (The Ranger Test-Bed)

Initial operational validation and data gathering were successfully executed using a borrowed high-wing prototype to prove the concept in live airspace.

* **Airframe:** Volantex Ranger (Borrowed Prototype)
* **Completed Sorties:** 2 successful validation flights
* **Flight Duration:** 6 to 7 minutes per flight
* **Operational Altitude:** Achieved up to 150 meters altitude
* **Data Logging Strategy:** All incoming datasets were securely captured and committed directly to the flight controller's internal Blackbox (SD Card).
* **Recovered Telemetry Data:** Successfully recorded comprehensive datasets containing:
  * GNSS/GPS Altitude profiles
  * Dynamic IMU Accelerometer data
  * Environmental sensor readings (BME680 atmospheric metrics, temperature, gas resistance, and companion PM/MQ tracking)

---

## 🛠️ Hardware Architecture

### ✈️ Airframe & Propulsion Core
* **Airframe:** AtomRC Dolphin (Forward swept wing design)
* **Motor:** 2807 1100KV Brushless Outrunner Motor
* **ESC:** 6S 50A Electronic Speed Controller with integrated BEC
* **Propeller:** 8040-2 Dual-Blade Propeller (Precision balanced to eliminate high-frequency motor/acoustic vibrations and remove video jello)
* **Power Configuration:** 6S 3000–4000mAh LiPo Battery Pack (Baseline test unit: 6S 3500mAh)

### 🧠 Compute & Avionics
* **Flight Controller:** AtomRC F405 NAVI Deluxe
* **Primary Flight Firmware:** iNAV Configurator setup for fixed-wing navigation, stabilization profiles, and waypoint navigation.
* **Data Log Aggregator (Co-Processor):** Arduino Uno R4 running a dedicated custom code stack managing independent, non-blocking high-frequency $I^2C$ data polling loops and data storage.

### 🍃 Current Sensor Stack
* **BME680 Array:** Tracks and logs ambient temperature, relative humidity, barometric pressure, and volatile organic compound (VOC) gas resistance.
* **MQ-135 Module:** Tracks baseline environmental gas levels.
* **PM Sensor System:** Maps local airborne particulate matter counts.

---

## 🚀 Future Hardware Upgrades BOM (Next-Gen Specifications)

To achieve faster processing speeds, advanced onboard edge-computing capability, and highly accurate nose-isolated sensor arrays, the platform will transition to the following upgraded architecture:

### 🧠 Brains & Processing
* **Flight Controller Node:** Teensy 4.1 Microcontroller *(Configured for an ultra-high-frequency deterministic processing loop)*
* **AI Co-Processor:** Raspberry Pi *(Edge compute node for complex data modeling and filtering)*

### 🛰️ Sensors & Navigation
* **IMU:** ICM-20948 9-Axis High-Performance IMU
* **GPS Module:** Beitian BN-880 GPS & Compass Module
* **Altitude/Distance:** Time-of-Field (ToF) Precision Distance Sensor

### 🍃 Next-Gen Environmental Monitoring Suite
* **CO2 Sensor:** SCD40 Carbon Dioxide Sensor
* **Gas & Air Quality:** MQ-135 Gas Sensor
* **Weather/Atmospheric:** BME680 Sensor Matrix

### ⚙️ Actuators & Propulsion
* **Motor System:** Coaxial Brushless Motor Setup *(Contrarotating high-efficiency configuration)*
* **ESC Stack:** Dual Brushless Electronic Speed Controllers
* **Control Surfaces:** 4x Wing Servos, 4x Rudder/Tail Servos
* **Mechanisms:** 3x Landing Gear Servos, 4x Gimbal System Servos

### 📡 Telemetry & FPV (First Person View)
* **Visual Feed:** Analog Micro Camera + 5.8GHz Video Transmitter (VTX)
* **Ground Station:** 4.3-inch FPV Monitor with Built-in Receiver
* **Data Link:** Long-Range LoRa Telemetry Modules

### 📐 Structural & Airframe Materials
* **Airframe Composites:** Lightweight PLA (LW-PLA) for maximum structural weight savings
* **Reinforcements:** High-modulus Carbon Fiber Rods and Tubes
