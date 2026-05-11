# ISAT-420 Massanuten Snowfall Group Final Report
## Problem Statement
Climate change is increasingly affecting the weather across the United States. Rising winter temperatures are reducing snowfall events through the winter as well as snowfall totals. The depleted snow cover is creating challenges for ski resorts, particularly on the East Coast, where historically, snowfall was already limited. Resorts like Massanutten have turned to alternative methods like artificial snow making; however, making snow increases operational costs, and the lack of good powdery snow decreases tourists' interest in the resort. To better understand these impacts, it is necessary to analyze long-term snowfall and temperature trends in the Harrisonburg, Virginia region and evaluate how warming winters may be influencing snow reliability at Massanutten Resort.

## Background
The focus of this project is to examine snowfall patterns in the Harrisonburg, Virginia region, with particular attention to how climate change may be influencing snowfall trends at Massanutten Resort. This issue is significant because warming temperatures are increasingly linked to reductions in snowfall and shorter winter seasons across many mid-Atlantic ski areas. As average winter temperatures rise, precipitation that historically fell as snow is more likely to occur as rain, directly affecting both snow accumulation and snowpack longevity.
Research from organizations such as the Environmental Protection Agency indicates that winters in the United States have warmed considerably over the past several decades, contributing to declining snow cover in many regions. Similarly, a report by the National Oceanic and Atmospheric Administration (NOAA) highlights that the southeastern United States has experienced noticeable variability and, in some cases, decreases in snowfall as temperatures trend upward. Additionally, the NY Times recently did an article on the difficulties Western US ski resorts have faced this year due to the recent “snow drought”. For Massanutten as well as resorts in the west, a lack of consistent cold temperatures and natural snowfall can have significant economic consequences. Lack of snowfall and cold temperatures lead to an increased reliance on artificial snowmaking and shorter seasons, which increase operational cost, reduce consumer interest, and shorten the amount of time the resort is open, bringing in revenue.
Overall, understanding the relationship between climate change and snowfall trends in the Harrisonburg area is critical not only for environmental analysis but also for assessing the long-term sustainability and economic viability of local winter tourism.

## Research Questions
To explore the effect warming winter temperatures have on snow, we created three research questions.
1. How has snowfall at Massanutten changed over time?
2. How does snowfall change over time correlate with temperature change?
3. How has the number of days of snowfall per year changed over time?

To understand the effect of global warming on snowfall, we are looking at the local impact at a ski resort that is close to us versus a broader view of the issue. Because the scope of the project is smaller than all US ski areas, the project is localized and focused on giving a good understanding of one area. The core mechanism of the issue is global warming, so we want to see the direct correlation between temperature and snowfall. The number of days with snowfall is important because it shows how much strain the lack of snowfall is putting on the ski areas.
Data and Methods
To address the research questions, multiple climate and snowfall datasets were analyzed to examine long-term temperature and snowfall trends in the Harrisonburg and Massanutten region.

## Datasets:
1. Local Massanutten Station

  This dataset is a short-term, local observation record for Massanutten covering the period from 2016 through 2026. The station ID is: US1VARH0011, indicating that this record is likely a volunteer observer station record distributed through the NOAA daily summaries system. 
The dataset is a CSV file and formatted with one row per day, covering variables including: DATE, PRCP, SNOW, and SNWD, along with station metadata fields. 
In this study, this data is used as recent snowfall observations at the specific location we are looking at. The dataset shows the current snowfall and precipitation conditions at Massanutten. While this dataset is specific to the location of study, it lacks the length of data necessary in order to assess change of snowfall over time. 

2. Daymet point data

  The second dataset used was the Daymet Version 4 R1 gridded climate dataset produced by the Oak Ridge National Laboratory. Daymet provides daily climate estimates on a 1-km grid across North America.
