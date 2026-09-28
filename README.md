# AIML-Based Thunderstorm & Lightning Nowcasting
AIML-Based Thunderstorm &amp; Lightning Nowcasting Smart India Hackathon (SIH) | Problem Statement ID: 26072 | Ministry of Earth Sciences (MoES) - IMD
# 🌩️ Thunderguard.AI 

[![Smart India Hackathon 2026](https://img.shields.io/badge/Smart_India_Hackathon-2026-orange?style=for-the-badge&logo=appveyor)](https://sih.gov.in/)
[![Problem Statement](https://img.shields.io/badge/PS_ID-26072-blue?style=for-the-badge)](https://sih.gov.in/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

> **Ministry of Earth Sciences (MoES) - India Meteorological Department (IMD)**  
> **Theme:** Disaster Management | **Category:** Software 

## 📖 Project Overview
An integrated AI/ML web platform designed to predict severe thunderstorms and lightning strikes within a critical 0–3 hour window (Nowcasting). 

By automatically fusing real-time atmospheric data from Doppler weather radars, INSAT satellites, lightning detection networks, and NWP models, this system provides hyper-local, automated warnings. It shifts forecasting from slow, compute-heavy physics models to instant AI pattern recognition, buying crucial time to save lives and protect infrastructure.

---

## 🚀 Key Features
*   **📡 True Multi-Modal Data Fusion:** Synchronizes disparate live data feeds (Radar dBZ, Satellite Cloud-Top Temperature, NWP grids) into a unified predictive tensor.
*   **🧠 Deep Learning Predictive Engine:** Utilizes advanced spatiotemporal models (ConvLSTM / Attention U-Net) to detect storm cell formation and predict trajectory.
*   **🗺️ Interactive Spatial Dashboard:** A high-performance React/Leaflet interface that renders real-time AI outputs as dynamic "Danger Polygons" over geographic maps.
*   **📱 Hyper-Local Geofenced Alerts:** Automatically queries user locations against AI risk zones to trigger zero-latency SMS and push notifications.
*   **👥 Role-Based Access Control (RBAC):** Dedicated views for meteorological duty officers (advanced diagnostics) and the general public (simplified tracking and alerts).

---

## 🛠️ Tech Stack
**Frontend**
*   React.js / Vite
*   Leaflet.js & GeoJSON (Spatial Visualization)
*   Tailwind CSS (Styling)

**Backend**
*   Python / FastAPI (High-performance async API)
*   Celery & Redis (Background data ingestion tasks)

**AI/ML & Data Processing**
*   PyTorch (Deep Learning architecture)
*   NumPy, Pandas, Xarray,XgBoots (NetCDF & GRIB2 meteorological data processing)

**Database**
*   PostgreSQL + PostGIS (Spatial queries & geofencing)

---

## 🏗️ System Architecture

1.  **Multi-Source Data Ingestion:** Automated fetching from IMD & MoES servers.
2.  **Data Preprocessing & Synchronization:** Spatial regridding and time-series alignment of satellite and radar pixels.
3.  **Multi-Source Data Fusion:** Stacking variables into unified ML inputs.
4.  **AI-Based Nowcasting:** 0–3 hour prediction of reflectivity and strike probability.
5.  **Risk Mapping & Scoring:** Converting grid outputs into actionable GeoJSON danger boundaries.
6.  **Alerts & Dashboard:** Real-time UI rendering and automated SMS dissemination via Twilio/Firebase.

---

## 💻 Getting Started (Local Development)

### Prerequisites
*   Node.js (v18+)
*   Python (3.9+)
*   PostgreSQL (with PostGIS extension enabled)
