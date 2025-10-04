# Project Sentinel

## Overview
Project Sentinel is a real-time retail analytics platform designed to monitor store operations, detect anomalies, and visualize key metrics. The system integrates data from various sources (RFID, POS, inventory, customer flow, etc.) and provides a dashboard for store status monitoring.

## Main Python Modules

### `challenge_detection.py`
Contains functions (currently placeholders) for detecting various store challenges:
- Scan avoidance
- Barcode switching
- System crashes
- Weight discrepancies
- Long queues
- Inventory discrepancies
- Long wait times

### `dashboard.py`
A Streamlit-based dashboard for real-time store status, featuring:
- Inventory status table
- Customer flow visualization (line chart)
- Resource allocation (POS usage bar chart)
- Data loading from JSONL and CSV files in `data/input`
- Integration with challenge detection and data synchronization modules

### `data_integration.py`
Utility functions for data loading and synchronization:
- Load JSONL and CSV files from `data/input`
- `synchronize_data()` returns a dictionary of all relevant dataframes (rfid, queue, pos, recognition, inventory, products, customers)

## Data Directory Structure
- `data/input/` — Raw input data (CSV, JSONL)
- `data/output/` — Output events

## Usage
1. Place input data files in `data/input/`.
2. Run the dashboard with Streamlit:
   ```powershell
   streamlit run dashboard.py
   ```
3. Extend `challenge_detection.py` with real detection logic as needed.

## Notes
- Some files (e.g., `streaming-server/stream_server.py`, `streaming-clients/client_example.py`) could not be read and are not described here.
- For more details, see the code and comments in each module.
