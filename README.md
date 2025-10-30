# 🛰️ EDC ↔ ArcGIS Connector UI  
**Interactive Jupyter Notebook for Data Transfer and Publishing**

This tool provides a user-friendly Jupyter interface for transferring data between Connectors (https://github.com/Mobility-Data-Space/mds-edc) — acting as **Consumer** and **Provider** — and publishing the received data to **ArcGIS Online or Portal**.


## 🚀 Overview
This notebook automates and visualizes:
- 🔄 **EDC data transfers** using the Management API (`/v3/transferprocesses`)
- 📥 **HttpData-PULL** flow with automatic EDR retrieval and download
- 📤 Optional **HttpData-PUSH** flow support
- 🌍 **ArcGIS publishing** (GeoJSON, CSV, Shapefile, etc.)
- 💾 **Config Save/Load** for quick reuse
- 🧭 Interactive UI built with `ipywidgets`

## ⚙️ Requirements

### Environment
- Python ≥ 3.8  
- Jupyter Notebook or JupyterLab  

### Install Dependencies

pip install arcgis requests ipywidgets

## ⚡ Quick Start

 1. Install dependencies
pip install arcgis requests ipywidgets

 2. Launch Jupyter
jupyter notebook

 3. Open notebook
arcgis assert test.ipynb

## ⚙️ Required Fields

| Field | Description |
|-------|--------------|
| **Consumer Mgmt API** | URL of consumer’s management API (`/api/management`) |
| **Provider DSP** | Provider’s DSP endpoint (`/api/dsp`) |
| **Contract ID** | Active contract between connectors |
| **Transfer Type** | `HttpData-PULL` (default) or `HttpData-PUSH` |
| **Save to** | Local path to save downloaded data |
| **ArcGIS Auth** | Choose Pro login or Portal credentials |


## 🧭 How It Works 
1. Fills in connection details & ArcGIS info.  
2. Sends a transfer request to the Provider DSP.  
3. Polls EDC until transfer = `COMPLETED`.  
4. Retrieves the EDR & downloads the data.  
5. Publishes the result to ArcGIS (if configured).
