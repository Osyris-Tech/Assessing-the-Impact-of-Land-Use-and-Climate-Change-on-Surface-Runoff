# Assessing the Impact of Land Use and Climate Change on Surface Runoff

This repository contains the Python code and instructions necessary to replicate the analysis presented in the "Assessing the Impact of Land Use and Climate Change on Surface Runoff Response Using Gridded Observations and SWAT+" paper using the Osyris Replicate python package. The analysis focuses on the SWAT+ model and high-resolution gridded data to analyze the impacts of land use and climate change on surface runoff in African catchments, demonstrating the significant influence of land use changes over climate change on runoff and advocating for improved land management to mitigate potential increases in runoff-related issues.

## Steps to Replicate the Analysis

### Getting started
Install and import the package

`pip install osreplicate`\
`from osreplicate import Paper`

### Access the paper you want to replicate
Provide the papers alias to start analyzing

`analysis = Paper('hydrology/Surface Runoff Response Using Gridded Observations')`

### Get the datasets
Locally download any available datasets associated with this paper

`analysis.get_data()`

### Replicate the paper
Automatically run the full analysis on the available datasets and reproduce the figures from the paper

`analysis.run()`

### Mix and match      
Access core analysis methods from to the paper

`analysis.stratified_random_sampling_gridded_data(data, num_stations)`\
`analysis.train_urban_occurence_nn(land_use_data, driving_factors)`\
`analysis.simulate_land_use_flus(initial_map, future_map, driving_factors, restrictions)`
`analysis.evaluate_rcm_performance(rcm_data, reference_data)`