Variables used in this study included: year, yday, prcp (mm/day), swe (kg/m²), tmax (°C), tmin (°C)
The Daymet dataset was used to analyze long-term climate conditions between 1980 and 2024 for both valley and mountain locations near Harrisonburg and Massanutten. Because the Daymet dataset spans multiple decades, it was used to extend climate analysis beyond the shorter local observation record.
[Daymet Dataset] (link : https://daac.ornl.gov/DAYMET/guides/Daymet_Daily_V4.html)

3. NOAA Dale Enterprise Station Dataset

  A third dataset was obtained from the National Oceanic and Atmospheric Administration Climate Data Online archive. Data from the Dale Enterprise station served as a long-term regional proxy for snowfall and winter temperature trends. This dataset spans from 1893 through 2026, providing over 130 years of climate observations. This dataset enabled multi-decade trend analysis of snowfall and winter temperature changes in the region.

## Data Processing
Data processing involved cleaning, organizing, and comparing datasets from multiple sources to evaluate snowfall and temperature trends.
Steps in this process included:
- Aggregate daily snowfall and precipitation observations into annual and winter seasonal totals
- Winter minimum and maximum temperatures were calculated using December through February averages
- Daymet data was extracted for both Massanutten Mountain and Harrisonburg valley locations to compare climate differences associated with elevation
- Correlation analyses were conducted between snowfall totals and winter temperatures
- Overlapping periods between Daymet and local station observations were compared to validate the reliability of the gridded Daymet dataset
Data quality checks included identifying missing values and removing incomplete records where necessary.

## Results
Long-Term Snowfall and Temperature Trends: Analysis of the NOAA Dale Enterprise proxy station showed a long-term decline in annual snowfall totals between 1893 and 2026. Over the same period, winter minimum temperatures displayed a warming trend of approximately 1–2°C.

Snowfall and Temperature Correlation: A correlation analysis between snowfall and winter temperature showed a moderate negative relationship between winter snowfall totals and winter minimum temperatures (r=−0.54). This indicates that warmer winters consistently produce lower snowfall totals. Annual correlations were weaker because summer temperatures do not affect snowfall.
Correlation Results:
Annual Snowfall vs Annual Tmin: -0.29
Annual Snowfall vs Annual Tmax: -0.12
Winter Snowfall vs Winter Tmin: -0.54
Winter Snowfall vs Winter Tmax: -0.54
These results demonstrate that winter seasonal temperatures are much more important than annual averages when evaluating snow reliability.
Validation of Daymet Data: Comparison of Daymet precipitation data with observed local station data during the 2016–2024 overlap period showed a very strong positive correlation (r=0.95). This strong agreement validated the use of Daymet data for longer-term climate analysis in the region.
Valley vs. Mountain Climate Comparison: The analysis also showed that the mountain location near Massanutten receives slightly more precipitation and experiences more below-freezing days than the nearby Harrisonburg valley location. Key findings include: Massanutten receives approximately 5–10% more annual precipitation vs the valley. Additionally, mountain locations experience roughly 5–10 additional below-freezing days per year. These findings suggest that elevation provides some protection against warming temperatures; however, regional climate warming still threatens long-term snow reliability.

## Discussion
This project demonstrates that warming winter temperatures are associated with declining snowfall in the Massanutten region. The analysis supports broader scientific findings that climate change is reducing snow reliability across many ski regions in the United States. As temperatures warm, there are fewer days in the year below freezing, limiting the number of possible days for snow to fall yearly. This directly snowfall, however, when there is accumulated snow, the warming temperatures or possible rain cause snow to melt faster than if the same snow accumulation had happened during a colder season. 
One challenge encountered during the project was locating long-term snowfall data directly from Massanutten Resort. Because the local station records only extended back to 2016, we had to use the Dale Enterprise NOAA station as a regional climate proxy for historical analysis. Although proxy datasets are useful, they may not perfectly represent conditions at higher elevations on the mountain itself. Luckily, we performed a correlation analysis and found that the proxy dataset closely mirrored the data from the Massanutten weather station and, therefore, was valid to use in the study.
From a FAIR data perspective, the datasets used in this study generally adhered to FAIR standards. The data used was findable because it was available through NOAA and Daymet online archives. The datasets used were also accessible. The weather station data was available via CSV, a common file type that most users know how to interact with. However, daymet data was available as a gridded dataset, which takes slightly more expertise to manage compared to other common file types. The data used was also interoperable; each dataset was comparable across GIS, statistical, and spreadsheet software. Because the data was well-documented with metadata, it is easily reusable. However, combining datasets from multiple sources required additional processing to ensure consistency in units and formatting.
If additional time were available, future analyses could include modeling future snowfall under different UN climate change scenarios to understand the impact on the ski industry in each scenario. This could include the evaluation of snowmaking efficiency in each scenario. Other work could include the comparison of Massanutten trends with other mid-Atlantic ski areas or examining the economic impact of shorter ski seasons, which could include the impact of snowmaking efficiency or the loss of revenue based on ticket sales lost due to the date seasons are ending.
Summary and Conclusion
This study examined the relationship between climate change and snowfall trends in the Harrisonburg and Massanutten region using local observations, Daymet climate data, and long-term NOAA records. 
The analysis found that:
Winter temperatures in the region are warming
Snowfall totals have generally declined over time
Warmer winters are strongly associated with reduced snowfall
Mountain elevations provide some protection from colder temperatures and additional freezing days
Daymet data effectively extend short local records for climate analysis
These findings suggest that continued climate warming may threaten the long-term snow reliability and economic sustainability of ski operations at Massanutten Resort.
More broadly, this project demonstrates the importance of combining multiple environmental datasets to investigate climate impacts at local scales. Additionally, this project highlighted challenges involving data quality, consistency, and long-term record availability.
Future research should focus on predicting future snow conditions and identifying adaptation strategies that can help ski resorts remain economically viable under changing climate conditions.
Overall, this project highlights both the usefulness and the challenges of working with environmental datasets to study climate-related problems.

## Works Cited
National Oceanic and Atmospheric Administration National Centers for Environmental Information. (n.d.). U.S. billion-dollar weather and climate disasters: Southeast region. Retrieved from:
NOAA Southeast Climate Disasters Summary
Oak Ridge National Laboratory. (n.d.). Daymet: Daily Surface Weather Data on a 1-km Grid for North America, Version 4 R1. Retrieved from:
Daymet Dataset Documentation
United States Environmental Protection Agency. (n.d.). Climate change indicators: Weather and climate. Retrieved from:
EPA Climate Indicators
United States Environmental Protection Agency. (2021, December 21). EPA’s new report shows how climate change is influencing seasonal events in the U.S. and impacting people’s health and environment. Retrieved from:
EPA Seasonal Climate Report
The New York Times. (2025). Articles discussing western U.S. ski resort snow drought conditions.
