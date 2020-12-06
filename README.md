# Project to predict Covid19 severity from the known health indicator data within a community

This project utilizes the information from the Center for Disease Controls Behavioral risk factor surveillance system (BRFSS, 2011-2017) to determine if Covid19 severity within a community can be predicted from known health indicators. 

**This is a work in progress.** 

The initial code to review, compile, aggregate by metropolitan area, and merge have been uploaded. Here is the correlation plot for that data, as a teaser.

![Correlation Matrix](/images/Correlation_plot.jpg)

<!DOCTYPE html>
<html>

<head>
    <title>Basic Embed</title>
    
    <script type="text/javascript" src="https://public.tableau.com/javascripts/api/viz_v1.js"></script>
    <script type="text/javascript">
        function initViz() {
            var containerDiv = document.getElementById("viz1607286138420"),
                url = "https://public.tableau.com/views/RegionalhealthimpactonCovid19severityoutcome/HealthIndicatorsvsCovidOutcomeseverity?:language=en&:display_count=y&publish=yes&:origin=viz_share_link",
                options = {
                    hideTabs: true,
                    onFirstInteractive: function () {
                        console.log("Run this code when the viz has finished loading.");
                    }
                };
            
            // Create a viz object and embed it in the container div.
            var viz = new tableau.Viz(containerDiv, url, options); 
        }
    </script>
</head>

<body onload="initViz();">
    <div id="vizContainer" style="width:800px; height:700px;"></div>    
</body>

</html>

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
