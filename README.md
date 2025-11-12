# Graduate Capstone

Independent research project focused around information architecture, inspired by the shortcomings of Apple and Samsung’s mobile weather apps, which include data like moon phases but omit ocean tidal information, requiring a separate web browser to look up high and low tide patterns. <br/><br/>

As a result, the project has worked to build a Python application to automate the integration and analysis of structured information by incorporating custom functions for JSON and CSV parsing and transformation, and customized output handling to support multiple access methods. 


## Background

The effects of climate change are to only increase. Coupled with the impacts of other human caused issues, our environment is to continue facing extreme and variable patterns that will be life altering. Thus, it’s important the public has easily accessible access to the real-time data that’s gathered globally to stay informed and allow them to plan accordingly to their current or sought out location.

Real-time environmental data is collected from a variety of different sources and locations, only some of which can actually be easily found and understood by the general public. Yet, none provide a consolidated overview of the information. This is especially true for oceanic data, which at this time has yet to be fully integrated into traditional weather applications. Navigating between fragmented data sources can be difficult for the average user. It requires time and patience finding sites that not only hold the correct information they seek in relation to the desired location, but also an intuitive format that makes sense and doesn’t require special downloads or software.

As a result, this project organized, structured, and labeled traditional weather information from atmospheric resources and integrated new data from oceanic resources to centralize the information for users. To accommodate the fragmented data across government agencies, universities, research institutions, and other organizations, the platform will use schema mapping to draw data from its various structured information sources. Consequently, presenting the information systems into a unified, accessible format with features that allow users to quickly and easily, access an enhanced weather overview for their desired area.

The information presented in this project can be used in fields like web design, app development, user experience (UX) design, and content strategy.


### Current Applications

<img align="right" width="300" height="330" alt="Image" src="https://github.com/user-attachments/assets/4586b5aa-3417-4062-8d67-077be8ddb54e" />
The Weather Channel provides hourly, 5-day, and 10-day atmospheric forecasts. With more specialized readings of flu risk predictions from the CDC like influenza, allergy tracking of pollen density in the air, and air quality assessments of pollutions related to ozone, carbon monoxide, nitrogen dioxide, particulate matter less than 10 microns, particulate matter less than 2.5 microns, and sulfur dioxide. The Weather Channel also offers a radar map to visualize rain, snow, and fog, and a search feature to find locations globally by city (“Weather Forecast and Conditions,” 2025). <br/><br/><br/><br/><br/>

<img align="right" width="300" height="400" alt="Image" src="https://github.com/user-attachments/assets/58115b0e-3a15-46a6-bc4f-8ee1f9586946" />
AccuWeather provides similar information plus a health and activity feature, a global severe weather map, and a few live coverage weather notifications on the top of the site’s navigation bar. The health and activity feature allows you to view a bar graph of how the weather will impact certain health conditions like arthritis, migraines, asthma, and sinus pressure. As well as, monitoring pest levels like mosquitos, garden care like mowing and composting, and other outdoor activities like fishing and pool days which give readings of cloud cover, rain, UV index, and wind (“Beach & Pool,” 2025). <br/><br/><br/><br/><br/><br/><br/><br/>

<img align="right" width="300" height="400" alt="Image" src="https://github.com/user-attachments/assets/3a945041-fbf5-4b49-8c23-090c5211c32b" />
The National Oceanic and Atmospheric Administration (NOAA)  has a National Weather Service site that is more simplified but less intuitive than the other applications. It offers a U.S. image loop radar map of tornados, severe thunderstorms, flash floods, special marine, and snow squall across the country. Additionally, it includes a static U.S. map of 30 weather warnings and advisories that could be showcased via different colors on the map (“National Weather Service,” 2025). <br/><br/><br/><br/><br/><br/><br/><br/>

<img align="right" width="300" height="308" alt="Image" src="https://github.com/user-attachments/assets/3cdaa004-ac53-4097-b815-6292e5a70c6f" />
Web application Earth, provides a non-traditional layout. The site seems more intuitive given its clean user interface which lacks any navigation bar or featured news articles seen in the other popular sites provided. However, it may be less legible for the general public who aren’t familiar with certain data points like what the speed of an ocean current is and what dictates it as normal or not. While Earth allows users to navigate to different areas, it doesn’t provide a location search feature to ensure an accurate pinpoint of an area (“Earth,” 2025). <br/><br/><br/><br/>


