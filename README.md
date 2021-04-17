# Submarine Volcanic Eruption Detection using Google Earth Engine
## Vanderbilt University 
## Spring 2021 
## Capstone 599
## Linh Nguyen

<hr>

<br>

## Project Description
Submerged volcanic eruptions are difficult to detect however make up a significant number of total eruptions on Earth. A small number of submarines are well documented and monitored due to insufficient detection techniques (Chadwick et al. 2008, 2019
). Although detection of the phenomena is sparse, submerged volcanic eruption is important to marine life by providing nutrients and habitats from hydrothermal & pumice rafts (Black, Mittal, et al. 2020, Bryan et al. 2012). These sparse events are often collected by satellites that orbit the Earth. However detection and monitoring these events are approached by manually investigation of a multitude of sallite images. The approach is tedious and time consuming. Automating this process can significantly reduce the overhead time investment needed to detect submerged volcanic eruptions by filtering the number of images that need to be processed by humans. 

For this project, I focused on using remote sensing in order to build classification models to detect discolored water, a common signial for submerged volcano eruption and hydrothermal vent activity. The detection method utilizes images collected from sallites that orbit the Earth. The satellites collect information over a range of wavelengths (spectral bands). Observations allows different methods to detect and distinguish subaerial and submerged volcanic signals (clouds, ash, ocean discoloration, pumice, etc.) Specifically, for the project I will be using data products from the Sentinel-2 Satellite. 

Google Earth Engine (GEE) was used to conduct the project analysis. Google Earth Engine is a platform for Earth Science data & allows individuals to conduct geospatial analysis of Earth's surface. Utilizing this platform allows individuals to bypass the  infrastructure needed to handle and process the large volume of data. [More information about Google Earth Engine can be found here](https://earthengine.google.com/). 


This project builds upon previous work by Maggie Zheng (MIT) and Tushar Mittal (MIT) utilizing Google Earth Engine to detect discolored water and pumice rafts. 

<hr>

<!-- 
> ## Remote sensing
> 
> ["Remote sensing is acquiring information from a distance via the use of remote sensing satellites and aircrafts"][1]


[1]: [https://earthdata.nasa.gov/learn/backgrounders/remote-sensing][1]
-->


## Project Goals
The project goals are as follows:

1. Utilizing top of atmosphere reflectance bands to build a classification model to discriminate between:
   > - Discolored water
   > - Normal water
   > - Light clouds
   > - Heavy clouds
2. Build additional classification models that utilize surface reflectance bands.
3. Automatically classify the area of Kavachi over several years of data.

<hr>

## Methodology

### Data collection:
Training, validation, and testing data points were collected by hand utilizing's rectangular selection tool. The tool allows user to select different regions within the satellite image that can be utilized for data pre-processing. 
> Training points were collected in the region of Rabul which is located north east of Papa New Guineau. Each class was manually collected from a training area.
> 
> Validation points were also collected in a region of Rabul. These points were collected in a validation area that was not close to the training area.
>
> Test points were collect at the Kavachi submerged volcano. These points were not close to the region of Rabul.

An important note to make is that since training, validation, and testing points were manually created and therefore bias is introduced. The metric of 'accuracy' used to rank and compare the models is subjective since not all points within the training, validation, and testing regions was manually classified. The main reason that each point within the regions were note classified is because GEE has a computational limit that is allowed for each individual. 

