# 🗺️ Google Maps Scraper

A Python-based Selenium scraper to collect business and point-of-interest (POI) data from **Google Maps** around a given location.  

This script automates searching multiple categories (e.g., banks, hospitals, hotels, etc.), extracts details, and exports them to CSV.

---

## 📖 Project Overview

This project is a **Python-based web automation tool** that uses **Selenium** to scrape **Google Maps** for business and point-of-interest (POI) data around a specified location.  

Instead of manually searching for businesses like *banks, hotels, hospitals, schools, restaurants*, and copying their details one by one, this scraper automates the entire process.  

You provide:  
- A **location** (e.g., `"Sankaraperi, Tamil Nadu 628002"`)  
- A list of **categories** (e.g., `"Bank"`, `"Hospital"`, `"Hotel"`, `"School"`)  

The script will:  
1. Search Google Maps for each category near that location.  
2. Automatically scroll through all the results to load every place.  
3. Visit each place’s page and extract details such as:  
   - ✅ Place Name  
   - ✅ Google Maps Category (as shown in Maps)  
   - ✅ Address  
   - ✅ Phone Number  
   - ✅ Website  
   - ✅ Latitude & Longitude (parsed from the Maps URL)  
   - ✅ Business Status (Active, Temporarily Closed, Permanently Closed)  
   - ✅ Reviews Count  
   - ✅ Direct Google Maps URL  
4. Save everything into a structured **CSV file** for easy analysis.  

---

## 🛠️ Why is this useful?

- **Market research** → Find all businesses in a region.  
- **Competitor analysis** → See what types of shops/facilities exist nearby.  
- **Data enrichment** → Collect address/phone data for CRM or GIS systems.  
- **Geospatial analytics** → Use latitude/longitude in mapping & GIS tools.  

---

## 📊 Example Use Case

If you run this script for:  
- Location: `"Sankaraperi, Tamil Nadu 628002"`  
- Categories: `["Bank", "Hospital", "School", "Hotel"]`  

It will produce a CSV with rows like:  

| Name            | Search Category | Google Category | Address                | Phone      | Website                | Latitude_URL | Longitude_URL | Status             | Reviews Count | Google Maps URL    |
|-----------------|-----------------|-----------------|------------------------|------------|------------------------|--------------|---------------|--------------------|---------------|--------------------|
| Canara Bank     | Bank            | Bank            | Main Road, Sankaraperi | +91-123456 | https://canarabank.com | 8.73456      | 77.89456      | Active             | 45            | maps.google.com/... |
| Apollo Hospital | Hospital        | Hospital        | XYZ Nagar, Sankaraperi | +91-987654 | https://apollo.com     | 8.73567      | 77.89567      | Temporarily Closed | 230           | maps.google.com/... |

---


