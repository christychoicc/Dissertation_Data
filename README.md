# Dissertation Data Preparation and Prevalidation

## Data
|Data Type/ Methodology|Dataset|Description|Source|Purpose|
|---|---|---|---|---|
|Google Earth Engine|Landsat 8/9 Collection 2 Level 2|Relevant bands will be used to derive LST, NDVI and NDWI for summer periods|[View Link](https://developers.google.com/earth-engine/datasets/catalog/LANDSAT_LC08_C02_T1_L2)|Obtain Land Surface Temperature (LST), NDVI, NDWI to identify hot/ cool areas|
|r5r|National Public Transport Access Nodes (NaPTAN)|Public transport stops locations|[View Link](https://beta-naptan.dft.gov.uk/)|Stops data used to connect stops data with timetable data for GTFS for r5r|
|r5r|TransXchange Data, Traveline National Dataset (TNDS) via Core FTP|Public transport services (bus, tram, tube) timetable data|[View Link](https://www.travelinedata.org.uk/traveline-open-data/traveline-national-dataset/)|[Convert to GTFS format](https://itsleeds.github.io/UK2GTFS/articles/transxchange.html) with stops data for r5r|
|r5r|Bus Open Data Service|Ready-made GTFS feed for bus timetable|[View Link](https://data.bus-data.dft.gov.uk/timetable/download/)|Avoid errors caused by conversion, tested as Method 2 (as below)|
|r5r|National Rail Timetable Data|Train timetable data to be used alongside public transport services|[View Link](https://opendata.nationalrail.co.uk/)|Train network for GTFS for r5r|
|r5r|OpenStreetMap, Greater London|Road network data in .pbf format|[View Link](https://download.geofabrik.de/europe/united-kingdom/england/greater-london.html)|Road network for r5r|
|Polygons/ Access Points|OS Open Greenspace|Accessible greenspace and its access points (parks, playing fields, etc.)|[View Link](https://www.ordnancesurvey.co.uk/products/os-open-greenspace)|Accessibility routing destination of greenspace access points|
|Polygons/ Boundaries|Lower layer Super Output Areas (December 2021) Boundaries EW BFC (V10)|LSOA boundaries Shapefile|[View Link](https://geoportal.statistics.gov.uk/datasets/2bbaef5230694f3abae4f9145a3a9800_0/explore?location=52.837550%2C-2.489483%2C6)|London LSOA boundaries for aggregating LST, NDVI, NDWI, socioeconomic indicators, accessibility origin destinations|
|Polygons/ Boundaries|Greater London Boundary|Greater London Boundary|[View Link](https://data.london.gov.uk/dataset/statistical-gis-boundary-files-for-london-20od9/)|Filter/ clip boundaries to London|
|Socioeconomic data|Indicies of Multiple Depriviation (IMD 2025)|LSOA-level deprivation indicies for England|[View Link](https://www.gov.uk/government/statistics/english-indices-of-deprivation-2025)|Socioeconomic vulnerability and compare accessibility to cool greenspace across more/ less deprived neighbourhoods|

### GTFS Data
|Method|Conversion File|Dataset and Source|Description|
|---|---|---|---|
|1|converted in: 2_GTFS_Data_Conversion.Rmd, tested in: 4_r5r_Data_Prevalidation.Rmd|As listed above|Found a substantial amount of missing data (100002 errors) (majority of London Tube and Overground) from using NaPTAN and TNDS converted GTFS|
|2|tested in: 5_r5r_Data_Prevalidation2.Rmd|Bus GTFS-ready data directly downloaded from [Bus Open Data Service](https://www.gov.uk/transport/bus-services-routes-and-timetables)'s [All timetables data](https://data.bus-data.dft.gov.uk/timetable/download/); National Rail will be the same as above (include tube)|No errors, some warnings and infos|