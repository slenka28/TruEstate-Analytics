# TruEstate-Analytics

A comprehensive analysis of Bangalore's real estate market for **Truestate**, a real estate analytics firm. This project cleans, enriches, and visualizes property data to derive actionable insights and support data-driven decision-making.

---

## 📌 Table of Contents
- [Project Objective](#-project-objective)
- [Dataset](#-dataset)
- [Methodology](#-methodology)
- [Business Insights](#-business-insights)
- [Key Questions & Hypotheses](#-key-business-questions)
- [Files](#-files)
- [Dashboard Features](#-power-bi-dashboard-features)
- [Technologies Used](#-technologies-used)
- [Code Snippets](#-sample-python-snippets)

---

## 📌 Project Objective

Clean, enrich, and analyze raw real estate data to:
- Present **current market trends** in Bangalore
- Generate **actionable business intelligence insights**
- Identify gaps in property listings
- Build an **interactive Power BI dashboard**
- Introduce metrics like **affordability score** and **IQR**

---

## 🧾 Dataset

### Attributes
- Property Name, Location, Price, Type (e.g., "2 BHK Flat")
- Extracted Features: `Price_Cleaned`, `Room Type`, `House Type`, `Apartment_Name`, etc.

### Enriched Features (Boolean Flags from Descriptions)
| Feature             | Description                          |
|---------------------|--------------------------------------|
| `Has_Parking`       | Parking availability                |
| `Near_Metro`        | Proximity to metro stations         |
| `Fully_Furnished`   | Furnishing status                   |
| ...                 | ...                                  |

---

## 🔬 Methodology

### Data Enrichment
- **Affordability Score**: Categorized properties as *Affordable* (<₹50L), *Medium* (₹50L–1Cr), or *Expensive* (>1Cr).
- **Statistical Metrics**: Calculated IQR, percentiles, and median prices by property type.
- **Feature Extraction**: Used regex to flag amenities (gym, pool, etc.) from descriptions.

### Tools & Techniques
- **Python**: Pandas for cleaning, regex for text extraction.
- **Power BI**: Interactive dashboards with filters, maps, and heatmaps.
- **Statistical Analysis**: Price distribution analysis using IQR.

---

## 📈 Business Insights

### Gap Analysis
| Area              | Issue                                | Visualization          |
|-------------------|--------------------------------------|------------------------|
| Price Consistency | High IQR in some property types     | Box Plot               |
| Furnishing Trends | Incomplete furnishing data          | Stacked Bar Chart      |
| Neighborhood Info | Unstructured location tags          | Geospatial Map         |

### Recommendations
- Standardize pricing formats to reduce IQR volatility.
- Add structured fields for amenities and furnishing status.
- Use geospatial analysis to identify underserved areas.

---

## ❓ Key Business Questions

1. Which **Room Type + House Type combinations** are most affordable?
2. Which areas have high price inconsistency (IQR) needing regulation?
3. Do amenities like gyms or pools significantly affect prices?
4. Are budget buyers better served by Flats vs. Villas?

---

## 💡 Hypotheses

- 🏘️ **Flats** are more affordable and price-consistent than Villas.
- 🚇 Properties near metros command **10–15% higher prices**.
- 📉 Low-IQR areas offer **safer investment opportunities**.

---

## 📁 Files

| File                                | Description                          |
|-------------------------------------|--------------------------------------|
| `Bangalore_RealEstate.csv`          | Raw property listings                |
| `..._Cleaned.csv`                   | Normalized prices and locations      |
| `..._Enriched.csv`                  | Added amenities and affordability    |
| `Price_Distribution_Summary.csv`    | IQR, median, and price stats         |

---

## 📊 Power BI Dashboard Features

- **Interactive Filters**: Price range, room/house type, amenities.
- **Visualizations**: 
  - Heatmaps for affordability scores
  - Box plots for price distribution analysis
  - Geospatial maps for neighborhood trends
- **Amenity Analysis**: Side-by-side comparison of gym/pool/parking availability.

---

## ⚙️ Technologies Used

- **Python**: Pandas, Regex
- **Power BI**: Dashboarding
- **Excel/CSV**: Data storage and reporting

---
