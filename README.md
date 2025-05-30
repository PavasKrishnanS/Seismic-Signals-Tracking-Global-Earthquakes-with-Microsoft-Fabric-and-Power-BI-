# 🌍 Seismic Signals: Tracking Global Earthquakes with Microsoft Fabric and Power BI

This project analyzes real-time earthquake data using the USGS Earthquake API. Built using Microsoft Fabric's Lakehouse architecture, Python notebooks, and Power BI, the solution tracks seismic activity across the globe—specifically focusing on the Myanmar-Thailand region between **March 19 – April 4, 2025**, a period of intense earthquake activity.

---

## 📌 Project Objectives

- Fetch global earthquake data using the [USGS Earthquake Catalog API](https://earthquake.usgs.gov/fdsnws/event/1/)
- Store and manage raw and transformed data using Microsoft Fabric Lakehouse (Bronze, Silver, Gold layers)
- Enrich and classify earthquake data using geolocation and significance metrics
- Build an interactive Power BI dashboard for quick analysis and awareness

---

![generated-image](https://github.com/user-attachments/assets/186402ac-f85e-4321-a0a7-80c4be769a88)



## 🧱 Architecture Overview

### 1. **Data Ingestion (Bronze Layer)**
- **Tools:** Microsoft Fabric Workspace, Python Notebooks
- **Process:** Data fetched from USGS API using `requests` and stored as raw JSON in the Lakehouse

### 2. **Data Transformation (Silver & Gold Layers)**
- **Silver Layer:** 
  - Cleaned raw data
  - Converted timestamps from Unix to readable datetime
  - Selected relevant fields only
- **Gold Layer:**
  - Added country code using reverse geocoding
  - Categorized significance into `Low`, `Moderate`, `High`

### 3. **Data Visualization**
- **Platform:** Microsoft Power BI (integrated with Fabric)
- **Features:**
  - Bar charts showing earthquake counts by date and severity
  - Filters for magnitude and date range
  - Map visual was limited due to trial account restrictions

---

## 📅 Focus Timeframe

- **Date Range:** March 19, 2025 – April 4, 2025
- **Reason for Focus:** Multiple high-magnitude earthquakes occurred in Myanmar and Thailand during this time. The project aims to bring awareness to regional seismic activity and its implications.
 https://en.wikipedia.org/wiki/2025_Myanmar_earthquake
 https://www.bbc.com/news/articles/crlxlxd7882o



## 🔧 Tools & Technologies Used

| Tool            | Purpose                             |
|-----------------|-------------------------------------|
| Microsoft Fabric| Data ingestion, processing pipeline |
| Lakehouse       | Storage for raw and transformed data|
| Python Notebook | API data pull, transformation       |
| Power BI        | Dashboard & Visualization           |
| Reverse Geocoder| Geolocation enrichment              |


## 🚀 How to Run

1. Clone the repository
2. Open Microsoft Fabric and create a new workspace and Lakehouse
3. Use the provided notebooks to:
   - Fetch data from the API
   - Perform transformation steps
4. Connect Power BI to the Gold Layer table to build your own visuals

