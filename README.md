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

## 🏗️ Architecture

The project follows a modern web application architecture with separate frontend and backend components:

```
Lokus-Indian-Squid-Prediction/
├── src/
│   ├── backend/           # Flask API server
│   │   ├── app.py         # Main Flask application
│   │   ├── locus.csv      # Historical squid and environmental data
│   │   ├── LOWYES.h5      # Trained LSTM model
│   │   ├── hotspot_metadata.csv  # Fishing hotspot information
│   │   └── requirements.txt      # Python dependencies
│   ├── Frontend/          # React web application
│   │   ├── Home.js        # Landing page component
│   │   ├── Heatmap.js     # Interactive heatmap visualization
│   │   ├── Graph.js       # Time series graph component
│   │   ├── About.js       # About page component
│   │   └── style.css      # Styling and animations
│   └── Hardware/          # Additional React components
├── assets/                # Static assets (images, fonts, etc.)
└── docs/                  # Documentation and user manuals
```

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

## 📦 Installation

### Prerequisites
- Python 3.8 or higher
- Node.js 16+ and npm
- Git

### Backend Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/Lokus-Indian-Squid-Prediction.git
   cd Lokus-Indian-Squid-Prediction
   ```

2. **Set up Python environment**
   ```bash
   cd src/backend
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install Python dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Start the Flask server**
   ```bash
   python app.py
   ```
   The backend will be available at `http://localhost:5000`

### Frontend Setup

1. **Navigate to the frontend directory**
   ```bash
   cd src/Frontend
   ```

2. **Install Node.js dependencies**
   ```bash
   npm install
   ```

3. **Start the React development server**
   ```bash
   npm start
   ```
   The frontend will be available at `http://localhost:3000`

## 🎮 Usage

### Getting Started

1. **Access the Application**: Open your browser and navigate to `http://localhost:3000`

2. **Home Page**: Learn about the project, traditional jigging, and available features

3. **Heatmap Analysis**:
   - Click "Go to Heatmap" or navigate to `/heatmap`
   - Select the desired year and month
   - Click "Predict" to generate the heatmap
   - View color-coded abundance levels across fishing hotspots

4. **Graph Analysis**:
   - Click "Go to Graph" or navigate to `/graph`
   - Select year and month for prediction
   - View time series graphs showing abundance trends
   - Compare different hotspot predictions

### Data Input Format

The system expects the following data structure:

```csv
date,latitude,longitude,squid_abundance_per_kgs,sst,chl,ssh
2024-01-31,11.1711016,123.4625467,10.234,29.01999328,1.082147,0.531632435
```

Where:
- `date`: Date of observation (YYYY-MM-DD format)
- `latitude`: Geographic latitude coordinate
- `longitude`: Geographic longitude coordinate  
- `squid_abundance_per_kgs`: Squid catch rate in kilograms
- `sst`: Sea Surface Temperature in Celsius
- `chl`: Chlorophyll concentration
- `ssh`: Sea Surface Height

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

## 📈 API Endpoints

### POST `/predict`
Generates predictions for specified time periods.

**Request Body:**
```json
{
  "year": 2024,
  "month": 6
}
```

**Response:**
```json
{
  "heatmap_data": [...],
  "graphs": {...},
  "predictions": {...}
}
```

## 🔧 Configuration

### Environment Variables
- `FLASK_ENV`: Set to `development` or `production`
- `CORS_ORIGINS`: Allowed frontend origins
- `MODEL_PATH`: Path to the trained LSTM model

### Model Parameters
- **Sequence Length**: 12 time steps
- **Feature Count**: 33 variables
- **Hotspot Count**: 19 locations
- **Prediction Horizon**: Up to 12 months

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Team

- **Lead Developer**: [Your Name]
- **Data Scientists**: [Team Members]
- **Fishery Experts**: Local jiggler fishermen from Estancia, Iloilo
- **Research Partners**: [Institution Names]

## 🙏 Acknowledgments

- **Local Fishermen**: For providing valuable catch data and traditional knowledge
- **Research Institutions**: For environmental data and technical support
- **Open Source Community**: For the excellent tools and libraries used in this project

## 📞 Support

For questions, issues, or contributions:
- **Issues**: [GitHub Issues](https://github.com/yourusername/Lokus-Indian-Squid-Prediction/issues)
- **Email**: [your.email@example.com]
- **Documentation**: See the `docs/` folder for detailed user manuals

## 🔮 Future Enhancements

- [ ] Real-time data integration
- [ ] Mobile application development
- [ ] Advanced visualization options
- [ ] Machine learning model improvements
- [ ] Multi-species prediction capabilities
- [ ] Climate change impact analysis

---

**Lokus** - Empowering sustainable fishing through predictive analytics 🦑
