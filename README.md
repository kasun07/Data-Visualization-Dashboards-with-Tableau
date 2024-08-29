# Final-Project-Tableau

## Project/Goals
To understand the behavior of Tableau tool and how to convert a dataset into meaningful visualizations which help to make a conclusion or decision in a business. 

We had to study few datasets and choose one which is comfortable to answer the questions. Studying different datasets were helped to understand the behavior of datasets, discipline and data types. 

I choose the Global Burden of Disease – Causes of Death Diseases in the world dataset. 

The main goal of this project is to analyze the Global Burden of Disease dataset to identify the most significant causes of death across countries, detect trends and patterns, and create insightful visualizations.

Using Tableau, I was able to build few visualizations, including maps, forecasts, line charts and packed bubbles to gain a deeper understanding of the data. The final deliverable is an interactive dashboard that answers key questions, highlights meaningful insights, and provides a data-driven understanding of global mortality trends.

I created my own questions based on the dataset and answered them using visualization. 


## Process
### Analyze the Dataset (Dataset: Cause of Death - Our World In Data)
Basically dataset contains 32 causes for the death of people around the world and it categorized to each countries and also a few regions. They have gathered data from years 1990 – 2019. All together there was 36 columns and 8255 rows. 

36 Columns contain:

      1). Entity
      2). Code
      3). Year
      4). Number of executions (Amnesty International)
      5). 32 causes of death

Note – Please refer to the jyputer Notebook – Dataset EDA.ipynb for the python code in the folder called – Files. 

	In the folder called Files contains following: 
	    Dataset EDA. Ipynb
	    death_cause_add_zero_to_nulls.xlsx
	    death_cause_column_removed.xlsx
	    death_cause_dataset_original.csv
	    death_cause_final_version.xlsx
	    null_values_report.txt
Step 01 – Load the original dataset, death_cause_dataset_original.csv

Step 02 – check the duplicate rows in the dataset and from the code it says there’s no duplicate rows. 

Step 03 – Checked the number of null values for each column and save it to a text file to explore more. File name is ‘null_values_repot.txt’

Step 04 – Based on the null values report, I removed columns - Number of executions (Amnesty International) because it contained 7987 null values. And saved as an excel file, ‘death_cause_column_removed.xlsx’

#### Findings – I realized there were 2048 null values in the column, Code but it was helped me to find the countries out of the whole Entity values. Entity column contains countries and region (continents, formal regions, etc…). Only a country has code, then I was able to create new column called Countries including only countries. (In Tablaeu using calculated field option)

Step 05 – Added zero to all the empty values for each columns except column, Code. (in columns Entity and Year don’t have empty values) There won’t be any issue adding zero because all are numeric values and we can consider as there are zero deaths because of the related cause. Saved as an excel file, ‘death_cause_add_zero_to_nulls.xlsx’

Step 06 – Checked it there are any row where all column values are zero except columns, Entity, Code, Year and it says there are rows with zero values. 

Step 07 – Removed those rows. 

Step 08 – Again checked for rows with zero values, and this time there was nothing. And save as an excel file, ‘death_cause_final_version.xlsx’. This will the version used for the data visualization.

Step 09 - Data Visualization 

## Results
I choose Option 02 and Dataset is Cause of Death - Our World in Data.
### Findings – 
1.	Created new fields combining similar causes for death as below and it helps to understand the patters of the causes of death.
   
I.	Total - Terrorism and Conflict:

        Terrorism (deaths)
        Deaths - Conflict and terrorism
II.	Total - Infectious Diseases:

        Deaths - Meningitis
        Deaths - Malaria
        Deaths - HIV/AIDS
        Deaths - Tuberculosis
        Deaths - Lower respiratory infections
        Deaths - Neonatal disorders
        Deaths - Diarrheal diseases
        Deaths - Acute hepatitis
