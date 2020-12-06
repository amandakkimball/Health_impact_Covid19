# Project to predict Covid19 severity from the known health indicator data within a community

This project utilizes the information from the Center for Disease Controls Behavioral risk factor surveillance system (BRFSS, 2011-2017) to determine if Covid19 severity within a community can be predicted from known health indicators. 

**This is a work in progress.** 

The initial code to review, compile, aggregate by metropolitan area, and merge have been uploaded. Here is the correlation plot for that data, as a teaser.

![Correlation Matrix](/images/Correlation_plot.jpg)

<div class='tableauPlaceholder' id='viz1607287359351' style='position: relative'><noscript><a href='#'><img alt=' ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Re&#47;RegionalhealthimpactonCovid19severityoutcome&#47;USHealth&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz'  style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='embed_code_version' value='3' /> <param name='site_root' value='' /><param name='name' value='RegionalhealthimpactonCovid19severityoutcome&#47;USHealth' /><param name='tabs' value='yes' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Re&#47;RegionalhealthimpactonCovid19severityoutcome&#47;USHealth&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='language' value='en' /><param name='filter' value='publish=yes' /></object></div>                <script type='text/javascript'>                    var divElement = document.getElementById('viz1607287359351');                    var vizElement = divElement.getElementsByTagName('object')[0];                    if ( divElement.offsetWidth > 800 ) { vizElement.style.minWidth='800px';vizElement.style.maxWidth='100%';vizElement.style.minHeight='650px';vizElement.style.maxHeight=(divElement.offsetWidth*0.75)+'px';} else if ( divElement.offsetWidth > 500 ) { vizElement.style.minWidth='800px';vizElement.style.maxWidth='100%';vizElement.style.minHeight='650px';vizElement.style.maxHeight=(divElement.offsetWidth*0.75)+'px';} else { vizElement.style.width='100%';vizElement.style.minHeight='1800px';vizElement.style.maxHeight=(divElement.offsetWidth*1.77)+'px';}                     var scriptElement = document.createElement('script');                    scriptElement.src = 'https://public.tableau.com/javascripts/api/viz_v1.js';                    vizElement.parentNode.insertBefore(scriptElement, vizElement);                </script>

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
