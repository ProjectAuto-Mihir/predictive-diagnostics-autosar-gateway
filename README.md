# Predictive Diagnostics in Classic AUTOSAR Gateway ECU

This repository contains a Classic AUTOSAR-compliant implementation of a Predictive Diagnostic Feature, combining embedded C, Python, and TinyML to forecast ECU faults or abnormal behavior based on signal patterns.

## Tech Stack
- **AUTOSAR Classic Platform (RTE, BSW, DEM)**
- **Embedded C (AI logic, fault injection)**
- **TinyML (TFLite Micro / CMSIS-NN)**
- **Python (Model training & conversion)**

## Features
- Signal monitoring and anomaly detection
- Embedded AI model integration
- Interface with Dem for DTC logging
- AUTOSAR Software Component (SWC) integration

## Project Structure
- `src/` – Core embedded modules: SWC, AI, BSW hooks
- `models/` – Trained model in `.tflite` and `.h` formats
- `scripts/` – Python training, preprocessing, conversion
- `docs/` – Architecture, signal flow, implementation notes
- `tests/` – Unit test and fault injection validation

## Getting Started

1. **Train model**:
    ```bash
    python scripts/train_predictive_model.py
    ```

2. **Convert to embedded C header**:
    ```bash
    python scripts/convert_to_tflite.py
    python scripts/generate_header.py
    ```

3. **Integrate `.h` model in `src/ai_module/model_predictor.c`**

4. **Configure SWC and Dem hooks** using `config/DiagPredictiveSWC.arxml`

## Use Cases
- Predict sensor failures or line anomalies
- Early CAN node communication loss detection
- Forecasting actuator degradation over time

## License
[MIT License](LICENSE)
