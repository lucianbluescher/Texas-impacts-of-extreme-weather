# Environmental Justice analysis of Texas blackouts in Feburary 2021
Lucian Scher
11/11/2025

The purpose of this project is to identify the impacts of the series of storms in Febuary of 2021 that devastated the Houston Texas power grid. The project acomplishes this by estimating the number of homes in the Houston metropolitan area that lost power and investigating whether impacts were disproportionately felt by low-income communities and non-white areas. It also compares night light intensities before and after the first two storms and mapping the homes that lost power.

The entire project can be found and ran in the texas-blackout.qmd. The repository also includes this README and project files. Filepaths can be found in the tree below.

All data can be found in the /data folder and is read in the second code chunk of the qmd file. This project uses four separate data files accessed 11/1/2025 through a data folder provided by course instruction. 

1. Night Lights
    VIIRS (Visible Infrared Imaging Radiometer Suite) data from NASA's LAADS DAAC captures nighttime light emissions. We used cloud-free imagery from February 7, 2021 (before the storm) and February 16, 2021 (during the blackout) covering Houston-area tiles h08v05 and h08v06 in sinusoidal projection.
Source: [NASA Worldview](https://ladsweb.modaps.eosdis.nasa.gov/)
Files: VNP46A1.A2021038.* (Feb 7) and VNP46A1.A2021047.* (Feb 16)

3. Roads
    Highway data from OpenStreetMap via Geofabrik, filtered to the Houston metropolitan area. Used to exclude areas where reduced nighttime lights may indicate lower traffic rather than power outages.
Source: https://download.geofabrik.de/
File: gis_osm_roads_free_1.gpkg

4. Buildings
Residential building footprints from OpenStreetMap via Geofabrik, filtered to houses in the Houston metropolitan area.
Source: https://download.geofabrik.de/
File: gis_osm_buildings_a_free_1.gpkg

5. Socioeconomic Data
Census tract-level data from the U.S. Census Bureau's American Community Survey (2019 5-year estimates) for Texas. Stored as an ArcGIS File Geodatabase with geometry and attributes in separate layers.
Source: [https://www.census.gov/programs-surveys/acs](https://www.census.gov/programs-surveys/acs/technical-documentation/table-shells.html)
Folder: ACS_2019_5YR_TRACT_48.gdb

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
