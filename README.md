Zomato Dataset Exploratory Data Analysis (EDA)
This repository contains an Exploratory Data Analysis (EDA) of the Zomato dataset. The analysis is performed using Python with the Pandas, Matplotlib, and Seaborn libraries to inspect the data, uncover patterns, and visualize key insights.

Project Overview
The goal of this EDA is to explore the Zomato dataset to understand the distribution of restaurants, ratings, cuisines, and services across different countries and cities.

Data Loading and Preparation
Datasets: Two datasets were used:

zomato.csv: Contains the main restaurant data, including ID, name, location, rating, and services.

Country-Code.xlsx: A mapping file to link country codes with country names.

Merging: The two datasets were merged into a single DataFrame (final_df) using the Country Code as the common key.

Initial Data Inspection
Shape: The merged dataset contains 9551 rows and 22 columns.

Columns: Key columns include Restaurant Name, Country, City, Cuisines, Aggregate rating, Has Table booking, and Has Online delivery.

Missing Values: A check for missing values revealed 9 null entries in the Cuisines column. A heatmap was generated to visualize this.

Data Types: Data types were inspected, showing a mix of numerical (int64, float64) and categorical (object) data.

Key Analysis and Visualizations
1. Geographical Distribution (Countries)
A pie chart was generated to show the distribution of restaurants across the top 3 countries.

Observation: The dataset is heavily dominated by India, which accounts for 94.39% of all restaurant records. The United States (4.73%) and the United Kingdom (0.87%) are the next two most frequent countries.

2. Ratings Analysis
The Aggregate rating, Rating color, and Rating text columns were analyzed to understand the rating system.

Rating Mapping:

4.5 - 4.9: Excellent (Dark Green)

4.0 - 4.4: Very Good (Green)

3.5 - 3.9: Good (Yellow)

2.5 - 3.4: Average (Orange)

1.8 - 2.4: Poor (Red)

0.0: Not rated (White)

Rating vs. Count: A bar plot of Aggregate rating vs. Rating Count shows two key findings:

A very large number of restaurants (2148) are "Not rated" (0.0 rating).

The majority of rated restaurants fall in the "Average" range (2.5 to 3.4).

3. "Not Rated" Analysis
To understand the high volume of zero ratings, the data was grouped by country.

Observation: The "Not rated" (0.0 rating) entries are almost exclusively from India (2139 out of 2148).

4. Currency Analysis
The analysis identified the currency used by each country in the dataset (e.g., India uses Indian Rupees, UAE uses Emirati Diram, Australia uses Dollar).

5. Online Delivery
The availability of online delivery was analyzed by country.

Observation: Online delivery is primarily available in India and the UAE. Other countries in the dataset do not show "Yes" for this service.

6. Geographical Distribution (Cities)
A pie chart was created for the top 5 cities with the most restaurant listings.

Observation: Similar to the country distribution, the city distribution is dominated by Indian cities. New Delhi alone accounts for 68.87% of the records from the top 5, followed by Gurgaon (14.07%) and Noida (13.59%).

Conclusion
This EDA reveals that the provided Zomato dataset is heavily focused on India. Key insights include:

A significant portion of listed restaurants (especially in India) are "Not rated".

The most common ratings are in the "Average" bracket.

Features like online delivery are not universal and are primarily offered in India and the UAE.

New Delhi is the most represented city by a large margin.

Future Work
The notebook includes an "Assignment" to find the top 10 cuisines, which would be a valuable next step in this analysis. This would involve parsing the Cuisines column (which contains comma-separated values) and aggregating the counts for each cuisine.
