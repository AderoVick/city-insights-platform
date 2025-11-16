# City Insights Platform

<p align="left">
  <img alt="Python" src="https://img.shields.io/badge/Python-3.11-blue?logo=python" />
  <img alt="FastAPI" src="https://img.shields.io/badge/FastAPI-API-green?logo=fastapi" />
  <img alt="Streamlit" src="https://img.shields.io/badge/Streamlit-Dashboard-red?logo=streamlit" />
</p>

End-to-end project for city mobility + air-quality analytics. Generates synthetic hourly data, cleans it, builds features, and trains a RandomForest to predict next-hour PM2.5. Ships a FastAPI `/predict` endpoint and a Streamlit dashboard for KPIs, charts, and live scoring. Docker, tests, and notebooks included.

## Preview
*(Appears after you upload the `assets/` folder)*
![Dashboard Preview](assets/screenshot.png)

## Quickstart
```bash
python -m venv .venv
# macOS/Linux
source .venv/bin/activate
# Windows PowerShell
.venv\Scripts\Activate.ps1
pip install -r requirements.txt

# Pipeline
python -m src.etl.make_dataset
python -m src.features.build_features
python -m src.models.train_model
