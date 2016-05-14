---
layout: post
title: CfR Elevation Data
published: true
---

## Code for Resilience Elevation Data Integration


### CURRENT STATUS
* Developed a User Interface in Inasafe to facilitate production of flood maps from qgis.

* Integrating the python script which has the codes for producing flood maps in the inasafe repository and make it available in Inasafe plugin  from QGIS.

### HOW TO 

#### STEPS

1. Launch GRASS with the grassdata location and import raster data.
   2015-05-20_tandale_merged_dsm.tif was used for analysis.

    This is the input map for analysis
![Input Map](https://raw.githubusercontent.com/Mloweedgar/Mloweedgar.github.io/master/images/input_map_sm.png)


2. Execute g.region on the input map and it should be ready to run r.hazard.flood procedure. Here is the command to run on the    console
          g.region raster=2015-05-20_tandale_merged_dsm
          r.hazard.flood map=2015-05-20_tandale_merged_dsm flood=flood mti=mti


3.The raster map named flood is the expected output flood map, It can now be displayed to view flood prone areas.


This is the map obtained after analysis 
![Flood Map](https://raw.githubusercontent.com/Mloweedgar/Mloweedgar.github.io/master/images/flood_hazard_map.png)




### PROGRESS 
I have been able to produce flood hazard maps using grass gis. I have prepared a document that describes step by step how to produce flood maps using grass gis
I have been able to create a python script that can initialize grass session(environment) and hence being able to access grass modules without explicitly starting grass gis. Therefore being able to produce flood maps without using grass gis directly


### CHALLENGES
The most big challenge is the computer processing ability and RAM, this has lead to difficulties in running analysis in maps of size more than 500MB.this has made me rely on sample data set which I obtained from grass gis official website. The data set has raster files with size less than 400MB which my computer could process.
