# Project to predict Covid19 severity from the known health indicator data within a community

This project utilizes the information from the Center for Disease Controls Behavioral risk factor surveillance system [(BRFSS, 2011-2017)](https://www.cdc.gov/brfss/smart/Smart_data.htm) to determine if Covid19 severity within a community can be predicted from known health indicators. 

# Dataset compilation

The initial code to [review, compile, aggregate health data by metropolitan area](https://github.com/amandakkimball/Health_impact_Covid19/blob/main/Health%20indicator%20data%20by%20MMSA%20region), and [review, compile and merge covid19 data](https://github.com/amandakkimball/Health_impact_Covid19)have been uploaded. 

# Exploratory Data Analysis

The data was further described via a set of visualizations that can be viewed on Tableau Public:

[<div class='tableauPlaceholder' id='viz1607286138420' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Re&#47;RegionalhealthimpactonCovid19severityoutcome&#47;HealthIndicatorsvsCovidOutcomeseverity&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='RegionalhealthimpactonCovid19severityoutcome&#47;HealthIndicatorsvsCovidOutcomeseverity' /><param name='tabs' value='yes' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Re&#47;RegionalhealthimpactonCovid19severityoutcome&#47;HealthIndicatorsvsCovidOutcomeseverity&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en' /><param name='filter' value='publish=yes' /></object></div>](https://public.tableau.com/views/RegionalhealthimpactonCovid19severityoutcome/HealthIndicatorsvsCovidOutcomeseverity?:language=en&:display_count=y&publish=yes&:origin=viz_share_link)

We can see variation overlap in the age category and weight categories, as expected. Age: There is a positive correlation with the high age categories vs the health indicators and negative correlation with the young age categories. Note the high correlation with age 50-60 with regards to covid19 severity 'death_rate', this will prove important in the models.

Health: The health indicators general health bad, cholesterol high, diabetes, heart disease, and to some extent kidney disease are all positively correlated. Surprisingly the smoking population is negatively correlated to the other health indicators. The uninsured regions value being negatively correlated with death rate is also important in the models.

![Correlation Matrix](/images/Correlation matrix.jpg)

Based on this plot, I expect to see age 50-60, normal weight, uninsured, and cholesterol high as important variables in the models.

# Predictive Modeling

Creating a decision tree model with the BRFSS data and using covid19 statistics for each of the regions the most important variables were determined. For the categorical model categories are defined as follows (basis is quartiles of the covid19 death rates):
severe > 2.74%
medium > 1.90%
medium_high > 1.37%
lowest <= 1.37%

To decrease multi-collinearlity in the model only 1 weight characteristic and only 1 age characteristic was used. Overweight and age 50-60 were determined to have the highest importance.  Overweight is shown as more important than normal weight using variable importance for decision tree models.

![rparttree2](/images/rparttree2.jpg)![rparttree](/images/rparttree.jpg)

# Future Research

Further analysis will be to see how this data and model compare to recent covid19 outbreaks. Stay tuned for that analysis at the start of next year.

# References

Kimball, A. (2020a). Health impact for covid19 outcomes. Github. Retrieved from:  https://github.com/amandakkimball/Health_impact_Covid19 
  
Kimball, A. (2020b). Regional health impact on Covid19 severity outcome. Tableau Public. Retrieved from:  https://public.tableau.com/profile/amanda.kimball#!/vizhome/RegionalhealthimpactonCovid19severityoutcome/HealthIndicatorsvsCovidOutcomeseverity 
  
Unknown. (2020a). Coronavirus disease 2019 (COVID-19): United States COVID-19 cases and deaths by county. Centers for Disease Control and Prevention. Retrieved from:  https://covid.cdc.gov/covid-data-tracker/#county-map 
  
Unknown. (2020b). Coronavirus disease 2019 (COVID-19): People with certain medical conditions. Centers for Disease Control and Prevention. Retrieved from:  https://www.cdc.gov/coronavirus/2019-ncov/need-extra-precautions/people-with-medical-conditions.html?CDC_AA_refVal=https%3A%2F%2Fwww.cdc.gov%2Fcoronavirus%2F2019-ncov%2Fneed-extra-precautions%2Fgroups-at-higher-risk.html 
  
Unknown. (2020). 2019 BRFSS survey data and documentation. Center for Disease Control and Prevention: Behavioral risk factor surveillance system. Retrieved from: https://www.cdc.gov/brfss/annual_data/annual_2019.html 
  
Unknown. (2020). Core based statistical areas (CBSAs), metropolitan divisions, and combined statistical areas (CSAs), March 2020. United States Census Bureau. Obtained November 3, 2020 from: https://www.census.gov/geographies/reference-files/time-series/demo/metro-micro/delineation-files.html (Note: Used for separation of county data and CBSA regions) 
  
Unknown. (2020). US obesity trends: County-specific diabetes and obesity prevalence, 2007. American Obesity Treatment Association. Retrieved from: https://www.americanobesity.org/obesityInAmerica.htm 
  
Unknown. (2019) TIGER/Line shapefile, 2019, nation, US, Current metropolitan statistical area/Micropolitan statistical area (CBSA) national: tl_2019_us_cbsa.shp.data.gov retrieved November 4, 2020 from https://catalog.data.gov/harvest/object/7857a9a8-82a8-430d-b3ef-af4ed5141782/html 
  
Unknown. (2017) Smart: City and county survey data: 2017 Data. Center for Disease Control and Prevention: Behavioral risk factor surveillance system. Retrieved November 1, 2020 from: https://www.cdc.gov/brfss/smart/smart_2017.html 

Unknown. (2011-2017) 2011 – 2017 SMART Data and Documentation. Center for Disease Control and Prevention: Behavioral risk factor surveillance system. Retrieved November 1, 2020 from: https://www.cdc.gov/brfss/smart/Smart_data.htm
