language:
-  en
- es
- et
- gl
- hr
- lt
- ny
- pt
- sl
- uz
- ca
- de
- fr
- id
- it
- lg
- ms
- nl
- 'no'
- pl
- rw
- sr
- sv
tags:
- climate
- environment
- land cover
pretty_name: GLOBE_Data
size_categories:
- 10K<n<100K

- # Dataset Card for Dataset Name

Satellite data from GLOBE Observer, 1995 to 2024. 


## Dataset Details

### Dataset Description

This data is from the GLOBE Observer Data explorer, which originally covers data from 1995 to 2024. Main areas of focus include, date, time, location, and surface conditions. Data contains image URLS from 6 directional angles: north, south, east, west, upward and downward. 



- **Curated by:** Lisa Liubovich, American University
- **License:** NA

### Dataset Sources
https://observer.globe.gov/get-data
https://api.globe.gov/search/swagger-ui.html
https://datasearch.globe.gov/


- **Repository:** https://github.com/lisaml02/adoptapixelF24 


## Uses

### Direct Use
- environmental monitoring and analysis
- geographic information systems (GIS) analysis
- temporal analysis and seasonal studies
- urban planning and resource management
- climate change studies
- ecology and biodiversity research
- data calibration and validation for remote studies

Machine Learning applications:
  - image processing/classification
  - anomaly detection
  - clustering
  - remote sensing


### Out-of-Scope Use

- real time weather forecasting
  - The dataset likely contains historical or periodic measurements of surface conditions, latitude/longitude, and local times, rather than the real-time meteorological data (e.g., atmospheric pressure, temperature, wind speed) needed for live weather forecasting.
  - Real-time weather forecasting requires a continuous feed of high-frequency meteorological data, often sourced from weather stations, satellites, and radars, which goes beyond the data collected in this dataset.
- urban planning for infrastructure development
  - lacks detailed urban data such as zoning regulations, building codes, population density, and infrastructure information.
  - Urban planning requires highly detailed and localized data on transportation networks, utilities, land use, and human activity patterns, which are not represented in this dataset.
- individual-level health studies
  - The dataset primarily focuses on geographic and environmental variables, without including individual-level health data (e.g., health records, demographics, physical activity data).
  - Studies aiming to link environmental factors to health outcomes (e.g., respiratory conditions, physical activity) require detailed, sensitive information about individuals and their exposure to various environmental conditions over time.
- detailed economic analysis
  - The dataset does not include economic indicators (e.g., GDP, income levels, market prices) or data on human economic activities (e.g., agriculture production, trade, commerce).
  - Detailed economic analysis, especially at a micro or macro level, typically requires data sources like economic surveys, market prices, business activity logs, and financial records.
- social and behavioral studies
  - Social science research often involves studying human behavior, social interactions, and cultural aspects, requiring data on human activities, demographics, communication patterns, and social networks.
  - The dataset is focused on environmental and geographic data, lacking information on human social behavior, demographics, or cultural practices.
- high-resolution biodiversity and wildlife tracking
  - The dataset does not include specific biodiversity indicators (e.g., species counts, wildlife movement data, habitat quality metrics) at the level of detail required for in-depth ecological or wildlife tracking studies.
  - High-resolution wildlife tracking typically requires GPS collar data, camera trap information, or direct field observations, which go beyond the scope of surface conditions and geographic coordinates provided.
- advanced soil and geological analysis
  - In-depth soil and geological analysis (e.g., soil composition, mineral content, rock structure) requires data from soil sampling, core drilling, remote sensing, and geophysical surveys, which the dataset does not include.
  - Detailed geological studies need highly specific datasets focused on subsurface characteristics and soil chemistry.
- Predictive Modeling for Precise Crop Management (Precision Agriculture)
  - Precision agriculture often requires highly granular, real-time data from sensors, drones, soil health measurements, weather forecasts, and even genetic information of crops, which are not covered by the dataset.
  - This dataset, while providing general environmental conditions, may lack the specificity and real-time data feeds required for highly localized and immediate decision-making in crop management.
