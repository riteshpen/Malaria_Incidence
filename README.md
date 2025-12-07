*The Impact of Malaria Prevention Measures on Child Mortality* 


Group 30
Date: 12/04/2025

Table of Contents

Group Members

Project Overview

Key Changes From Original Analysis

Interactive Dashboard

Visualizations

Strengths

Challenges

Advice for Future Students

License

Group Members
Name	UT EID	Email
Ritesh Penumatsa	rp37458	rp37458@utexas.edu

Lucy Schilling	lms5598	lucy.schilling@utexas.edu

Xinrui Song	xs3979	suszanee@utexas.edu
Project Overview

This project investigates the relationship between Insecticide-Treated Nets (ITNs) and child mortality rates across countries of varying income levels and regions.
We focused on:

Data cleaning and quality assurance

Interactive geographic and statistical visualizations

Random Forest modeling

Subgroup fairness evaluation using Brier Scores

Our goal was to determine whether ITN coverage is associated with lower child mortality and how these patterns differ across economic and regional contexts.

Key Changes From Original Analysis

Used only a Random Forest model instead of four ML models

Updated interpretation:

ITN coverage did not significantly reduce child mortality in the available dataset

Poorest and richest households showed similar ITN coverage levels

Reduced dataset size from 251 → 63 rows by using only the most recent year per country

Removed original claim that ITNs are “the most effective” intervention because no comparison was made with other prevention methods

Interactive Dashboard

The interactive dashboard includes:

Global Folium map of child mortality

Choropleth shading by mortality rate

Clickable markers showing ITN coverage and country context

Linked-brushing scatterplots (Altair)

Income-group filters

Region-level comparisons

To view the dashboard, open the file:

malaria_dashboard.html

Visualizations

Below are selected key visuals extracted from the analysis.

World Mortality Map

ITN Coverage vs. Child Mortality (Plotly)

ITN Coverage by Wealth Group (Stacked Bar Chart)

Random Forest Feature Importance

Brier Score: Subgroup Comparison

Strengths

Built validated economic and health indicators enabling cross-country comparison

Identified meaningful disparities and trends across regions and income levels

Created intuitive, interactive visualizations for deeper exploration

Used ML (Random Forest) to extract feature importance and predictive insights

Evaluated model fairness with subgroup-level Brier Scores

Communicated results clearly to both technical and non-technical audiences

Applied strong data-cleaning practices (range checks, duplicates, dtype validation)

Challenges

Dataset skewed toward low-income and Sub-Saharan African countries

Limited data for high-income countries weakened generalizability

Narrow scope (only ITNs examined) restricted broader conclusions

Small dataset reduced model prediction reliability

Hard to extrapolate future patterns due to real-world complexity

Advice for Future Students

Choose a topic you genuinely care about

Start early, especially with visualizations and data cleaning

Secure a reliable dataset as soon as possible

Ask deeper “why” questions beyond basic trends

Combine technical analysis with domain understanding

License
All Rights Reserved

This project is not licensed for reuse.
No code, data, notebook content, or visualizations may be copied, modified, or redistributed without explicit permission from the authors.
