# 📋 Project Phantom: The Real BOM List

This is the complete breakdown of what's currently sitting on the lab bench versus the upgraded hardware kit we actually need to get this platform scratch-built.

---

## 🛠️ Stuff We Already Have (The Current Lab Bench)

This is the gear we already own. We're using a lot of this for initial testing, bench setups, and flight physics checks. Anything with a `*` next to it will be kept on the side as a backup or used for desk testing later on.

### ✈️ Airframes & Power Core
* **Apprentice S15e Airframe** (Awesome high-wing trainer for testing concepts)
* **AtomRC Dolphin Pro Airframe** (Forward-swept wing frame)
* **2807 1100KV Brushless Outrunner Motor**
* **6S 50A BLS ESC Unit**
* **2x 8040-2 (8x4) Two-Blade Propellers**
* **4x S09M 9g Digital Metal Gear Servos**
* **4S 2200mAh LiPo Battery** `*`
* **6S 3500mAh LiPo Battery**

### 🧠 Flight Compute & Boards
* **AtomRC F405 NAVI Deluxe Flight Controller** (Came stock inside the Dolphin Pro RTH)
* **Arduino Uno R4** (Currently acting as our main data log aggregator)
* **Arduino Nano** `*` (Good old secondary micro-node)

### 🛰️ Telemetry, Radio, & Basic Sensors
* **RadioLink TD12 Transmitter & R12F Receiver Setup** (Our main radio control link)
* **AtomRC BE220 GPS Module** (Stock navigation unit that came with the plane)
* **Standard NEO-6M / NEO-M8N GPS Module** (Basic standalone unit)
* **MPU6050 6-Axis IMU** `*`
* **RF Transceiver Modules** (For basic wireless data tracking)
* **BME680 Sensor Matrix** (Tracks VOC gas, temp, humidity, and pressure)
* **PMS5003 Particulate Matter Sensor** (Laser dust sensor for PM2.5 monitoring)
* **DHT11 Sensor** `*` (Basic temp and humidity stick)
* **Standard MQ Gas Sensor Module** `*` (Baseline gas tracker)

---

## 🛠️ Structural Building Supplies & Bench Consumables (~$20 - $120)

The essential setup gear needed to wire up the custom frame, solder connections, and keep everything secure inside the hull so nothing shifts mid-air.

* [ ] **Silicone Hookup Wire Assortment** (20AWG down to 28AWG so the sensor signals stay flexible and clean)
* [ ] **Thick Power Wire & Connectors** (12AWG/14AWG wire and XT60/XT90 plugs for the main battery lines)
* [ ] **Solderless Breadboards** (For testing code layouts on the desk before soldering it permanent)
* [ ] **High-Strength CA Glue & Activator** (Absolutely necessary for bonding the 3D-printed LW-PLA parts together)
* [ ] **Heavy-Duty Velcro Straps** (To lock the big 6S battery and components flat against the airframe floor)
* [ ] **Heat-Shrink Tubing Pack** (To cleanly cover up soldered connections)
* [ ] **Zip Ties & Adhesive Mounts** (To route wiring clean and keep it completely away from moving servo arms)

---

## 🚀 The Shopping List: What We Need to Build It From Scratch

This is the big upgrade loop. To make the airplane truly custom and incredibly powerful, we are bypassing pre-built foam kits and commercial autopilot brains. Everything we already have has been taken out of this list so we don't buy double.

| Category | What We Need | Why We Need It | Real Market Price (USD) |
| :--- | :--- | :--- | :--- |
| **Fabrication** | [ ] Desktop 3D Printer | **The main priority.** Needed to print the whole custom airframe from zero. | $200 - $350 |
| **Materials** | [ ] LW-PLA Filament Spools | Foaming filament to make the 3D-printed plane super light. | $35 - $65 / spool |
| **Materials** | [ ] Carbon Fiber Rods & Tubes | Internal main spars to give the wings and body real strength. | $15 - $25 |
| **Flight Compute**| [ ] Teensy 4.1 Microcontroller | To run our own completely custom, high-speed PID control loop software. | $30 |
| **AI & Vision** | [ ] Raspberry Pi 5 (Recent Model) | Upgraded heavyweight co-processor brain to run edge AI and handle vision tasks. | $115 - $165 |
| **AI & Vision** | [ ] Depth Camera | RealSense or binocular equivalent for spatial mapping, obstacle avoidance, and 3D environment tracking. | $280 - $520 |
| **AI & Vision** | [ ] Lightweight Industrial Camera | Global shutter / highly crisp optical capture for fast aerial imaging without rolling distortions. | $80 - $150 |
| **Navigation** | [ ] ICM-20948 9-Axis IMU | Upgrading from the basic MPU6050 to poll motion data way faster. | $15 |
| **Navigation** | [ ] Beitian BN-880 GPS/Compass | Gives us high-accuracy waypoint navigation with an external compass. | $20 |
| **Navigation** | [ ] Time-of-Field (ToF) Sensor | Laser distance altimeter for perfect landings and low alt tracking. | $10 - $15 |
| **Atmospheric** | [ ] SCD40 CO2 Sensor | True photoacoustic sensor to get real, exact greenhouse gas mappings. | $40 - $50 |
| **Atmospheric** | [ ] MQ-135 Gas Sensor | Target specialized air quality levels in the atmosphere. | $5 |
| **Propulsion** | [ ] Coaxial Brushless Setup | Contrarotating motor assembly for a massive power boost. | $40 - $60 |
| **Propulsion** | [ ] Secondary 6S ESC | To drive the second motor in the coaxial dual-stack configuration. | $25 - $35 |
| **Servos** | [ ] 4x Wing + 4x Rudder/Tail | Getting all the servos needed for our custom control surfaces. | $30 - $50 total |
| **Mechanisms** | [ ] 3x Landing Gear Servos | To build our own custom deployable/retractable gear system. | $20 - $30 total |
| **Gimbal** | [ ] 4x Gimbal Servos | Active servo setup to keep the main sensor/camera payload completely stable. | $25 - $45 total |
| **Telemetry & FPV**| [ ] Complete FPV Kit System | Combo kit including Low-latency Analog Micro FPV Camera, 5.8GHz Video Transmitter (VTX), and 4.3" FPV Ground Monitor Screen. | ~$135 (500 AED) |
| **Telemetry** | [ ] Long-Range LoRa Modules | Dedicated data link to pass raw telemetry text strings independently. | $25 - $40 |

> ⚠️ *Note: We'll pull our existing **BME680** off the test bench and throw it right into the new setup when building, so no need to buy a second one.*

---

## 💡 Why Go Through All This Trouble?

* **Scratch-Made Airframe:** Moving away from standard factory-molded EPO foam means we can 3D print our own airframe exactly how we want it. We can design internal cooling ducts and special nose slots for the air sensors that you simply can't do on a pre-bought plane.
* **Our Own Code & PID Loop:** Instead of flashing normal open-source autopilot setups that lock you out of the core data, we are writing the custom flight software and tuning the PID stabilization loops completely from scratch.
* **Heavyweight Computational Power:** Splitting up the processing makes the plane insanely fast. The **Teensy 4.1** focuses entirely on the lightning-fast flight control loops. Meanwhile, the **Raspberry Pi 5** works alongside the depth and industrial cameras to analyze vision data, process edge maps, and tag greenhouse metrics in real-time mid-air.
