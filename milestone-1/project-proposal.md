# Project proposal

Title: Assessment of environmental fragility in the Tramandaí River basin, RS, Brazil  
Author: Rodrigo Mota (environmental engineer and geospatial analyst)

## Background information

The potential of natural and human resources and the fragility of the environment are premises that must be taken into account during the economic and environmental planning of a territory. In this sense, analytical studies on fragility, which can be expressed through maps and texts, are important documents.

According to the Systems Theory proposed by Tricart, in nature the forces of energy and matter are processed through dynamic equilibrium relations. This balance, however, can be altered by human interventions, generating states of temporary or permanent imbalances. The environments are considered stable when in dynamic equilibrium and unstable when in disequilibrium. Environmental fragility concerns the system's susceptibility to undergo interventions or to be changed. The magnitude of the instability depends on the tension applied to the system and the degree of susceptibility to change in the system itself.

The integrated analysis of environmental systems is based on the principle that they are formed by highly interrelated variables (climate, relief, soils, vegetation cover, etc), each of which has a certain degree of influence on the environment, interfering with more or less intensity.

**This project aims to identify the degree of environmental fragility of the Tramandaí River basin, located in the south of Brazil, through the classification of the system in different levels of vulnerability.** It is hoped with this to recognize and map the areas most susceptible to instability, that is, those that due to their natural characteristics can easily be altered (either due to erosive processes, landslides, silting, floods, etc).

## Potential data sources

In this analysis I will make use of four datasets, which are:

a. Digital Elevation Model (DEM): this data will be used to generate a slope raster of the area. NASA's Shuttle Radar Topography Mission (SRTM) DEM should be fine. The 30m spatial resolution version is available at https://dwtkns.com/srtm30m/.

b. Land Use Cover: MapBiomas project has a great dataset available at http://mapbiomas.org/. It covers all over Brazil in a historical series of 34 years of data (1985-2018). For this case I will be using 2018 layer.

c. Geology: the Brazilian Institute of Geography and Statistics (IBGE) maintains an extensive catalog of statistical and geospatial data related to the country and its territory. The geology data will be used to assess the degree of fragility of the rocks that make up the study area. Available at https://www.ibge.gov.br/geociencias/downloads-geociencias.html.

d. Pedology: just like geology, the study of soils is important to assess places with greater susceptibility to alteration. For example, some types of soils are more susceptible to erosion, landslides and silting. These data are also available at IBGE catalog.

## Planned methods

For each variable (class) within the themes (slope, land use, geology and pedology), dimensionless values will be empirically assigned for the expected degree of fragility (ranging from 1 to 3; 1 being equivalent to low fragility and 3 being equivalent to high fragility).

After evaluating the variables, each of the thematic maps will be rasterized for later use in the calculation of environmental fragility.

Due to the fact that the land use layer represents the different types of vegetation cover and the main anthropic uses in the study area, which are determining factors for the balance of the system, greater weight will be given to this component in the equation.

The steepness of the terrain is also an important component within the dynamics of the earth's surface, since the instability resulting from morphogenic processes is a limiting factor for the development of living beings. In this case, a median weight will be given to the slope theme.

The planned weights for the themes are these:

|Theme|Weight|
|-----|-----:|
|Geology|0.15|
|Pedology|0.15|
|Slope|0.30|
|Land Use|0.40|

The final information plan for environmental fragility in the Tramandaí River basin will be obtained using the “Raster Calculator” tool and will be the result of the following equation:

**Environmental Fragility = Geology x 0,15 + Pedology x 0,15 + Slope x 0,30 + Land Use x 0,40**

The results will be classified like this:

|Value|Fragility|
|-----|-------------------|
|Between 1,0 and 1,3|Very low|
|Between 1,4 and 1,7|Low|
|Between 1,8 and 2,2|Regular|
|Between 2,3 and 2,5|High|
|Equal or higher than 2,6|Very high|

## Expected results

Due to the wide variety of ecosystems found in the Tramandaí River basin, it is expected that the result of the analysis will also present different degrees of environmental fragility.

Without a prior assessment of the data it is very difficult to predict whether the predominance will be of high or low fragility. Anyway, I believe that the data selected for the analysis will be satisfactory to generate a model compatible with reality.
