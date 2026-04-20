# indian-food-truck-market-analysis-bangalore

## Data-driven analysis of restaurant competition and high-traffic areas in Bangalore to identify the best location for launching an Indian food truck.

---

## Project Overview

This project aims to conduct a data-driven market research analysis to identify the most promising areas in Bangalore for launching an Indian food truck.

The analysis combines structured restaurant data with location-based insights to understand market conditions, competition, and potential customer demand.

The project focuses on Bangalore as a case study, leveraging real restaurant data and external APIs to evaluate where a food truck could succeed.

Key factors analyzed include:

- Restaurant density and competition  
- Customer ratings and satisfaction  
- Pricing patterns and affordability  
- High-traffic areas (e.g., metro stations, tech parks)  
- Indicators of demand and consumer behavior  

---

## Goal

Identify high-potential locations and market opportunities for launching an Indian food truck, and provide actionable insights to support a data-driven business decision.

---

## Scope Limitation

Due to time and data constraints, the analysis focuses on Bangalore as a single case study.

The findings are based on available datasets and may not capture all real-world variables (e.g., permits, operational costs, or real-time foot traffic).

---

## Business Goal

The goal of this project is to evaluate the viability of launching an Indian food truck in Bangalore by analyzing market demand, competition, pricing, and customer preferences.

---

## Problem Statement

Aspiring food entrepreneurs often lack clear, data-driven insights to determine where to launch a food business and how to position it in a competitive market.

In the case of Bangalore, key challenges include:

- identifying areas with strong customer demand  
- understanding the level of restaurant competition  
- evaluating pricing expectations in different locations  
- identifying gaps in the market for quick-service or street food options  

Without structured data analysis, these decisions are often based on intuition rather than evidence.

---

## Analytical Approach

This project combines two complementary data sources:

- **Zomato dataset**  
  Used to analyze restaurant competition, ratings, cuisine types, and pricing patterns.

- **TomTom API**  
  Used to identify high-traffic hubs such as metro stations and tech parks, representing potential customer flow.

By combining these datasets, the project aims to identify areas where demand and opportunity intersect.

---

## Data Sources

- Zomato Restaurant Dataset (Kaggle)  
- TomTom API (for high-traffic locations)

---

## Methodology

The project follows these main steps:

1. Data Collection  
   - Load Zomato dataset  
   - Extract high-traffic hubs using API  

2. Data Cleaning & Wrangling  
   - Handle missing values  
   - Clean pricing and rating columns  
   - Standardize text data  
   - Filter relevant restaurant categories  

3. Data Analysis (EDA)  
   - Analyze restaurant distribution by area  
   - Evaluate competition density  
   - Analyze pricing and ratings  
   - Identify patterns in customer behavior  

4. Data Combination  
   - Merge restaurant data with traffic hubs  
   - Aggregate data by area  

5. Insight Generation  
   - Identify high-opportunity zones  
   - Detect gaps in the market  
   - Evaluate trade-offs between competition and demand
     


6. POI Identification
   - Queried the `poiSearch` endpoint for **"Tech Parks"** and **"Metro Stations"** to pinpoint high-density lunch and commuter demand zones.
7. Geospatial Filtering
   - Restricted results to a **20km radius** around Bangalore center ($12.9716, 77.5946$) to ensure geographic relevance.
8. Data Extraction
   - Parsed raw JSON response to extract key features:
    * `Name`: Identification of the hub.
    * `Lat / Lon`: Precise coordinates for mapping.
    * `postalCode`: Primary key for dataset joining.
    * `neighborhood`: Secondary key for regional grouping.
9. Key Linking Standardized 
   - `neighborhood` as a string to create a consistent **Primary Key**, enabling a direct join between TomTom demand hubs and Zomato restaurant supply.
10. Gap Analysis 
   - Aggregated the data to calculate the **Opportunity Score**, identifying areas with high hub density but low "Quick Bite" competition.
---

## Insights

#### 1. The Supply-Demand Gap
We found a major mismatch in Bangalore:
* **Saturated Areas:** Places like Koramangala and Indiranagar have 100+ restaurants, making it hard for new trucks to survive.
* **Gold Mines:** Major **Tech Parks** and **Metro Stations** have thousands of people but **zero to five** affordable food options. These are our top targets.

#### 2. Pricing Advantage
The average "Quick Bite" in Bangalore costs **₹300-₹400 for two**. A food truck offering quality meals at **₹150-₹200** per person can easily undercut local restaurants while maintaining profit.

#### 3. Smart Launch Strategy
The data supports a **"Follow the Crowd"** model:
* **8 AM – 10 AM:** Park at a **Metro Station** for the breakfast commute.
* **12 PM – 2 PM:** Move to a **Tech Park** gate for the lunch rush.
This strategy maximizes sales by being where the hunger is, at the right time.

#### 4. Data-Driven Decision
By using the **"Red Line" benchmark** (the city average for competition), we have statistically proven that our recommended sites are safer and more profitable than picking a spot based on intuition.


## Conclusions

## 🏁 Conclusion

This project successfully proves that **Data Intelligence** is more effective than intuition for business expansion. By merging TomTom's demand hubs with Zomato’s supply data, we identified high-traffic "Market Deserts" where a food truck can operate with virtually **zero competition**. 

Our final recommendation provides a low-risk, high-reward roadmap for launching in Bangalore’s tech corridors, ensuring the business is always positioned where the demand is highest and the competition is lowest.
