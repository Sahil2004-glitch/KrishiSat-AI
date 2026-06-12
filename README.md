# KrishiSat-AI
KrishiSat-AI: AI-Driven Crop Mapping, Moisture Stress Detection, and Irrigation Advisory
1. Project Title
AI-Driven Automated Crop Type Mapping, Phenological Stage Monitoring, Moisture Stress Detection, and Irrigation Advisory Using Moderate-Resolution Optical and Microwave Satellite Signatures
Short name: KrishiSat-AI
2. Problem Statement
Indian agriculture needs timely, scalable, and field-level intelligence for crop type identification, growth-stage monitoring, moisture stress detection, and irrigation planning. Conventional field surveys are accurate but slow, expensive, and difficult to scale over large agricultural regions. Optical satellite data can detect crop vigour and canopy condition, but cloud cover often limits usability during monsoon and critical crop periods. Microwave SAR data works under cloud and day/night conditions and is sensitive to crop structure and surface moisture, but it needs careful preprocessing and interpretation.
KrishiSat-AI addresses this gap by fusing moderate-resolution optical and microwave satellite observations with AI models to generate crop type maps, phenological stage labels, moisture stress alerts, and irrigation advisories.
3. Proposed Solution
KrishiSat-AI is an automated geospatial decision-support system that ingests multi-temporal optical and SAR satellite data, extracts crop-relevant spectral and radar features, identifies crop type, tracks crop growth stage, detects moisture stress, and generates irrigation recommendations.
The system is designed for district, block, village, and field-scale agricultural monitoring. It can support government agencies, irrigation departments, crop insurance programs, farmer producer organizations, and agri-tech advisory services.
4. Objectives
Automate crop type classification using multi-date optical and microwave satellite signatures.
Monitor phenological growth stages such as sowing, vegetative, flowering, grain filling, maturity, and harvest.
Detect moisture stress at crop-stage level by combining vegetation indices, water indices, SAR backscatter, weather, and soil information.
Generate actionable irrigation advisories based on crop, stage, stress severity, soil type, and forecast rainfall.
Provide map-based and API-ready outputs for decision makers and farmers.
5. Innovation
Optical + microwave fusion: Uses vegetation vigour from optical bands and moisture/structure sensitivity from SAR.
Phenology-aware stress detection: Moisture stress is interpreted differently across growth stages instead of using one fixed threshold.
Explainable advisory engine: The recommendation includes the reason, stress class, urgency, expected rainfall adjustment, and confidence.
Scalable pipeline: Can run on cloud geospatial platforms such as Google Earth Engine and open-source Python geospatial stacks.
India-relevant design: Supports crops such as paddy, wheat, maize, cotton, sugarcane, pulses, oilseeds, and millets.
6. Data Sources
Satellite Data
Optical: Sentinel-2 MSI, Landsat OLI/TIRS, Resourcesat LISS-III/LISS-IV/AWiFS, MODIS or similar moderate-resolution time series.
Microwave SAR: Sentinel-1 C-band SAR, EOS-4/RISAT-style SAR, NISAR-ready future extension.
Ancillary Data
Crop calendars and agro-climatic zone information.
Soil texture and available water capacity.
Rainfall and temperature data.
Irrigation command area boundaries.
Ground truth crop labels and field observations.
7. Methodology
7.1 Data Ingestion
The system ingests satellite imagery for the area of interest and season. Optical data is filtered for cloud cover, atmospherically corrected, and composited. SAR data is calibrated, terrain corrected, speckle filtered, and converted to VV/VH backscatter.
7.2 Feature Engineering
Optical features:
NDVI for vegetation vigour.
EVI for dense canopy condition.
NDWI/LSWI for canopy and surface water condition.
NDMI for vegetation moisture.
SAVI for sparse vegetation and early crop stages.
Red-edge indices where available.
Microwave features:
VV and VH backscatter.
VH/VV ratio.
Radar Vegetation Index.
Temporal change in backscatter.
SAR-derived moisture proxy.
Temporal features:
Peak NDVI date.
Green-up rate.
Senescence rate.
Seasonal amplitude.
Stage-wise feature trajectory.
7.3 Crop Type Classification
The crop classifier uses multi-temporal feature stacks. Initial models can use Random Forest, XGBoost, or LightGBM for interpretability and strong tabular performance. Advanced versions can use temporal CNN, LSTM, Transformer, or hybrid CNN-RNN models.
Expected output:
Crop type raster or field polygon label.
Confidence score.
Confusion matrix and accuracy metrics.
7.4 Phenological Stage Monitoring
Phenology is estimated from vegetation index trajectories and SAR temporal patterns. Stage detection uses crop-specific calendars and time-series curve analysis.
Stages:
Sowing/emergence.
Vegetative growth.
Flowering/reproductive phase.
Grain or boll filling.
Maturity.
Harvest/post-harvest.
7.5 Moisture Stress Detection
Moisture stress is detected using a crop-stage-aware model. A stress score is calculated from vegetation decline, moisture index anomaly, SAR backscatter anomaly, rainfall deficit, soil water holding capacity, and crop sensitivity during the current stage.
Stress classes:
No stress.
Mild stress.
Moderate stress.
Severe stress.
The model distinguishes normal phenological senescence from true water stress by comparing the current crop trajectory against historical or regional normal trajectories for the same crop and stage.
7.6 Irrigation Advisory
The advisory engine converts stress score into field-level action:
Irrigation required or not required.
Suggested irrigation depth in mm.
Urgency window.
Rainfall adjustment.
Crop-stage-specific warning.
Confidence level.
Example advisory:
Crop: Wheat. Stage: Flowering. Stress: Moderate. Recommendation: Irrigate within 2 days with 35-45 mm unless rainfall above 20 mm is forecast. Flowering is a critical water-sensitive stage; delay can reduce yield.

