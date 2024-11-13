# hydropower-inflow-generator

This repository contains a workflow for easily generating hydropower inflow data. The current version does not differentiate between RoR and reservoir hydropower. The workflow is almost exclusively based on [atlite](https://github.com/PyPSA/atlite). 

## Requirements

The workflow requires some data to run:
1. A shapefile for the geographical location studied.
    * European shapefiles can be download from [eurostat](https://ec.europa.eu/eurostat/web/gisco/geodata/statistical-units/territorial-units-statistics)
2. Historical hydropower data, to normalise the annual data
    * Available from [EIA](https://www.eia.gov/international/data/world/electricity/electricity-generation) 
3. Weatherdata
    * Such as [ERA5 data from ECMWF](https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5) for the year studied. 

## Running the workflow 

1. Clone the repository
2. Install Snakemake from the conda environment
    * I recommend creating the environment from workflow/envs/environment.yaml
3. Adjust the config file with the proper paths, studied years and geographical regions. 
    * config/config.yaml
4. Run the snakemake workflow `snakemake -c 1`