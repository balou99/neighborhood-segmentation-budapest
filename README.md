# Data-driven location scouting for ruin pubs in Budapest
### IBM Data Science Professional Certificate - Capstone Project

## Project Overview
This project aims to identify the most suitable district in Budapest for opening a new "ruin pub." While the market in the inner districts (especially the 7th district) is highly saturated, the "ruin pub" concept remains a major attraction for both locals and tourists. This analysis uses a data-driven approach to find a location that balances high tourist traffic with lower operational costs (proxied by real estate prices).

## The Business Problem
The central question of this research: **If an investor wants to open a new ruin pub in Budapest, which of the 23 districts offers the best potential?**

A successful location must meet three main criteria:
1. It should be similar in character to the successful, established "party districts."
2. It should have high tourist activity (measured by guest nights).
3. It should have relatively lower real estate prices to ensure financial sustainability.

## Data Sources
To solve this problem, I integrated data from multiple sources:
* **Foursquare API:** Used to fetch venue data (categories and locations) for each district to understand the local "vibe" and existing competition.
* **Hungarian Central Statistical Office (KSH):** Used to gather 2016 tourism statistics (guest nights per district).
* **Real Estate Market Data:** Average housing prices per square meter were used as a proxy for rental and acquisition costs.

## Methodology
1.  **Data Extraction & Cleaning:** Automated data collection via Foursquare API and processing of KSH Excel files using Python and Pandas.
2.  **Neighborhood Segmentation:** Used **One-Hot Encoding** to transform venue categories and calculated the frequency of venue types per district.
3.  **Clustering:** Applied the **K-means Clustering algorithm** to group districts based on their venue profiles.
4.  **Correlation Analysis:** Investigated the relationship between guest nights, venue density, and price levels.
5.  **Visualization:** Created interactive maps using **Folium** to visualize the clusters and potential locations.

## Key Results
The analysis narrowed down the 23 districts to a specific cluster (Cluster 1) that shares characteristics with the established entertainment hubs. By overlaying tourism intensity and price levels, the study concluded that:

**District 8 (Józsefváros)** is the optimal location. 
* It belongs to the same cluster as the successful 7th district.
* It showed a high number of guest nights.
* Real estate prices remain significantly lower than in the 5th, 6th, or 7th districts, offering a better ROI for investors.

![Budapest Clusters](map_cluster.png)

## Technologies Used
* **Python 3**
* **Pandas & NumPy** (Data manipulation)
* **Matplotlib & Seaborn** (Data visualization)
* **Folium** (Geospatial mapping)
* **Scikit-learn** (K-means Clustering)
* **Foursquare API** (Location data)

---
*Note: This project was completed as the final capstone for the IBM Data Science Professional Certificate.*
