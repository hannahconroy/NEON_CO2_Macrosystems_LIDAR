# NEON CO2 Macrosystems Final Project


By: Hannah Conroy 

## Background
Knowledge of meta-ecosystem carbon transport is limited and many large uncertainties remain in estimates of biosphere carbon cycling, sources, and sinks. In particular, terrestrially derived CO2 from respiration in soils, geochemical weathering, and stream metabolism all contribute to net CO2 emissions from inland waters, but their relative contributions to meta-ecosystem carbon fluxes are not well-quantified across seasons or biomes.  This research will quantify multi-scale properties of watershed carbon cycling by linking ecosystem processes with meta-ecosystem carbon fluxes in watersheds that have varying terrestrial productivity, soil carbon stocks, climate, geology, and hydrologic regimes. 

To aid in this research, it will be important to understand the total biomass, the gross primary production, and the net primary production at each site. The National Ecological Observatory Network (NEON) conducts airborne remote survey over 47 field sites through out the United States. The surveys are supported by the NEON Airborne Observation Platform (AOP), a collection of instruments installed into a light aircraft designed to collect high resolution remote sensing data at low altitude. The remote sensing data will be used to answer some of the research questions of interest. 

The research will be conducted at five NEON sites across the United States selected to represent a range of climate, hydrological, and productivity regimes. The sites include an aquatic monitoring station co-located with a terrestrial monitoring station: 

|Aquatic Site     | Terrestrial Site           | Location  | NEON Descriptor<sup>1</sup> (Aquatic/Terrestrial)
| :------------- |:-------------| :-----| :---------
| King Creek      | Konza Prairie | Kansas | KING/KONZ
| Walker Branch      | Oak Ridge National Labratory | Ohio | WALK/ORNL
| Como Creek     | Niwot Ridge | Colorado | COMO/NIWO
| Martha Creek      | Wind River Experimental Forest | Washington |  MART/WREF
| Caribou Creek      | Caribou-Poker Creeks Research Watershed | Alaska | CARI/BONA

<sup>1</sup>Used to download data off the NEON database for each site.

## Problem Statement 
This project will attempt establish the differences between the five sites in terms of terrestrial carbon transport. Specifically, I hope to answer: 
* What is the total biomass at each site? 
* What is the net primary productivity at each site? 
* What is the gross primary productivity at each site? 

## The Data 
Datasets you will use (with links, if available)
Neon collects multiple data sets with their Airborne Observation Platform (AOP). The data is processed at different levels and includes a discrete and full-waveform lidar to provide 3-D information about the landscape and an imaging spectrometer to allow discrimation of land cover types and vegetation. I will look at the following data for this project:

Elevation - LiDAR 
https://data.neonscience.org/data-products/DP3.30024.001 

Fraction of incident photosynthetically active radiation (fPAR) 
https://data.neonscience.org/data-products/DP2.30014.001

Leaf area index (LAI)
https://data.neonscience.org/data-products/DP2.30012.001

Vegetation indices - NDVI - Normalized ratio of NIR and IR bands
https://data.neonscience.org/data-products/DP2.30026.001

MODIS Gross Primary Productivity (GPP) / Net Primary Production (NPP)
https://modis.gsfc.nasa.gov/data/dataprod/mod17.php

## The Tools
The NEON website provides a variety of tools and methods for working with the LIDAR data on their site. While most of these tutorials are in R, they will be useful for working with the data of interest and bring me closer to my expected outcomes. 
https://www.neonscience.org/resources/learning-hub/tutorials

I plan on using the python packages numpy, pandas, gdal, matplotlib, and os. 

## Methodology
To compute biomass, I will use the LIDAR data to derive the canopy height values from lidar data. I will create a mask layer of all vegetation points to segment the watershed. 

## Expected outcomes
The project will answer the questions in the problem statement with maps for total biomass, net primary productivity, and gross primary productivty at each site. 

## References
https://data.neonscience.org/ 
https://modis.gsfc.nasa.gov/data/dataprod/mod17.php
