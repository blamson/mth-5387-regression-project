# Math 5387 - Linear Regression Analysis - Final Project

The goal of this project is to take publicly available data, analyze it, and use that data to create a multiple linear regression model.

# Research Question

My goal is to find variables that are linked with **injuries** in car accidents specifically as that may help us gain some insight into the main things putting Colorado drivers at risk behind the wheel.

# Main Dataset

For this project I opted to use Colorado car accident data pulled directly from the Colorado Department of Transportation [found here](https://www.codot.gov/safety/traffic-safety/data-analysis/crash-data). The data I'm using includes a variety of information relating to car accidents in each county from 2021-2023.

## Directory

All of the tables related to this primary dataset are found in the `data/car_accidents` directory. This directory includes 3 files.

1.  A smaller joined version of the 2021-2023 tables. It features all of the variables I will be considering for this project. Titled `truncated_accident_data.csv`
2.  A data dictionary which describes all of the variables in the original tables. Titled `crash-data-dictionary.csv`
3.  Finally, an aggregated and preprocessed version of this data used for the modeling process. Titled `accidents.csv`

# Supplementary Datasets

On top of that dataset I'm pulling some additional demographic information that I think will be relevant. Pre-processed versions of these tables are all included within the `data/demographic_data` directory.

1.  I pull in county population data from the [Colorado Department of Local Affairs](https://demography.dola.colorado.gov/assets/html/county.html). I need this information so we can look at a variety of metrics while accounting for a counties population.

2.  I pull information relating to the median household income for each county in Colorado from the [National Institute on Minority Health and Health Disparities](https://hdpulse.nimhd.nih.gov/data-portal/social/table?age=001&age_options=ageall_1&demo=00011&demo_options=income_3&race=00&race_options=race_7&sex=0&sex_options=sexboth_1&socialtopic=030&socialtopic_options=social_6&statefips=08&statefips_options=area_states). The information they have is taken from the Census Bureau and is a exactly what I would've wanted to take from the Census data anyway.

3.  Lastly I pull in some out of data information on average commute time per county in Colorado from [opendatasoft](https://hdpulse.nimhd.nih.gov/data-portal/social/table?age=001&age_options=ageall_1&demo=00011&demo_options=income_3&race=00&race_options=race_7&sex=0&sex_options=sexboth_1&socialtopic=030&socialtopic_options=social_6&statefips=08&statefips_options=area_states). This is another source that is simply a cleaned API call from the Census Bureau. This data is from 2017 which isn't ideal but I was having trouble getting this information myself from the Census API and did not have time to refine my search.

# Usage guide

As this is simply a class project I do not have an RENV setup. Installation of necessary libraries is left to the user. All necessary libraries will be at the top of each respective notebook.

All notebooks are intended to be ran top to bottom in isolation. It is recommended, though not necessary, to wipe the local environment variables before running other notebooks. There should be no risk of other notebooks interfering with output, though I make no guarantees of this. However, I do not prioritize consistency in my variable naming in this repository so if one does not take my recommendation your environment namespace will become unwieldy.
