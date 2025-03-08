# 🚇 DC Metro Ridership Analysis 🚇

## 📌 Project Overview
This project analyzes **Washington, D.C.'s Metro ridership trends** to help transit planners and businesses optimize services and marketing strategies. Using publicly available ridership data, we explore seasonal trends, station-specific traffic, and metro line performance.

## 🔍 Research Questions
We aim to answer the following questions:

### 1️. Overall Ridership Trends (Big Picture for Metro & Businesses)
- What season has the highest overall ridership?
- What months have the highest overall ridership?

### 2. Metro Line Analysis (Broad Perspective → Business Relevance)
- Which metro lines handle the most ridership overall?
- How does ridership fluctuate across metro lines by month?

### 3. Station-Specific Ridership (Metro Service & Business Insights Together)
- What are the **top 10 busiest stations** each month?
- What are the **middle 10 most used stations** each month?
- What are the **10 least busy stations** each month?

### 4. Metro Line & Station Type Analysis (Service & Business Insights Together)
- How is ridership distributed across metro stations and lines over time?
- How many stations of each type (residential, commercial, transfer) exist on each metro line?
- Which station types (residential, commercial, transfer) handle the most traffic?

### 5. Business-Driven Optimization (Closing with Data-Backed Opportunities)
- Can Metro adjust pricing based on congestion?

## 📊 Data Sources & Processing
- **Data Collection:** Raw data obtained from **WMATA Metrorail Ridership Summary** and **WMATA Corridor Data Maps.**
- **Data Processing:**  
  - Cleaned and normalized data for better analysis  
  - Merged relevant columns into structured **dataframes**  
  - Used Python libraries for analysis (e.g., Pandas, Matplotlib, Seaborn)  

## 📈 Exploratory Data Analysis & Visualizations
Key visualizations include:
- **Ridership Trends**: Histogram of average daily ridership by season and month
- **Metro Line Analysis**: Total ridership per metro line, monthly trends
- **Station Ridership**: Line graphs for busiest, mid-range, and least busy stations
- **Station & Line Breakdown**: Heatmaps, bar charts, and pie charts to analyze station types and ridership distribution
- **Business Optimization**: Dynamic pricing model for Metro revenue and congestion management

## ⚙️ How to Run the Project

### Requirements
- **Python 3.x**
- **Libraries**: 
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `numpy`
  - `pypalettes`

### Important Files:
- Advertising_Smart_Pricing_Final.ipynb - Dynamic Pricing Script
- Visualizations.ipynb - Exploratory Data Analysis and Findings

### Datasets:
- **All_Months.csv:** dataset on Average daily entries by station by month for all days of the week in 2024
- **Annual_Station_Boarding_Compiled.csv:** compiled average annual daily entries for all days, weekdays, and weekends in respective order
- **entries_exits_transformed_data.csv:** entries and exits per each day and station in 2024 (numeric only)
- **everyday_2024_w_metro_stations.csv:** entries and exits per each day and station in 2024 merged with metro_stations.csv
- *merged_df.csv:**  merged_df is a result of merging All_Months.csv and metro_stations.csv on Station Name
- **metro_stations.csv:** data regarding location and specs of each metrorail station

## ⏰ Future Implementations/Limitations: 

### 1. **Normalization of `everyday_2024_w_metro_stations.csv`**
- **Objective**: Normalize the `everyday_2024_w_metro_stations.csv` dataset.
- **Benefits**:
  - This would allow us to create an SQL database for storing and querying our data, enabling us to build more complex queries and views.
  - **Tableau Integration**: This normalization would enable us to connect to Tableau to create dynamic data stories.
  - **Mapping Insights**: We would be able to utilize the X, Y, and Address data we have on stations, along with mapping sheets, to create geographical visualizations.

### 2. **Dynamic Pricing Script**
- **Objective**: This script provides a good foundation for future research and the implementation of dynamic advertisement pricing within the metro lines.
- **Future Enhancements**:
  - The current script uses a simple formula to calculate how the base price should be adjusted based on foot traffic and the rolling average foot traffic from the past week.
  - **Data Expansion**: To improve the accuracy of the script, we can add data from previous years (not limited to 2024). More variables such as weather forecasts, event schedules, car traffic, and holiday schedules from previous years could further enhance the model.
  - **Predictive Model**: By incorporating more data, we can develop a predictive model that forecasts foot traffic on any given day, considering all the parameters.
  - **Advertising Optimization**: The refined model could help advertising agencies dynamically adjust the price of advertising at any given time and location within the metro system. This would not only optimize revenue for the metro but also provide valuable insights for clients to understand the best times, stations, lines, and seasons for their advertisements.
  - **Further Expansion**: We could help clients identify not only the right time and day for their advertisements but also the best stations, lines, and times of year that would provide the highest return on investment, based on their target audience and product profiles.

### 3. **Data Accuracy**
- **Objective**: Address and improve data accuracy and reliability for future analysis.
- **Actions**:
  - **Station Type Classification**: The data in the `Station_Type` column of `metro_stations.csv` was generated using ChatGPT based on examples of station types. While this was a useful approach, it may not be entirely accurate, especially for less busy stations with limited published data.
  - **Research on Smaller Lines**: Future efforts should focus on researching smaller metro lines more thoroughly to ensure that the station types are properly assigned.
  - **Standardization**: We aim to standardize the dataset columns (data types, pivoting vs. unpivoting) across CSVs to facilitate easier creation of complex graphs and improve our ability to pair dataframes for more comprehensive analyses.
  - **Utilizing `Annual_Station_Boarding_Compiled.csv`**: This dataset can be used to explore how the time of week (weekdays vs. weekends) and day of the week impact ridership on different metro lines, station types, and throughout 2024.
  - **Geographical APIs**: We could integrate geographical APIs that provide information on events and businesses around stations, helping us understand ridership patterns with more context. This would enable better predictions of trends for 2025 if event data for that year becomes available.

### 4. **Business-Driven Insights**
- **Objective**: Understand the impact of businesses and events around metro stations to help refine advertising and marketing strategies.
- **Actions**:
  - **Event-Based Analysis**: By incorporating data on local events and popular areas around the stations, we can correlate ridership patterns with external factors, improving our understanding of trends.
  - **Target Audience Profiling**: Understanding the businesses around each station and the types of customers frequenting them can help us better profile the personas using the metro. This information would be valuable for advertising strategies.

---

## ⚙️ AI Usage

### AI Programs Used
- **ChatGPT**
- **Microsoft Copilot**


**Dataset Transformation**:
- Help generate/fix scripts to transform the CSVs into dataframes
- Fixing data types
- Normalization/standardization
- Adding and removing columns
- Assigning station types and validating correct line type assignment per station

**Jupyter Notebook/Markdown File Readability**:
- Took inputted text files from Google Docs and reformatted them for readability in markdown syntax

**Python Visualizations**:
- Making Python graphs more visually appealing
- Based on our context and scripts, resolving errors in Python visualizations

**Dynamic Pricing Script**:
- Brainstorming ideas
- Fixing errors in the script
- Coming up with the formula for pricing

## 🛠 Contributors
- **Maya Patel**
- **Illia Polishchuk**
- **Adrien Rozario**
