# 🛰️ EDC ↔ ArcGIS Connector UI  
**Interactive Jupyter Notebook for Data Transfer and Publishing**

This tool provides a user-friendly Jupyter interface for transferring data between Connectors — acting as **Consumer** and **Provider** — and publishing the received data to **ArcGIS Online or Portal**.



 🚀 Overview
This notebook automates and visualizes:
- 🔄 **EDC data transfers** using the Management API (`/v3/transferprocesses`)
- 📥 **HttpData-PULL** flow with automatic EDR retrieval and download
- 📤 Optional **HttpData-PUSH** flow support
- 🌍 **ArcGIS publishing** (GeoJSON, CSV, Shapefile, etc.)
- 💾 **Config Save/Load** for quick reuse
- 🧭 Interactive UI built with `ipywidgets`

⚙️ Requirements

### Environment
- Python ≥ 3.8  
- Jupyter Notebook or JupyterLab  

### Install Dependencies
```bash
pip install arcgis requests ipywidgets
