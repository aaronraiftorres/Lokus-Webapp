# 🦑 Lokus: Indian Squid Prediction System

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![React](https://img.shields.io/badge/React-18.0+-blue.svg)](https://reactjs.org/)
[![Flask](https://img.shields.io/badge/Flask-3.0+-green.svg)](https://flask.palletsprojects.com/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.16+-orange.svg)](https://tensorflow.org/)

## 📖 Overview

**Lokus** is an advanced predictive web application that employs Long Short-Term Memory (LSTM) neural networks in conjunction with geospatial analysis to forecast the abundance and movement patterns of Indian squid in the northern Iloilo Sea. The application utilizes historical environmental data, including Sea Surface Temperature (SST), Sea Surface Height (SSH), and Chlorophyll (CHL) concentrations, along with squid catch rate data derived from firsthand interviews conducted with jiggler fishermen in Estancia, Iloilo.

### 🎯 Key Features

- **Predictive Analytics**: Monthly forecasts of squid abundance using LSTM models
- **Interactive Heatmaps**: Visual representation of squid density across fishing hotspots
- **Time Series Graphs**: Trend analysis and pattern recognition in squid populations
- **Geospatial Analysis**: Location-based predictions for optimal fishing areas
- **Real-time Data Processing**: Integration of environmental and catch data

## 🚀 Features

### 🔥 Interactive Heatmap
- **Visual Density Mapping**: Color-coded representation of squid abundance
- **Temporal Selection**: Choose specific months and years for predictions
- **Hotspot Identification**: Identify high-yield fishing areas
- **Legend System**: Clear color coding for abundance levels
  - 🔴 Red: High Abundance
  - 🟡 Yellow: Medium Abundance  
  - 🟢 Yellow-Green: Slight Abundance
  - 🔵 Blue: Low Abundance

### 📊 Time Series Graphs
- **Trend Analysis**: Visualize squid population changes over time
- **Multi-Hotspot Comparison**: Compare predictions across different fishing areas
- **Historical Data Integration**: Combine past data with future predictions
- **Interactive Controls**: Select time periods for detailed analysis

### 🎣 Traditional Jigging Information
- **Cultural Context**: Information about traditional squid jigging techniques
- **Fishing Methods**: Details about jig-based fishing practices
- **Community Impact**: Understanding of local fishing communities

## 🛠️ Technology Stack

### Backend
- **Python 3.8+**: Core programming language
- **Flask**: Web framework for API development
- **TensorFlow 2.16+**: Deep learning framework for LSTM models
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Scikit-learn**: Machine learning utilities
- **Folium**: Interactive map generation
- **Matplotlib**: Data visualization

### Frontend
- **React 18+**: Modern JavaScript framework
- **CSS3**: Styling and animations
- **Axios**: HTTP client for API communication
- **Responsive Design**: Mobile-friendly interface

### Data Sources
- **Environmental Data**: SST, SSH, and CHL measurements
- **Catch Data**: Historical squid abundance from jiggler fishermen
- **Geospatial Data**: Latitude/longitude coordinates for fishing hotspots


## 🔬 Model Details

### LSTM Architecture
- **Input Features**: 33 environmental and historical variables
- **Sequence Length**: 12 time steps for temporal modeling
- **Output**: Squid abundance predictions in kilograms
- **Training Data**: Historical data from 2016-2024
- **Geographic Coverage**: Northern Iloilo Sea (11-12°N, 123-124°E)

### Feature Engineering
- **Lag Variables**: 1-6 month lags for abundance, SST, CHL, and SSH
- **Rolling Statistics**: 3-month moving averages and standard deviations
- **Hotspot Encoding**: Location-based categorical features
- **Data Preprocessing**: MinMax scaling and missing value interpolation

### Prediction Accuracy
- **Short-term**: High accuracy for 1-3 month predictions
- **Long-term**: Decreasing accuracy for predictions beyond 6 months
- **Validation**: Cross-validation across multiple fishing hotspots

## 🌊 Geographic Coverage

The system focuses on the **Northern Iloilo Sea** with the following boundaries:
- **Latitude**: 11°N to 12°N
- **Longitude**: 123°E to 124°E
- **Primary Fishing Areas**: Estancia, Iloilo and surrounding waters
- **Hotspot Count**: 19 identified fishing locations


## 👥 Team

Lokus was developed by B.S. Computer Science students at West Visayas State University for their undergraduate thesis.

- Regino C. Gallena
- Kyla Joy O. Rapita
- Journey Mariz J. Sermonia
- Aaron Raif B. Torres


## 📞 Support

For questions, issues, or contributions:
- **Email**: [Lokus2025@gmail.com]
- **Documentation**: See the `docs/` folder for detailed user manuals

---

**Lokus** - Empowering sustainable fishing through predictive analytics 🦑
