# Texas Blackouts Data Analysis
<img width="772" height="400" alt="image" src="https://github.com/user-attachments/assets/101c2d43-d876-4cfe-ac66-ea08315cb657" />

Image Credits: [Anthony Cappelletti, Texas Winter Storm 2021: Accounting for Subsequent Events](https://www.soa.org/news-and-publications/newsletters/general-insurance/2021/june/gii-2021-06/texas-winter-storm-2021-accounting-for-subsequent-events/)

### Environmental justice geospatial data analysis in R of [Texas's blackouts](https://en.wikipedia.org/wiki/2021_Texas_power_crisis) (Feburary 2021)
Author: Lucian Scher

The purpose of this project is to identify the environmental justice impacts of the series of storms in Febuary of 2021 that devastated the Houston Texas power grid. The project acomplishes this by estimating the number of homes in the Houston metropolitan area that lost power and investigating whether impacts were disproportionately felt by low-income communities and non-white areas. It also compares night light intensities before and after the first two storms and mapping the homes that lost power.

The entire project can be found and ran in the texas-blackout.qmd. The repository also includes this README and project files. Filepaths can be found in the tree below.

## Data
All data can be found in the /data folder and is read in the second code chunk of the qmd file. This project uses four separate data files accessed 11/1/2025 through a data folder provided by course instruction. 

- Night Lights
    VIIRS (Visible Infrared Imaging Radiometer Suite) data from [NASA's LAADS DAAC](https://ladsweb.modaps.eosdis.nasa.gov/) captures nighttime light emissions. We used cloud-free imagery from February 7, 2021 (before the storm) and February 16, 2021 (during the blackout) covering Houston-area tiles h08v05 and h08v06 in sinusoidal projection.

- Roads
    Highway data from OpenStreetMap via [Geofabrik](https://download.geofabrik.de/), filtered to the Houston metropolitan area. Used to exclude areas where reduced nighttime lights may indicate lower traffic rather than power outages.

- Buildings
Residential building footprints from OpenStreetMap via [Geofabrik](https://download.geofabrik.de/), filtered to houses in the Houston metropolitan area.
Source: 

- Socioeconomic Data
Census tract-level data from the U.S. Census Bureau's [American Community Survey](https://www.census.gov/programs-surveys/acs/technical-documentation/table-shells.html) (2019 5-year estimates) for Texas. Stored as an ArcGIS File Geodatabase with geometry and attributes in separate layers.

```
EDS223-HW3
└───README.md
└───Rmd/Proj files    
└─── texas_blackout.qmd
└───.gitignore
    └───data
        └───gis_osm_buildings_a_free_1.gpkg     # Buildings
        └───gis_osm_roads_free_1.gpk            # Roads
        └───ACS_2019_5YR_TRACT_48_TEXAS.gdb     # Socioeconomic
            └───census tract gdb files
        └───VNP46A1                             #Night Lights
            └───VIIRS data files
```

## Acknowledgments 
This project was a homework assignment for the fall 2025 course, Geospatial Analysis & Remote Sensing (EDS 223). A part of the Master of Environmental Data Science (MEDS) program at UCSB's Bren school of Environmental Science & Management. The assigment was created by Ruth Oliver and administered by Annie Adams. I would like to thank them both for this insightful and enjoyable project, and Annie for providing feedback on my analysis. 


‌
