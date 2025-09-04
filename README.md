# Opening Range Gap (org) Automated Charting Script

## Overview

This script identifies and visualizes the Opening Range Gap in US index futures after the New York Open. It automates session construction, previous day level calculation, gap measurement, and chart annotation for research and strategy development.

## Features

- **Session Construction:**  
  Automatically builds US futures trading sessions (18:00 prior day to 16:59 current day) for each date in your dataset.

- **Session Data Filtering:**  
  Merges session info with price data, ensuring all analysis is session-aware.

- **Previous Day Levels:**  
  Calculates and plots previous day high (PD BSL) and low (PD SSL) for each session.

- **09:30 Open and Previous Close Annotation:**  
  Marks the 09:30 open and previous day close price for each session.

- **Opening Range Gap Calculation:**  
  Measures the gap between the 09:30 open and previous day close for each session.  
  Calculates 25%, 50%, and 75% gap levels for further analysis.

- **Interactive Candlestick Charts:**  
  Generates Plotly HTML charts for each session, showing price action, levels, and gap annotations.

## How It Works

1. **Load Data:**  
   Reads CSV files containing minute-level futures data.

2. **Build Sessions:**  
   Constructs session start/end times for each trading day.

3. **Merge & Filter:**  
   Merges session info with price data, filters to session times.

4. **Calculate Previous Day Levels:**  
   Computes previous day's high and low for each session.

5. **Calculate Opening Range Gap:**  
   Measures the gap between the 09:30 open and previous day close.

6. **Visualize:**  
   Plots candlestick chart with:
   - PD BSL/SSL levels
   - 09:30 open, previous close line, and its 25%, 50%, 75% levels
   - RTH Gap Range

8. **Export:**  
   Saves charts as HTML and gap events as a DataFrame.

## Usage

1. **Configure File Paths:**  
   Update the CSV path and output directory as needed.

2. **Run the Script:**  
   Execute in a Jupyter Notebook or Python environment.

3. **View Charts:**  
   HTML charts will be saved and displayed for each session.

## Requirements

- Python 3.x
- pandas
- numpy
- plotly
- IPython (for display in notebooks)

## Notes

- The script is designed for minute-level futures data with columns: `time`, `open`, `high`, `low`, `close`.
- All session logic is based on US Eastern Time.
- Gap closure analysis is performed for the overall session and at each 30-minute interval, labeled by the ending time (exclusive).

## Customization

- You can adjust session times, gap logic, or add more annotations as needed.
- The script is modular and can be extended for other markets or timeframes.

---

**Author:** livefreeordie_t ([https://x.com/livefreeordie_t](https://x.com/livefreeordie_t))  
**Last updated:** September 2025
