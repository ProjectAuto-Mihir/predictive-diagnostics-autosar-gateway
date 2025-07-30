# Predictive Diagnostics for Gateway ECU

This repository implements a predictive diagnostic feature for a Classic AUTOSAR-based Gateway ECU. It uses embedded C logic and optional TinyML to detect faults before they occur based on historical vehicle signals.

## Features
- Health monitoring of subsystems (CAN nodes, sensors)
- Signal trend analysis and anomaly detection
- Integration with AUTOSAR Diagnostic Event Manager (Dem)
- Offline model training with Python, deployment as embedded C or TinyML

## Project Structure
- `src/` – Embedded software modules (SWC, BSW hooks, AI)
- `models/` – Trained prediction models in .h or .tflite
- `docs/` – Design documentation, signal flow diagrams
- `scripts/` – Python scripts for training and analysis
- `tests/` – Unit and integration test cases

## Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/ProjectAuto-Mihir/predictive-diagnostics-autosar-gateway.git
