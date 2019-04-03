Outline for Tutorial: 

Overview: 
A brief intro to the purpose and content of this tutorial. Describe the datasets and the packages used. 

Menu: 
List the major steps/tasks (hyperlinks that directly lead the readers to the specific section?) 

Task 1: How to download and visualize species occurrence data? 
Download occurrence data from GBIF
Transform the data to a spatial point data frame
Visualize the data (may need a basemap)
Subset data (based on time/location)

Task 2: How to download and visualize the climate dataset PRISM? 
- Download climate data from PRISM
```
install.packages("prism") #install the package needed to download and process PRISM dataset 
library(prism) #load the package 
options(prism.path = "C:\\Users\\Sarah\\Documents\\Essig_GETITDONE\\PRISM") #set the directory where you want to put the PRISM data 
get_prism_monthlys("ppt", years = 1895:2005, mon = 1:12, keepZip = NULL) #download monthly data for precipitation between 1895 and 2005
get_prism_monthlys("tmin", years = 1895:2005, mon = 1:12, keepZip = NULL) #download monthly data for minimum temperature between 1895 and 2005
get_prism_monthlys("tmax", years = 1895:2005, mon = 1:12, keepZip = NULL) #download monthly data for maximum temperature between 1895 and 2005
get_prism_monthlys("tmean", years = 1895:2005, mon = 1:12, keepZip = NULL) #download monthly data for mean temperature,(tmin + tmax)/2), between 1895 and 2005
ls_prism_data(name = TRUE) #take a look at all the PRISM data downloaded 
}
```
Download climate data from PRISM
Check/assign the projection, resolution, etc. 
Basic plotting 

Task 3: How to match species occurrence with climate variables according to time? 
Match the occurrence data with the PRISM data

Task 4: How to visualize and manipulate land cover data? 
Download land cover data from USGS EROS center 
Import the data to R 
Check the projection, resolution, etc. 
(branch: how to reclassify land cover data)
Visualize the data 

Task 5: How to align multiple datasets to make sure they have the same projection, resoltution, and extent? 
Find the subset of useful land cover data 
Align the data with the PRISM data (projection, resolution, extent) 

Task 56: How to match occurrence with land cover according to time? 
Match the occurrence data with the land cover data 