## Overview
The repository contains a new portable information structure. The structure compiles atmospheric data (seen in current weather apps) and oceanic data (available only on government agency sites). To make the data more portable, several sources have been integrated by combining them into one JSON structure. This was completed through schema mapping by matching IDs/keys so that technical users can better understand the information and easily apply the structure to their application. <br/>

### Data Sources:
+ NOAA ocean buoy data map, list, guide, and description - https://www.ndbc.noaa.gov/ / https://www.ndbc.noaa.gov/data/latest_obs/latest_obs.txt / https://www.ndbc.noaa.gov/docs/ndbc_web_data_guide.pdf / https://www.ndbc.noaa.gov/faq/measdes.shtml <br/>
+ NOAA CO-OPS api - https://tidesandcurrents.noaa.gov/api-helper/url-generator.html / https://api.tidesandcurrents.noaa.gov/api/prod/ / https://api.tidesandcurrents.noaa.gov/api/prod/#requestResponse
+ NOAA CO-OPS sensor observations - https://opendap.co-ops.nos.noaa.gov/ioos-dif-sos/ <br/>
+ NOAA CO-OPS station list - https://api.tidesandcurrents.noaa.gov/mdapi/prod/webapi/stations.json / https://opendap.co-ops.nos.noaa.gov/stations/stationsXML.jsp <br/>
+ EPA air quality observations - https://docs.airnowapi.org/webservices <br/>
+ NOAA NWS weather api - https://www.weather.gov/documentation/services-web-api / https://api.weather.gov/ <br/>

**Potential Sources For Later Integration:**
+ NOAA real-time data file list - https://www.ndbc.noaa.gov/data/realtime2/ <br/>
+ NOAA global monitoring data map - https://viz.pmel.noaa.gov/osmc/?color_by=platform_type&platform_code=PTAW1 <br/>
+ NOAA NCEI natural hazards - https://www.ngdc.noaa.gov/hazel/view/hazards/tsunami/runup-data?sourceMaxYear=2025&sourceMinYear=2008&typeMeasurementId=2&country=USA&area=CA&locInclude=SAN+DIEGO / https://www.ncei.noaa.gov/maps/hazards/?layers=0 / https://www.ngdc.noaa.gov/hazel/view/swagger#/ <br/>
+ NOAA tide and current data - https://tidesandcurrents.noaa.gov/map/ / https://tidesandcurrents.noaa.gov/products.html <br/>
+ NOAA tide and current prediction error - https://tidesandcurrents.noaa.gov/noaacurrents/assets/docs/Tidal_Current_Prediction_Uncertainty.pdf <br/>
+ NOAA currents prediction data - https://tidesandcurrents.noaa.gov/currents_info.html / https://tidesandcurrents.noaa.gov/education/tech-assist/training/user-guides/assets/pdfs/Current_Predictions_User_Guide_v5.pdf <br/>
+ NOAA PORTS active current stations - https://opendap.co-ops.nos.noaa.gov/axis/webservices/activecurrentstations/response.jsp?format=html / https://tidesandcurrents.noaa.gov/cdata/StationList?type=Current+Data&filter=active <br/>
+ NOAA CO-OPS SOAP Web Services - https://opendap.co-ops.nos.noaa.gov/axis/ <br/>
+ NOAA CO-OPS coastal inundation - https://tidesandcurrents.noaa.gov/inundationdb/ / https://api.tidesandcurrents.noaa.gov/dpapi/prod / https://tidesandcurrents.noaa.gov/api-helper/url-generator.html <br/>
+ NOAA CO-OPS tsunami capable tide stations - https://tidesandcurrents.noaa.gov/tsunami/# <br/>
+ NOAA CO-OPS main observational data resource hub - https://opendap.co-ops.nos.noaa.gov/ / https://opendap.co-ops.nos.noaa.gov/axis/ <br/>

## Methods
1. Download the Python Notebook file "OceanWeatherApp.ipynb" and import into Google Colab. Or, navigate to the preview section of the github file and click the link at the top labeled "Open in Colab."
2. From there you can run the application, view the executed code, and access the new structured JSON files.
