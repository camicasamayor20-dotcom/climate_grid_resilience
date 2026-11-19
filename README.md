Extreme Weather and Power Outages Across U.S. Counties

Capstone project for the YSE Environmental Data Science Certificate. Author: Camila Casamayor.

Project description

Climate-related hazards such as heavy precipitation and high winds can damage electric power infrastructure and leave customers without service. This project looks at historical relationships between extreme weather and power outages across U.S. counties, as a first step toward understanding infrastructure vulnerabilities and informing climate resilience and adaptation planning for electric grids.

The analysis matches county-level outage records with severe weather observations from 2014 to 2022.

Research questions

What is the relationship between extreme weather conditions, such as heavy precipitation and high winds, and power outage frequency across U.S. counties?
How does outage frequency vary across counties and time periods experiencing different weather conditions?
If suitable data are available, are extreme weather conditions associated with unusually high utility repair or maintenance expenditures?

Objectives

Combine county-level outage records with severe weather event data for the same counties and time periods (2014–2022).
Compare outage frequency during severe weather events with outage frequency during other periods.
Map and chart the geographic and temporal distribution of outages and their relationship with extreme weather.
Identify areas where weather hazards and frequent outages coincide.
If suitable data are found, test whether extreme weather is associated with higher utility repair or maintenance spending.
Build a foundation for future work connecting observed vulnerabilities with climate projections and utility adaptation planning.

Scope

Geography: United States, at the county level, because of the availability of public data. Argentina may be considered if suitable datasets are found.
Time period: 2014–2022, matching the coverage of the outage dataset.
Final scope will depend on data coverage and resolution.

Data
- **`raw_data/[eaglei_outages_raw].csv`**
  - Description: County-level estimates of customers without power at 15-minute intervals, with county identifiers (FIPS) and timestamps, 2014–2022
  - Source: [EAGLE-I Recorded Electricity Outages 2014–2022](https://figshare.com/articles/dataset/The_Environment_for_Analysis_of_Geo-Located_Energy_Information_s_Recorded_Electricity_Outages_2014-2022/24237376) 

- **`raw_data/[noaa_storm_events_raw].csv`**
  - Description: Significant weather events (storms, floods, high winds) with event type, date, location, and reported impacts
  - Source: [NOAA Storm Events Database](https://www.ncei.noaa.gov/access/storm-events-database/)

- **`raw_data/[emdat_raw].csv`** 
  - Description: Major disasters (floods, storms, wildfires) with event type, location, date, and impacts; used for added context on large events
  - Source: [EM-DAT International Disaster Database](https://www.emdat.be/) 

Known data issues

- EM-DAT: location resolution is too coarse for this analysis. The `location` column lists multiple states in a single row, but the analysis needs one state per row. I'm looking for a better-fit disaster dataset to replace it.

Repository structure

climate_grid_resilience/
├── README.md               ← you are here
├── raw_data/               ← original data, never edited
├── scripts/                ← notebooks, numbered in the order they run
├── clean_data/             ← cleaned data
├── metadata/               ← metadata for the datasets
├── outputs/                ← maps, plots, and tables 
└── archive/                ← past versions of files

How to run the code

All scripts are Google Colab notebooks written in R. Run them in number order:

0_project_setup.ipynb
1_data_cleaning_emdata.ipynb

[To be completed as work is done]


Expected results

Maps and charts showing the geographic and temporal distribution of outages.
Comparisons of outage frequency during severe weather events versus other periods.
Identification of areas where weather hazards and frequent outages coincide.

Status and next steps

[x] Set up the project folder and GitHub repository
[x] Download raw datasets (EAGLE-I, NOAA Storm Events, EM-DATA)
[-] Clean (partially done)
[ ] Combine the raw data
[ ] Exploratory maps and plots: outages by county and over time
[ ] Compare outage frequency during severe weather vs. other periods
[ ] Assess availability of utility repair/maintenance expenditure data (Question 3)

AI Disclosure

I used Claude Opus 5.5 as an aid to write my README. The research questions are my own. I identified the datasets myself, and all data cleaning steps were determined on my own. I used Claude as a writing aid to organize my capstone proposal into this README.
