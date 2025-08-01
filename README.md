# COVID-19 Impact Analysis
📌 Project Overview
This project analyzes the global impact of COVID-19 across different countries using real-world datasets from Kaggle.
The analysis covers:

Case trends & mortality rates

Government response severity (Stringency Index)

Economic impact (GDP per capita)

Development indicators (HDI)

All data processing, transformation, and visualization were done in Python using Google Colab.

📊 Dataset Details

1️⃣ Raw Data – raw_data.csv
Contains the original COVID-19 dataset with unprocessed country-level statistics, economic indicators, and government response measures.

2️⃣ Transformed Data – transformed_data.csv
Cleaned and structured dataset prepared for analysis.

Key Columns:

Country Code → ISO code of the country

Country → Name of the country

Date → Data record date

Total Cases (TC) → Cumulative COVID-19 cases

Total Deaths (TD) → Cumulative COVID-19 deaths

Stringency Index (STI) → Severity of government response (0–100%)

HDI → Human Development Index (0–1 scale)

GDP Per Capita (GDPCAP) → GDP per person

Population (POP) → Total population of the country

🔍 Data Analysis Workflow
1️⃣ Data Cleaning
Removed unnecessary columns (Unnamed: 9–13) from raw dataset

Fixed column names for better readability (iso_code → CODE, location → COUNTRY)

Removed duplicate rows if any existed

Handled missing values in Stringency Index, HDI, and GDP per capita

Ensured all numeric columns were correctly typed (float instead of object)

Converted Date column to proper datetime format

2️⃣ Data Transformation
Aggregated daily data into country-level summaries:

Average HDI

Average Stringency Index

Average Population

Total Cases

Total Deaths

Manually added GDP Before COVID and GDP During COVID values for top countries

Sorted countries by Total Cases to identify top 10 most affected nations

Created new DataFrame (aggregated_data) for final analysis

3️⃣ Data Analysis
Identified Top 10 countries by total cases and deaths

Calculated global death rate: ~3.6%

Compared GDP per capita before vs during COVID

Analyzed whether Stringency Index correlated with lower case counts

Checked correlation between Total Cases and Total Deaths (positive correlation)

4️⃣ Data Visualization
Used Plotly, Matplotlib, Seaborn, WordCloud, and NetworkX to create:

Bar Charts – Top 10 countries by cases & deaths

Grouped Bar Charts – Comparing cases vs deaths

Pie Chart – % of total cases vs deaths

Colored Bar Charts – GDP Before/During COVID, HDI, Stringency Index

WordCloud – Most frequent countries in dataset

Heatmap – Correlation between cases and deaths

Histogram – Distribution of total cases

Network Graph – Links between case counts and deaths

🔧 Technologies Used
Python → Pandas, NumPy, Plotly, Matplotlib, Seaborn, WordCloud, NetworkX

Google Colab → Development & execution environment

CSV Data Processing → Loading, cleaning, transforming datasets

🚀 How to Run the Project
1️⃣ Clone the Repository

git clone https://github.com/Kishan-Analyst/Covid_19_Impact_Analysis.git
cd Covid_19_Impact_Analysis
2️⃣ Open the Notebook in Google Colab
Go to Google Colab

Click File → Upload Notebook

Select Covid_19_Impacts_Analysis.ipynb

3️⃣ Upload the Datasets
Download raw_data.csv and transformed_data.csv from this repository

In Colab, click the 📂 Files icon → Upload → Select both CSV files

4️⃣ Run the Notebook
Execute the cells one by one to process data, perform analysis, and view visualizations

📈 Example Insights from the Analysis
USA, Brazil, and India recorded the highest total cases and deaths

GDP per capita decreased in all top-affected countries during COVID

Global death rate was approximately 3.6%

Stringency Index did not always directly reduce case counts

Higher HDI countries were still significantly affected
