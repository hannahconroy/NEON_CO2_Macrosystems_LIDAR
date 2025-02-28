# NEON CO2 Macrosystems Final Project
Exploring terrestrial carbon transport at five sites across the United States managed by the National Ecological Observatory Network.

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
* What is the biomass averaged by area at each site? 
* How does the biomass at each site change from year to year? 

## The Data 
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

I plan on using the python packages numpy, pandas, gdal, matplotlib, and os. I will also use the neonUtilities package - a package developed by NEON in R. To use this in python, I will use the rpy2 package. 

https://www.neonscience.org/resources/learning-hub/tutorials/neon-utilities-python

## Methodology
To compute biomass, I will use the LIDAR data to derive the canopy height values from lidar data. I will create a mask layer of all vegetation points to segment the watershed and then determine individual trees. I will use the method described in the following link to define predictor variables based on the properties of the trees in the watershed (area, diameter, maximum tree height, and minimum tree height). Biomass will be calculated according to formulas in Jenkins et al. (2003). This will result in a plot of the biomass at each site as well as a mass of total biomass weight. 

https://www.neonscience.org/resources/learning-hub/tutorials/calc-biomass-py

To gain an understanding of net and gross primary productivity, I will map the fPAR, LAI, and NDVI datasets available on the NEON site as well as the MODIS GPP/NPP dataset available from NASA. The CASA model has been used to estimate NPP and GPP from Lidar and climate data, althought this may be out of the scope of this project. I hope to use these data sets to at least gain a broad understanding of what is going on at each site.  

## Expected outcomes
The project will answer the questions in the problem statement with maps for total biomass, net primary productivity, and gross primary productivty at each site. The project will also compare outcomes of each site to each other to gain a broad understanding of the terrestrial transport of carbon in each watershed. 

## References

Jenkins et al. 2003. “Comprehensive Database of Diameter-based Biomass Regressions for North American Tree Species.” Forest Science. 

Gader, P. , 2020. “Calculate Vegetation Biomass from LiDAR Data in Python” https://www.neonscience.org/resources/learning-hub/tutorials/calc-biomass-py

NEON (National Ecological Observatory Network). Ecosystem structure (DP3.30015.001). https://data.neonscience.org (accessed March 12, 2021)