- Disaster Response and Emergency Management
- Effective disaster response (e.g., for hurricanes, floods, wildfires) requires real-time, high-frequency data (e.g., live satellite feeds, radar data, weather station updates) to make rapid and informed decisions.
  - dataset is more suitable for historical or periodic environmental assessments rather than real-time monitoring needed for disaster management.

## Dataset Structure

Description of columns: 
- organization_id:The GLOBE ID assigned to the school or organization
- org_name: The name of the reporting school or other institution.
- site_id: The GLOBE ID assigned to site.
- site_name: The name assigned to the site where the data were collected; the
name is selected by the reporting person as part of site definition.
- latitude: The latitude of the measurement site. Sites are associated with
the lower-left corner of the 100x100m MGRS grid cell. Range: [-90, 90]. Units: decimal degrees north
- longitude: The longitude of the measurement site. Sites are associated with
the lower-left corner of the 100x100m MGRS grid cell. Range: [-180, 180]. Units: decimal degrees east
- elevation: The elevation of the measurement. Sites are associated with the
lower-left corner of the 100x100m MGRS grid cell. Units: meters above sea level
- measured on:The date only of when the data were observed in UTC. Format: yyyy-mm-dd
- landcover_id: unique ID associated with landcover observation
- data_source: Descriptor indicating whether the data were reported by a
GLOBE Educator via a method other than the app (“GLOBE Data
Entry Site Definition”) or reported from the GLOBE Observer app
(“GLOBE Observer App”)
- measured_at: The date and time when the data were observed in UTC. This is
listed for each protocol returned in ADAT. Format: yyyy-mm-ddTHH:MM:SS
- east_photo_url: url to photo of site from east directional view
- south_photo_url: url to photo of site from south directional view
- west_photo_url: url to photo of site from west directional view
- upward_photo_url: url to photo of site from upward directional view
- downward_photo_url: url to photo of site from downward directional view
- measure_lat: Latitude recorded by the GPS of a participant using the GLOBE
Observer app at the time of measurement. Range: [-90,90]. Units: decimal degrees north
- measure_long: Longitude recorded by the GPS of a participant using the
GLOBE Observer app at the time of measurement. Units: decimal degrees east
- measure_elev: Elevation at the latitude/longitude location recorded by the GPS
of a participant using the GLOBE Observer app at the time of measurement. Units: meters (m) above sea level
- loc_method:Indicates if the measurement location was determined by the
device’s GPS (“automatic”) or if the user supplied it manually
(“manual”)
loc_accuracy: Accuracy of this location within “x” meters. Units: meters (m)
- snow_ice: True/False indicating if this surface condition is present. 0 for not present, 1 for present.
- standing_water: True/False indicating if this surface condition is present. 0 for not present, 1 for present.
- muddy: True/False indicating if this surface condition is present. 0 for not present, 1 for present.
- dry_ground: True/False indicating if this surface condition is present. 0 for not present, 1 for present.
- leaves_on_trees: True/False indicating if this surface condition is present. 0 for not present, 1 for present.
- raining_snowing: True/False indicating if this surface condition is present. 0 for not present, 1 for present.
- are_equal: are measured_at and measured_on equal? Boolean true or false. 
- timezone_offset:Converts the longitude into a time zone offset. Positive values are for time zones east of the prime meridian, and negative values for those west.
- local_time: Adds the offset in hours to the measured_on column to get the local time. Each location’s local_time reflects the actual time experienced at that location.
- lattitude_offset_deg: Directly converts loc_accuracy from meters to degrees of latitude using the constant 111,320 meters per degree
- longtitude_offset_deg: Uses the latitude (measure_lat) to adjust the conversion of meters to degrees of longitude. The latitude is first converted to radians (measure_lat * pi / 180) for the cos() function
- month_day: day and month combination during which observation was recorded; format: dd-mm
- season: season (winter, spring, summer, fall) during which observation was recorded; determined by equinoxes and solsitces
- day_of_year: what number day out of 365 or 366 was the observation recorded on?
- date_outlier: is the date of this observation an outlier? Boolean true or false.
- loc_accuracy_outlier: is this location accuracy observation an outlier? Boolean true or false. 
- hour_of_day: hour of day during which the observation was recorded out of 24 hours
- month: month of year during which observation was recorded
- year: year in which observation was recorded

