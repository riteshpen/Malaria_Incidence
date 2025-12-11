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


## Interactive Dashboard


- Global Folium map of child mortality

- Choropleth shading by mortality rate

- Clickable markers showing ITN coverage and country context

- Linked-brushing scatterplots (Altair)

- Income-group filters

- Region-level comparisons


To view the dashboard, download the file: malaria_dashboard.html and open it up


## Visualization Tools

- Folium: For geospatial visualizations, emphasizing ITN coverage, malaria-related cases, and child mortality across regions or countries. Folium supports interactive maps with hover popups and color-coded regions. Ideal for highlighting geographic disparities in malaria prevention and outcomes.
- Plotly: Great for interactive charts and dashboards by allowing hovering, paning, filtering, and clicking on data points. It can help highlight relationships between ITN usage, child mortality, and wealth, as well as time-series trends across regions. 
- Altair: Altair is especially important for comparing ITN coverage vs. child mortality across economic groups through linked brushing and interactive visuals. Its grammar of graphics approach makes it optimal to layer multiple datasets and interactions while maintaining clean designs.
- Matplotlib/Seaborn: For static, high-quality visuals, such as boxplots, histograms, etc. These are useful for initial data exploration and providing contextual insights, like summarizing how child mortality varies by ITN coverage or economic groups. The plots can be annotated to make the visualization clear and interpretable. 

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

## Visual Layout

- ITN Distribution Reduces Malaria Transmission: A choropleth map using Folium will visually show countries with their ITN coverage in relation to their malaria transmission. There will be a map of all areas where red indicates higher ITN coverage and light yellow indicates less coverage. Hover tooltips over the markers will show additional information such as child mortality rates, coverage, and descriptive economic statistics. In addition to hovering, there will be zooming and panning. Overall, the visual will be a world map with all countries filled with a corresponding color, information when hovering, and a color-coded legend showing the ITN coverage.  
- Child Mortality Declines with ITN Use: An interactive scatterplot on Plotly will show the relationship between child mortality rates and ITN usage. ITN coverage will be plotted on the x-axis, child mortality rates will be charted on the y-axis, and upon hovering or clicking on the points, additional statistics, such as income group, country, and wealth gap, will be displayed. Additional interactions include panning and filtering data. The color scheme is based on income groups: red (Low Income), green (Lower Middle Income), and purple (Upper Middle Income), with a color-coded legend on income groups.
Economic Disparities Affect ITN Access: An Altair stacked bar chart with economic status on the x-axis and ITN use on the y-axis will show the relationship between economic status and prevention. Upon hovering over a bar, further information about child mortality rates, income status, ITN coverage, and the country will be displayed, with blue representing where ITN coverage corresponds to a poor household and yellow where ITN coverage corresponds to a rich household. The legend is color-coded by economic status. 
- Equitable Distribution is Key for Impact: Using Altair linked brushing scatterplots, side-by-side plots will be used to compare the effect of poorer populations on child mortality rates. Both plots will have the child mortality rate on the y-axis, with one graph showing ITN coverage of the poorest areas and the other showing the wealth gap. Using the brushing feature, specific data points can be compared between the two plots. Upon hovering over the points, further information can be displayed, such as country, income group, etc. The plots will be different colors for different regions of the world (Sub-Saharan, Middle East, etc), and the regions are color-coded in the legend. 
- Wealth Gaps Influence Child Mortality: Using Matplotlib, plot a scatterplot with wealth gap on the x-axis and child mortality rates on the y-axis, coloring points by income groups to show differences across economic levels. Each point represents a country with a clear legend, and the title provides context along with semi-transparent points to improve readability. This layout highlights that countries with larger wealth disparities tend to have higher child mortality rates. The legend is color-coded by income group: red (high income), blue (upper middle income), green (lower middle income), and yellow (low income).

### What/why we used Random Forest?

A tree-based bagging ensemble model that captures non-linear relationships between ITN usage, economic disparities, and child mortality.
This model is well-suited for handling interactions among variables and reducing overfitting through averaging across multiple decision trees. 

It gives us a feature importance ranking to see which feature is the most important when predicting the Child Mortality Rate.
I used the Brier Score as a metric evaluation so we can minimize False Positivies and False Negatives when distributing ITN Betnets to different income groups.
We want to make sure the betnets are being targeted towards lower-income households, as those are the ones with the higher prevalence of malaria. 


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

## Analysis

- Calculated correlation between ITN coverage and child mortality: r = 0.13 (Weak Positive).
- 63 countries analyzed, spanning multiple regions and income groups.
- The highest child mortality rate is 278.2 (South Sudan), lowest is 8.3 (Sri Lanka).
- Average coverage for the poorest quintile is 39.8%, slightly higher than the richest quintile's 39.0%.
- The highest overall coverage is 93.6% (Guinea-Bissau), 95.5% (Niger), and 79.1% (Mali).
- The lowest overall coverage is 0.4% (Pakistan), 1% (Tajikistan), and 1% (Azerbaijan).
- The biggest gaps favoring the rich are 38.0% (Central African Republic), 34.5% (Congo, Dem. Rep.), and 30.7% (Burundi).
- The biggest gaps favoring the poor are -50.8% (Vanuatu), -44.6% (Lao PDR), and -43.3% (Kiribati).


- The overall accuracy is 82%.
- The overall Brier Score is 0.176.
- The ITN coverage importance is 42%.

## Interpretation:

The statistical evidence suggests that increased ITN (insecticide-treated net) coverage does not have a strong or direct relationship with reducing child mortality across the 63 countries analyzed. The correlation between ITN coverage and child mortality is weak (r = 0.13) and not statistically significant (p = 0.32), meaning the data do not support a meaningful linear relationship.

Despite this, the Random Forest model assigns 42% importance to ITN coverage, indicating that ITN usage helps the model differentiate outcomes, but this does not imply causation. Instead, the weak real-world correlation suggests many other socioeconomic variables—such as poverty, infrastructure, healthcare access, conflict, and regional conditions—have a stronger influence on child mortality than ITN coverage alone.

The descriptive statistics reinforce this complexity:

- Child mortality ranges widely (from 8.3 in Sri Lanka to 278.2 in South Sudan).

- ITN coverage varies dramatically by country, with some extreme wealth gaps both favoring the rich and the poor.

- Overall accuracy (82%) and a Brier Score of 0.176 indicate the model performs reasonably well but still reflects significant uncertainty.

Overall, these results imply that prevention measures like ITN distribution cannot independently drive reductions in child mortality. The relationship is multifactorial, and effective policy interventions must account for the broader social and economic environment influencing health outcomes.



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
