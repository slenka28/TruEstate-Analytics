# TruEstate-Analytics

This project is a comprehensive data analysis and visualization exercise focused on real estate listings in **Bangalore, India**, conducted for a real estate analytics firm named **Truestate**. The goal is to analyze property listings to generate actionable business insights, create an interactive Power BI dashboard, and support decision-making using statistical and domain-specific metrics.

---

## 📌 Project Objective

To clean, enrich, and analyze raw real estate data in order to:

- Present the **current state of the Bangalore property market**
- Offer **business intelligence insights** for better decision-making
- Identify **gaps** and areas of improvement in listings
- Build a **Power BI dashboard** for interactive exploration of property trends
- Introduce new metrics like **affordability score**, **IQR**, and **enriched features**

---

## 🧾 Dataset

The base dataset consists of property listings in Bangalore, with attributes like:

- Property Name, Location, Price
- Property Type (e.g., 2 BHK Flat, 3 RK Villa)
- Description
- Additional info extracted during preprocessing

### Transformed Columns:

- `Price_Cleaned` – numeric representation of price
- `Room Type` – e.g., 2 BHK, 1 RK
- `House Type` – e.g., Flat, Villa
- `Apartment_Name`, `Street`, `City` – from cleaned `Location`
- `Price_Numeric` – numeric price without currency symbol
- Enriched Binary Features (from `Description`):
  - `Has_Parking`, `Has_Swimming_Pool`, `Has_Gym`
  - `Near_Metro`, `Near_School`, `Near_Hospital`
  - `Fully_Furnished`, `Semi_Furnished`, `Gated_Community`

---

## 🔬 Data Enrichment

### Feature Extraction from `Description`:

Each listing was enriched with additional boolean flags using keyword matching (e.g., presence of a gym, proximity to a school or metro station).

### Affordability Score:

Calculated based on median prices:
- **Affordable**: < ₹50 Lakhs
- **Medium**: ₹50 Lakhs – ₹1 Crore
- **Expensive**: > ₹1 Crore

### Percentiles and IQR:

Statistical metrics like `25%`, `50% (Median)`, `75%`, and `IQR` were calculated per Room Type & House Type combination to understand price distributions.

---

## 📈 Business Insights (For Client: Truestate)

### 1. Client Context
Truestate is a data-driven real estate consultancy aiming to enhance its data platform with deeper market insights and help buyers/investors make more informed choices.

### 2. Current State
The data initially lacked structure and had inconsistencies in pricing, property naming, and geographic tagging. There were no derived metrics like affordability or neighborhood analysis.

### 3. Desired State
Truestate wants to:
- Offer a unified property analytics dashboard
- Classify listings by affordability and amenities
- Segment listings based on buyer interest
- Understand regional price distribution and pricing volatility

### 4. Gap Analysis
| Area              | Issue                                                      | Visual Suggestion     |
|-------------------|------------------------------------------------------------|------------------------|
| Price Consistency | Some property types have wide IQRs                         | Box Plot / Violin Plot|
| Furnishing Trends | Incomplete furnishing data                                 | Stacked Bar Chart     |
| Neighborhood Info | Scattered location tags                                    | Map / Treemap         |
| Buyer-Fit         | No affordability classification                            | Heatmap / Matrix      |

---

## ❓ Key Business Questions

- What are the **most affordable combinations** of Room Type and House Type?
- Which areas show **high price inconsistency (IQR)** that may need regulation?
- Are **budget buyers better off** choosing Flats over Villas or vice versa?
- How do features like gym, parking, or pool **affect pricing**?
- Which **areas** are underserved in terms of amenities?

---

## 💡 Hypotheses

- Flat listings are more affordable and consistent than villas.
- Properties near metro stations or with amenities like gyms/swimming pools are priced higher.
- Areas with lower IQRs provide **better investment security** due to consistent pricing.

---

## 📁 Files

| File Name                              | Description                                      |
|----------------------------------------|--------------------------------------------------|
| `Bangalore_RealEstate.csv`             | Raw dataset                                      |
| `Bangalore_RealEstate_Cleaned.csv`     | Cleaned and price-normalized dataset             |
| `Bangalore_RealEstate_Enriched.csv`    | With additional features extracted from text     |
| `Price_Distribution_Summary.csv`       | Summary of average prices, IQR, etc.             |
| `Price_Distribution_Summary_Enhanced.csv` | Includes Affordability Score                    |

---

## 📊 Power BI Dashboard Features

- Interactive Filters for Room Type, House Type, Price Range
- Affordability Heatmaps
- Box Plots showing pricing spread & IQR
- Map visualizations by city and neighborhood
- Count of amenities like Gym, Metro Access, Parking, etc.

---

## 📌 Technologies Used

- Python (Pandas, Regex) for data wrangling
- Power BI for dashboard development
- Excel/CSV for reporting and portability
- Regex for pattern-based feature extraction

---
