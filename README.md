# **The Impact of Malaria Prevention Measures on Child Mortality**

<img width="304" height="333" alt="Image" src="https://github.com/user-attachments/assets/b8c55108-c866-4531-8309-f590bc4155e2" />

Child mortality is a major global health issue, with malaria as one of the leading preventable causes of death for children under five. 
Preventive measures, such as insecticide-treated bed nets (ITNs) and indoor residual spraying (IRS), are promoted by global organizations like UNICEF and WHO. 
This project examines whether more access to these measures correlates with lower child mortality across countries. 
Additionally, we aim to examine changes in malaria-related cases over time to determine whether the prevalence of malaria is decreasing, stable, or showing spikes in recent years.



This project investigates the relationship between Insecticide-Treated Nets (ITNs) and child mortality rates across countries of varying income levels and regions.

<img width="320" height="319" alt="Image" src="https://github.com/user-attachments/assets/c82b4252-5cb8-4e82-a111-5b53a6992275" />

Our goal was to determine whether ITN coverage is associated with lower child mortality and how these patterns differ across economic and regional contexts.
We hypothesize that higher access to prevention measures is associated with lower under-five mortality, controlling for socioeconomic factors.

### What datasets did we use?

1. UNICEF Malaria & Child Health Dataset (https://data.unicef.org/resources/dataset/malaria/)
2. World Bank Under-5 Mortality Data (https://data.worldbank.org/indicator/SH.DYN.MORT?)
3. World Bank Incidence of Malaria (https://data.worldbank.org/indicator/SH.MLR.INCD.P3?name_desc=true)

### What is df_latest_by_country.csv, and how did we get it? 

1. df_latest_by_country.csv is the dataset we used for our final evaluation, analysis, and dashboard.
2. We merged both datasets and selected the most recent data entry for every country. 
3. After doing that, we got the df_latest_by_country.csv file.


<img width="611" height="655" alt="Image" src="https://github.com/user-attachments/assets/f04c4a6b-6901-4474-a2c0-7b3157f61ddf" />

## Table of Contents

- Group Members

- Project Overview

- Key Changes From Original Analysis

- Interactive Dashboard

- Visualizations

- Strengths

- Challenges

- Advice for Future Students

- License

## Group Members
*Name	UT EID	Email*

*Ritesh Penumatsa	rp37458	rp37458@utexas.edu*

*Lucy Schilling	lms5598	lucy.schilling@utexas.edu*

*Xinrui Song	xs3979	suszanee@utexas.edu*


## What we focused on:

- Data cleaning and quality assurance

- Interactive geographic and statistical visualizations

- Random Forest modeling

- Subgroup fairness evaluation using Brier Scores

## Analysis
- Calculated correlation between ITN coverage and child mortality: r = 0.13 (Weak Positive).
- 63 countries analyzed, spanning multiple regions and income groups.
- The highest child mortality rate is 278.2 (South Sudan), lowest is 8.3 (Sri Lanka).
- Average coverage for the poorest quintile is 39.8%, slightly higher than the richest quintile's 39.0%.
- The highest overall coverage is 93.6% (Guinea-Bissau), 95.5% (Niger), and 79.1% (Mali).
- The lowest overall coverage is 0.4% (Pakistan), 1% (Tajikistan), and 1% (Azerbaijan).

## Interpretation:

- ITN coverage did not significantly reduce child mortality in the available dataset

- Poorest and Richest households showed similar ITN coverage levels

- 63 countries 

- Removed original claim that ITNs are “the most effective” intervention because no comparison was made with other prevention methods


## Interactive Dashboard


- Global Folium map of child mortality

- Choropleth shading by mortality rate

- Clickable markers showing ITN coverage and country context

- Linked-brushing scatterplots (Altair)

- Income-group filters

- Region-level comparisons


To view the dashboard, download the file: malaria_dashboard.html and open it up


## Visualizations


Below are selected key visuals extracted from the analysis.

### World Mortality Map 

<img width="886" height="640" alt="Image" src="https://github.com/user-attachments/assets/d3138ec8-23a7-4844-ad81-5913f774da00" />

### ITN Coverage vs. Child Mortality

<img width="886" height="424" alt="Image" src="https://github.com/user-attachments/assets/7d2041fb-d2ad-4eba-afd3-75ef4d39d902" />

### ITN Coverage by Wealth Group

<img width="888" height="382" alt="Image" src="https://github.com/user-attachments/assets/84768fa1-a503-432f-a44d-ce447226a519" />

### Random Forest Feature Importance and Brier Score: Subgroup Comparison

<img width="882" height="436" alt="Image" src="https://github.com/user-attachments/assets/f1af12a1-b973-4d21-b4be-19e62a103bc6" />
<img width="879" height="344" alt="Image" src="https://github.com/user-attachments/assets/5848ace2-d3e5-4792-a320-886baa59397d" />

## Strengths

- Built validated economic and health indicators enabling cross-country comparison

- Identified meaningful disparities and trends across regions and income levels

- Created intuitive, interactive visualizations for deeper exploration

- Used ML (Random Forest) to extract feature importance and predictive insights

- Evaluated model fairness with subgroup-level Brier Scores

- Communicated results clearly to both technical and non-technical audiences

- Applied strong data-cleaning practices (range checks, duplicates, dtype validation)


## Challenges

- The dataset skewed toward low-income and Sub-Saharan African countries

- Limited data for high-income countries weakened generalizability

- Narrow scope (only ITNs examined) restricted broader conclusions

- Small dataset reduced model prediction reliability

- Hard to extrapolate future patterns due to real-world complexity

  

## Advice for Future Students


- Choose a topic you genuinely care about

- Start early, especially with visualizations and data cleaning

- Secure a reliable dataset as soon as possible

- Ask deeper “why” questions beyond basic trends

- Combine technical analysis with domain understanding


## License
All Rights Reserved

This project is not licensed for reuse.
No code, data, notebook content, or visualizations may be copied, modified, or redistributed without explicit permission from the authors.
