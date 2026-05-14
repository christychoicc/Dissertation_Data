# Dissertation Data

## Data
|Data Type/ Methodology|Dataset|Description|Source|Purpose|
|---|---|---|---|---|
|Google Earth Engine|Landsat 8/9 Collection 2 Level 2|Relevant bands will be used to derive LST, NDVI and NDWI for summer periods|[View Link](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C02_T1_L2)|Obtain Land Surface Temperature (LST), NDVI, NDWI to identify hot/ cool areas|
|r5r|National Public Transport Access Nodes (NaPTAN)|Public transport stops locations|[View Link](https://beta-naptan.dft.gov.uk/)|Stops data used to connect stops data with timetable data for GTFS for r5r|
|r5r|TransXchange Data, Traveline National Dataset (TNDS) via Core FTP|Public transport services (bus, tram, tube) timetable data|[View Link](https://www.travelinedata.org.uk/traveline-open-data/traveline-national-dataset/)|Convert to GTFS format with stops data for r5r|
|r5r|National Rail Timetable Data|Train timetable data to be used alongside public transport services|[View Link](https://opendata.nationalrail.co.uk/)|Train network for GTFS for r5r|
|r5r|OpenStreetMap, Greater London|Road network data in .pbf format|[View Link](https://download.geofabrik.de/europe/united-kingdom/england/greater-london.html)|Road network for r5r|
|Polygons/ Access Points|OS Open Greenspace||[View Link](https://www.ordnancesurvey.co.uk/products/os-open-greenspace)|Accessibility routing destination of greenspace access points|
|Polygons/ Boundaries|Lower layer Super Output Areas (December 2021) Boundaries EW BFC (V10)|LSOA boundaries Shapefile|[View Link](https://geoportal.statistics.gov.uk/datasets/2bbaef5230694f3abae4f9145a3a9800_0/explore?location=52.837550%2C-2.489483%2C6)|London LSOA boundaries for aggregating LST, NDVI, NDWI, socioeconomic indicators, accessibility origin destinations|
|Socioeconomic data|Indicies of Multiple Depriviation (IMD 2025)||[View Link](https://www.gov.uk/government/statistics/english-indices-of-deprivation-2025)|Socioeconomic vulnerability and compare accessibility to cool greenspace across more/ less deprived neighbourhoods|