III.	Total - Non-Communicable Diseases (NCDs)

        Deaths - Neoplasms
        Deaths - Diabetes mellitus
        Deaths - Cardiovascular diseases
        Deaths - Chronic kidney disease
        Deaths - Chronic respiratory diseases
        Deaths - Cirrhosis and other chronic liver diseases
        Deaths - Digestive diseases
        Deaths - Alzheimer's disease and other dementias
        Deaths - Parkinson's disease
IV.	Total - External Causes (Accidents, Injuries, and Violence):

        Deaths - Fire, heat, and hot substances
        Deaths - Drowning
        Deaths - Interpersonal violence
        Deaths - Road injuries
        Deaths - Poisonings
        Deaths - Self-harm
        Deaths - Exposure to forces of nature
        Deaths - Environmental heat and cold exposure
V.	Total - Substance Use Disorders:

        Deaths - Alcohol use disorders
        Deaths - Drug use disorders
VI.	Total - Nutritional and Maternal Causes:

        Deaths - Maternal disorders
        Deaths - Nutritional deficiencies
        Deaths - Protein-energy malnutrition

2.	Created a field called ‘Regions’  including continents  - Asia/ Europe/ South America/ North America/ Africa/ Australasia
3.	Realized in the dataset, England/ Wales/ Scotland/ Northern Ireland are not considered as countries (they don’t have a Code). Instead of having separately those countries, dataset has ‘United Kingdom’ – combining values from each country. 
4.	Created a field called ‘Countries’ including only countries. (Excluding regions and more than one country combinations)

### Questions:
1.	What is the leading cause of death across all countries?
2.	What is the leading cause of death in each country?
3.	What is the leading cause of death in each continent?
4.	What are the top 3 countries that have most number of deaths throughout the years?
5.	If you consider causes of death for the entire world as a distribution (normalized to percentage) then are there countries that have statistically significantly different distributions?
6.	Are there any correlations between causes?
7.	Are there any interesting time trends across years?

### Visualization

1.	World distribution of deaths - map
2.	Deaths by terrorism in countries – bar chart 
3.	Total # of deaths by continent – bar chart
4.	Total # of deaths in each continent filtered by the year – line chart
5.	Total # of deaths by country by each cause – packed bubble
6.	Total # of deaths by year – line chart
7.	Total # of deaths for each country – line chart
8.	Total # of deaths for each country – Treemap
9.	World and each country distribution of deaths


## Challenges 
#### 01.	Data Cleaning and Preparation:

Handling missing or inconsistent data, such as mixed-up country names or null values in the dataset.
Standardizing the Entity column which contained a mix of countries, continents, and other regions.

#### 02.	Feature Selection:

Identifying the most important features out of the 36 available columns.
Deciding which causes of death to focus on and which features provided the most relevant insights for global or country-level analysis.

#### 03.	Visualization Challenges:

Designing effective visualizations that convey the key insights while dealing with a large number of variables.
Building interactive and meaningful dashboards that included maps, forecasting, clustering, and other analytical visuals.

#### 04.	Technical Issues:

Learning and applying Tableau’s calculated fields, filters, and custom visualizations.
Managing performance issues due to the size of the dataset, especially when creating complex visualizations.

#### 05.	Dashboard Design:

Iterating on the dashboard design to ensure it was user-friendly, informative, and answered the key questions identified during the analysis.
Deciding on which visualizations to include and how to layout the dashboard effectively.


## Future Goals
01. Include more granular country-level data or specific regions that were excluded or simplified in the initial analysis.

02. Study the impact of socio-economic factors or healthcare policies on death rates across different regions.

03. Explore the relationship between the number of deaths and population size in each country to gain insights into mortality rates and adjust for population disparities. This analysis could help uncover patterns such as countries with disproportionately high or low death rates relative to their population.

04. Expand the time-based analysis by breaking down the data into more granular periods, such as quarterly trends, to identify short-term fluctuations in death rates. Additionally, enhance the geographic analysis by incorporating state or regional data within each country, enabling a more localized understanding of mortality trends.
