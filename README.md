# 🌱 KrishiSat-AI: AI-Driven Crop Monitoring and Irrigation Advisory System

## Overview

KrishiSat-AI is an AI-powered precision agriculture platform designed to support farmers, researchers, and policymakers through automated crop type classification, phenological stage monitoring, moisture stress detection, and irrigation advisory generation.

The system integrates optical and microwave satellite imagery with Machine Learning and Deep Learning techniques to provide accurate and scalable agricultural intelligence for sustainable farming practices.

---

## Problem Statement

Accurate crop identification and moisture stress detection are critical for:

* Precision Agriculture
* Drought Monitoring
* Yield Forecasting
* Water Resource Management
* Climate-Resilient Farming

Traditional monitoring methods are time-consuming, expensive, and difficult to scale. KrishiSat-AI addresses these challenges using satellite remote sensing and artificial intelligence.

---

## Objectives

* Automated Crop Type Classification
* Growth Stage (Phenological) Mapping
* Moisture Stress Detection
* Irrigation Advisory Generation
* Multi-source Satellite Data Fusion
* AI-based Agricultural Decision Support

---

## Key Features

### 🌾 Crop Classification

Identify crop types using satellite imagery and machine learning algorithms.

### 📈 Phenological Monitoring

Track crop growth stages throughout the cultivation cycle.

### 💧 Moisture Stress Detection

Detect moisture deficiency using optical and SAR satellite data.

### 🚰 Irrigation Advisory

Generate field-level irrigation recommendations.

### 🛰️ Satellite Data Fusion

Combine optical and microwave datasets for improved accuracy.

### 📊 Interactive Dashboard

Visualize agricultural insights through maps and analytics.

---

## Technology Stack

### Programming Languages

* Python
* JavaScript

### Machine Learning & AI

* Scikit-Learn
* TensorFlow
* Keras
* XGBoost

### Remote Sensing

* Google Earth Engine
* Sentinel-1 SAR
* Sentinel-2 Optical
* Landsat
* MODIS

### Visualization

* Streamlit
* Plotly
* Folium

### Data Processing

* NumPy
* Pandas
* GeoPandas
* Rasterio

---

## System Architecture

```text
Satellite Data Sources
        │
        ▼
Data Acquisition Layer
        │
        ▼
Data Preprocessing
        │
        ▼
Feature Extraction
        │
        ▼
Machine Learning Models
        │
        ├── Crop Classification
        ├── Growth Stage Mapping
        ├── Moisture Stress Detection
        │
        ▼
Decision Support System
        │
        ▼
Irrigation Advisory Dashboard
```

## Repository Structure

```text
KrishiSat-AI/
│
├── README.md
├── PROJECT_ABSTRACT.md
├── IEEE_RESEARCH_PAPER.md
├── hackathon_proposal.md
├── technical_architecture.md
├── implementation_roadmap.md
├── pitch_deck_outline.md
├── data_schema.md
├── requirements.txt
│
├── src/
│   ├── sample_pipeline.py
│   └── gee_workflow.js
│
├── demo/
│   └── demo.html
│
└── docs/
    ├── architecture.png
    ├── workflow.png
    └── screenshots/
```

## Installation

### Clone Repository

```bash
git clone https://github.com/your-username/KrishiSat-AI.git
cd KrishiSat-AI
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Application

```bash
streamlit run app.py
```

---

## Workflow

1. Acquire satellite imagery.
2. Perform preprocessing and noise removal.
3. Extract vegetation and moisture features.
4. Train machine learning models.
5. Generate crop classification maps.
6. Detect moisture stress.
7. Provide irrigation recommendations.

---

## Future Enhancements

* Integration with IoT Soil Sensors
* Mobile Application Development
* NISAR Satellite Integration
* Deep Learning-Based Yield Prediction
* Real-Time Farmer Alerts
* Multi-Language Support

---

## Research Contribution

This project demonstrates the application of Artificial Intelligence, Machine Learning, and Remote Sensing for precision agriculture. The proposed framework supports sustainable farming by enabling data-driven irrigation management and crop monitoring at scale.

---

## Authors

**Sahil Kotpalliwar**

Artificial Intelligence | Machine Learning | Deep Learning | Remote Sensing | Precision Agriculture

---

## License

This project is licensed under the MIT License.
