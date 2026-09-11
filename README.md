# PROJECT: SAKAY

![AWS Glue DataBrew](https://img.shields.io/badge/AWS%20Glue%20DataBrew-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Amazon SageMaker](https://img.shields.io/badge/Amazon%20SageMaker-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Gemini API](https://img.shields.io/badge/Gemini%20API-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

Predictive crowd management web application for Mindanao's public transport terminals

## How to Run the Program

To run this project locally, follow these steps to start both the backend and the frontend.

### Server-Side (Python/FastAPI)
1. **Navigate and Run:**
   ```powershell
   cd server
   uvicorn main:app --reload

2. **Verify: Open your browser to the local link**. 
    It should display:
   ```text
   {"message": "AHP Server is Online"}
   ```
    Add these to the browser local link above to check the endpoints
     
    `/analyze`: View raw calculation results.

    `/map-data`: View raw school dataset.


### Client-Side (React/Vite)
1. **Navigate and Run:**
   ```text
   cd client
   npm run dev

2. **Access: Open the local URL** (usually `http://localhost:5173`) to view the site.

---

## Key Features
**Interactive Map & Layers**
   * Hazard Visualization: View **Active Faults** (Red Broken Lines) and **Major Rivers** (Blue Thick Lines).
   * School Exposure Markers: 50 schools (10 per province; 5 Public/5 Private) color-coded by exposure: 🟢 Low | 🟡 Moderate | 🔴 High

**Control Panel**
   * Run AHP Analysis: Dynamically run an analysis based on toggled hazard layers.
   * Exposure Summary: Live tally of results across the region.
   * Top 10 Rankings: A list of the schools with the highest exposure indexes. Clicking a school name automatically zooms the map to its location.

---

## Data Sources & Methodology

This project utilizes geospatial data from various government and open-source providers. To maintain a lightweight repository, raw GIS files (Shapefiles, original CSVs) are hosted externally.

| Data Type | Source | Format |
| :--- | :--- | :--- |
| School Locations | DepEd / Open Data PH | GeoJSON / CSV |
| River Networks | NAMRIA / Humanitarian Data Exchange | Shapefile |
| Regional Boundaries | PSA / GADM | Shapefile |

### Proof of Process
You can access the raw, unclipped datasets and the QGIS project files used for data preparation here:
**[Download Raw GIS Data (Google Drive)](https://drive.google.com/drive/folders/1RItRtYV2x-UkKXj6-ocxIhM2aU3BbYc9?usp=sharing)**
