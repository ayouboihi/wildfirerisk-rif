# WildfireRisk-Rif 
readme_content = """# 🔥 WildfireRisk-Rif — Forest Fire Risk Prediction

A geospatial machine learning project that predicts **wildfire risk zones** in the **Rif Mountains, Morocco** using real Sentinel-2 satellite imagery and a Random Forest classifier.

---

## 📌 Project Overview

| Item | Details |
|---|---|
| **Satellite** | Sentinel-2 L2A (ESA / Copernicus) |
| **Bands used** | B04 (Red), B8A (NIR), B11 (SWIR-1), B12 (SWIR-2) |
| **Study area** | Rif Mountains — Tétouan / Chefchaouen, Morocco |
| **Date** | September 23, 2023 (peak fire season) |
| **Resolution** | 20 metres per pixel |
| **ML Model** | Random Forest Classifier (scikit-learn) |

---

## 🗺️ Outputs

| File | Description |
|---|---|
| `rif_indices.png` | NDVI, NBR, NDWI spectral indices maps |
| `rif_fires_ndvi.png` | NDVI map with documented fire locations |
| `rif_fire_risk_map.png` | Static fire risk map (4 classes) |
| `wildfire_risk_interactive.html` | Interactive Folium web map |
| `morocco-wildfire-prediction.ipynb` | Full analysis notebook |

---

## 🔥 Fire Risk Classes

| Class | Color | Description |
|---|---|---|
| Low | 🟢 Green | Water bodies, wet zones, dense forest |
| Moderate | 🟡 Yellow | Sparse vegetation, some moisture |
| High | 🟠 Orange | Dry vegetation, low moisture |
| Extreme | 🔴 Red | Very dry, stressed vegetation — highest risk |

---

## 📊 Key Results

- **Study area:** ~1,000 km² — Rif Mountains, Morocco
- **Total pixels analyzed:** ~30 million (20m resolution)
- **Fire risk distribution:**
  - 🟢 Low: 65.3%
  - 🟡 Moderate: 10.2%
  - 🟠 High: 8.4%
  - 🔴 Extreme: 16.1%

---

## 🧠 Spectral Indices Used

| Index | Formula | Fire Risk Relevance |
|---|---|---|
| NDVI | (NIR - Red) / (NIR + Red) | Low NDVI = dry vegetation = high risk |
| NBR | (NIR - SWIR2) / (NIR + SWIR2) | Detects burned/dry areas |
| NDWI | (NIR - SWIR1) / (NIR + SWIR1) | Low moisture = high risk |

---

## 🔧 Installation

```bash
conda create -n geoenv python=3.11
conda activate geoenv
conda install -c conda-forge geopandas rasterio matplotlib jupyter -y
conda install -c conda-forge libgdal-jp2openjpeg -y
pip install rioxarray folium pillow pandas scikit-learn
```

---

## 🚀 Usage

1. Register at [Copernicus Data Space](https://dataspace.copernicus.eu)
2. Run `morocco-wildfire-prediction.ipynb` in Jupyter
3. Enter your credentials when prompted (getpass — never stored)

---

## ⚠️ Note on ML Approach

Labels were derived from rule-based spectral thresholds (NDVI, NBR, NDWI). For production use, real fire history data from [EFFIS](https://effis.jrc.ec.europa.eu/) or [NASA FIRMS](https://firms.modaps.eosdis.nasa.gov/) is recommended as ground truth.

---

## 📚 Technologies

`Python` `Sentinel-2` `Copernicus API` `Random Forest` `Scikit-learn` `RioXarray` `Rasterio` `NumPy` `Matplotlib` `Folium` `Remote Sensing` `GIS` `Machine Learning`

---

## 👤 Author

**Ayoub Oihi** — Geomatics & Remote Sensing | Geospatial Data Science  
📧 ayouboihi9@gmail.com  
🔗 [GitHub](https://github.com/ayouboihi)
🌐 https://ayouboihi.github.io/portfolio/
"""

with open("C:/Users/mon pc/wildfirerisk-rif/README.md", "w", encoding="utf-8") as f:
    f.write(readme_content)
print("✅ README.md created!")