## Dataset Creation

### Curation Rationale

- make GLOBE data more organized
- create descriptive metadata for future users

### Source Data

GLOBE Observer

#### Data Collection and Processing

Data was cleaned and processed in Rstudio
Renamed columns to eliminate spaces
selected exclusively, date, time, location, and sutface condition columns
filtered out incomplete data
Packages used: tidyverse, dplyr, ggplot2, magick, lubridate, httr


## Bias, Risks, and Limitations

- lack of surface condition data before development of GLOBE App in 2018
- Spatial and Temporal Bias: The dataset may have an uneven geographic distribution (e.g., urban vs. remote areas) and temporal skew (e.g., more data collected in specific seasons or years), limiting the generalizability of analyses across different regions and times. Variations in data accuracy, particularly in location precision (loc_accuracy), can introduce errors in spatial analysis.
- Data Quality and Measurement Limitations: Measurement errors, missing data, and varying precision in latitude/longitude can lead to biased conclusions. High loc_accuracy values indicate less precise measurements, potentially skewing results in environmental modeling or spatial analyses. The dataset may lack certain environmental variables (e.g., soil type, vegetation cover) crucial for comprehensive studies.
- Sampling and Observer Bias: Data collection might prioritize easily accessible locations (e.g., near roads, urban areas) or involve human judgment (e.g., visual assessment of surface conditions), introducing sampling and observer biases. This skews the dataset toward specific regions or perspectives, potentially overlooking critical environmental variations.
- Lack of Sociotechnical Context: The dataset focuses on geographic and environmental factors with limited human, cultural, or economic context. This omission can bias analyses of human-environment interactions and fail to account for sociotechnical influences such as agricultural practices or land-use changes.
- Dynamic Environmental Changes: The dataset represents conditions at specific points in time, potentially missing ongoing changes like climate shifts, urban development, or land use alterations. Analyses assuming static conditions may produce outdated or biased predictions.
- Ethical Considerations: Geographic data may include sensitive locations (e.g., private lands, conservation areas), raising concerns about privacy and ethical use. The potential misuse of this data for surveillance or exploitation underscores the need for careful handling and ethical compliance.


### Recommendations
Improve Data Representativeness: Expand data collection to underrepresented regions and seasons, and regularly update the dataset to capture recent changes, reducing spatial and temporal biases.

Enhance Data Quality: Use high-precision GPS tools for accurate measurements and employ advanced imputation methods for missing data to minimize spatial errors and preserve natural variability.

Use Robust Analysis Techniques: Identify and handle outliers in geographic and environmental data and employ context-aware models (e.g., seasonal time series) to mitigate temporal biases.

Integrate Additional Data: Supplement the dataset with sociotechnical information (e.g., human activities, land use) and remote sensing data to provide a more comprehensive understanding of environmental interactions.

Address Ethical Concerns: Anonymize sensitive locations, obtain necessary permissions for data use, and ensure compliance with privacy guidelines to prevent misuse of geographic data.

Communicate Uncertainty: Always report location accuracy and document the dataset's limitations to inform users of its scope and appropriate applications.

Users should be made aware of the risks, biases and limitations of the dataset. More information needed for further recommendations.



## Dataset Card Authors 

Lisa Liubovich, American University

## Dataset Card Contact

Lisa Liubovich: ll3540a@american.edu, lisamliubovich@gmail.com

