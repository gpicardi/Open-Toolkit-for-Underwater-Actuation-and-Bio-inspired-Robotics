# Open-Source Toolkit for Underwater Actuation and Bio-inspired Robotics

## Overview

The **Open-Source Toolkit for Underwater Actuation and Bio-inspired Robotics** is designed to facilitate the development of underwater robotic manipulators and legged systems. It provides modular, cost-effective, and open-source solutions for waterproofing, control, power management, and software integration, enabling researchers and developers to prototype and test underwater robotic systems more efficiently.

### Key Features
- **Waterproof Canisters**: Designed for Dynamixel actuators, tested up to 30m depth (40 m in hyperbaric chamber testing).
- **Control & Power Management**: Custom electronics enabling efficient underwater operations.
- **Leakage Detection System**: Early warning system for water ingress.
- **ROS 2-Based Software Stack**: Facilitates control, sensing, and actuation.
- **Open-Source Design**: Hardware and software available for community contributions.

## System Components

### 1. Underwater Robotic Joint (URJ)
- Uses **Dynamixel XM430-W350** servo motors enclosed in an aluminum canister.
- Includes a **capacitive humidity sensor** and **DHT11 temperature sensor** for early leakage detection.
- Designed with **O-ring sealing** and a **pressure relief plug** to maintain internal pressure stability.
- **CAD (STEP), fabrication drawings, STL**: [Zenodo DOI: 10.5281/zenodo.22828247](https://doi.org/10.5281/zenodo.22828247)
- **Live CAD (Onshape)**: [link version]

<img src="git_images/canister.JPG" width="400">

### 2. Control & Power Management
- Based on a **Raspberry Pi 4** architecture (main board) and a dedicated battery/power management board.
- Supports **RS485 communication** for Dynamixel servos.
- Includes **DC-DC converters** for stable power delivery.
- Features integrated **humidity monitoring** for early fault detection.
- Compatible with Blue Robotics canisters for integration.
- **Schematics, PCB layout, Gerber, BOM**: [Zenodo DOI: 10.5281/zenodo.22829033](https://doi.org/10.5281/zenodo.22829033)

<img src="git_images/battery_board.png" width="400">
<img src="git_images/control_board.png" width="400">

### 3. ROS 2 Software Stack
- Modular software framework for motor control, sensing, and data acquisition.
- Supports real-time monitoring and logging.
- Facilitates integration with **networking and surface communication**.
- Source code hosted in this repository.

## Experimental Validation

### 1. Leakage Detection Tests
- Humidity sensor successfully detected small water ingress during controlled tests.
- **Failure-depth tests**: several trials conducted at different depths, with minor failures recorded at **Calabria 2021** and **La Spezia 2021**.

### 2. Structural and Environmental Tests
- Hyperbaric chamber testing up to 5 bar (40 m equivalent depth), validating sealing performance and structural integrity under static and short-duration dynamic loading.
- Field deployments in real underwater conditions for long-term monitoring.

## Applications

### 1. **SILVER2 — Full Underwater Legged Robot**
- Multiple URJs combined into 3-DoF RRR serial manipulators used as legs.
- Full assembly CAD (live, Onshape): https://cad.onshape.com/documents/34402dba64ce1250bcea8ac1/v/df3b206351e93bc1e949439c/e/421de2a9f54ad70c6c42c07b

### 2. **Tendon-Driven Actuation**
- Used for soft robotic grippers requiring flexible motion.
- Features a spooling system for precise cable-driven control.

### 3. **Underactuated Mechanisms for Sampling**
- Designed for sediment collection in underwater environments.
- Utilizes a four-bar linkage mechanism for efficient grasping and storage.

## Open Science & Reproducibility

To foster collaboration and reproducibility, all hardware designs, software, and datasets are shared under open licenses:
- **GitHub Repository** (this repo): software/ROS 2 stack
- **Zenodo — Underwater Robotic Joint**: https://doi.org/10.5281/zenodo.22828247
- **Zenodo — Control and Power Management Electronics**: https://doi.org/10.5281/zenodo.22829033
- **Onshape — SILVER2 full assembly**: https://cad.onshape.com/documents/34402dba64ce1250bcea8ac1/v/df3b206351e93bc1e949439c/e/421de2a9f54ad70c6c42c07b

We encourage contributions, modifications, and feedback to improve the toolkit and extend its capabilities for broader underwater robotics applications.

## Citing this Repository

If you use this toolkit in your research or project, please cite it as follows:

```
@misc{OpenToolkitUnderwaterActuation,
  author = {G. Picardi and S. Iacoponi and M. Carandell and J. Aguirregomezcorta and M. Chellapurath and J. del Rio and M. Calisti and J. Aguzzi},
  title = {Open-Source Toolkit for Underwater Actuation and Bio-inspired Robotics},
  year = {2026},
  url = {https://github.com/gpicardi/Open-Toolkit-for-Underwater-Actuation-and-Bio-inspired-Robotics/}
}
```