8. System Architecture
KrishiSat-AI has seven modules:
Satellite data ingestion.
Preprocessing and cloud/SAR correction.
Feature extraction and time-series stack generation.
Crop classification model.
Phenology model.
Moisture stress model.
Irrigation advisory and visualization dashboard.
9. Expected Outputs
Crop type map.
Growth-stage map.
Moisture stress heatmap.
Field-wise irrigation advisory.
API output for integration with mobile apps.
Dashboard for administrative monitoring.
10. Validation Strategy
Model validation will use:
Ground truth crop survey points.
Farmer-reported crop and irrigation events.
Field moisture sensor data where available.
Weather station rainfall records.
Cross-season validation.
Accuracy, F1-score, RMSE, stress detection precision/recall, and advisory agreement with expert agronomy rules.
11. Impact
KrishiSat-AI can help:
Reduce irrigation water wastage.
Improve drought preparedness.
Support crop insurance and yield forecasting.
Enable targeted advisories for farmers.
Improve agricultural planning for government agencies.
Build a scalable national crop intelligence layer.
12. Hackathon Prototype Scope
For the qualification and prototype round, the team can demonstrate:
A sample district dashboard.
Satellite feature simulation or small-area Earth Engine workflow.
Crop classification using sample time-series data.
Phenology stage detection.
Moisture stress scoring.
Rule-based irrigation advisory generation.
13. Future Scope
NISAR integration for improved all-weather moisture and biomass monitoring.
Mobile app with multilingual farmer advisories.
Automated command-area water release planning.
Yield prediction module.
Integration with crop insurance and disaster response systems.
Edge deployment for local agricultural extension offices.
14. Conclusion
KrishiSat-AI is a scalable, AI-driven satellite intelligence system for crop type mapping, crop growth monitoring, moisture stress detection, and irrigation advisory. By combining optical and microwave satellite signatures with machine learning and agronomic rules, it can provide actionable, timely, and explainable agricultural intelligence across growth stages.
