# Stock Price Forecasting

## Overview
This project downloads historical stock price data, preprocesses it, trains a forecasting model, and provides a sleek, dark‑mode web UI to visualize past prices and future forecasts.

## Quick Start
```bash
# Create a virtual environment
python -m venv venv
source venv/Scripts/activate  # Windows PowerShell

# Install dependencies
pip install -r requirements.txt

# Download data (default ticker: AAPL)
python data/download_data.py

# Train the model
python src/train.py

# (Optional) Start the Flask API for the UI
python api/app.py
```

Open `index.html` in a browser to see the interactive chart.

## Project Structure
```
stock-forecast/
├─ README.md               # This file
├─ requirements.txt        # Python dependencies
├─ data/
│   ├─ download_data.py   # Fetches price data
│   └─ raw/               # CSV files
├─ src/
│   ├─ preprocess.py      # Data cleaning & splitting
│   ├─ model.py           # Model wrapper (ARIMA/LSTM)
│   ├─ train.py           # Training script
│   └─ predict.py         # Forecast generation
├─ notebooks/
│   └─ analysis.ipynb     # Exploratory analysis
├─ assets/
│   ├─ style.css          # Premium dark‑mode styling
│   ├─ app.js             # Front‑end logic
│   └─ chart.js           # Chart.js (CDN link)
├─ api/
│   ├─ app.py             # Flask API (optional)
│   └─ requirements.txt   # Flask dependency
├─ models/                 # Saved model files
└─ docs/
    └─ report.md          # Detailed report & future work
```

## License
MIT License – feel free to modify and extend.
