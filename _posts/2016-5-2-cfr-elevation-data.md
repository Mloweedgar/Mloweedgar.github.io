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

1. Launch GRASS with the following sample data [Grass Sample Data](https://grass.osgeo.org/download/sample-data/)

2. List available raster files from the sample data and load one 
with name lsat5_1987_10.
Execute the following command on the grass console.
<div style="font-style:italic; background-color:#CCC; border-radius:4px; padding:3% 2% 0 3%;">
   d.rast map= lsat5_1987_10
</div>
After this,the following map will be displayed
![Input Map](https://raw.githubusercontent.com/Mloweedgar/Mloweedgar.github.io/master/images/input_map_sm.png)

3. Execute g.region on the input map and it should be ready to run r.hazard.flood procedure.
Here is the command to run on the console
<div style="font-style:italic; background-color:#CCC; border-radius:4px; padding:3% 2% 0 3%;">
r.hazard.flood map= lsat5_1987_10  flood=flood_map mti=mti_map
</div>

The expected output for this example should be 
![Flood Map](https://raw.githubusercontent.com/Mloweedgar/Mloweedgar.github.io/master/images/flood_hazard_map.png)



The following video shows how the whole process of creating a flood map from the given tiff is operated
<a href="http://www.youtube.com/watch?feature=player_embedded&v=1ctU3jJewrk=youtu.be
" target="_blank"><img src="http://img.youtube.com/vi/1ctU3jJewrk=youtu.be/0.jpg" 
alt="HOW TO VIDEO" width="720" height="250" border="10" />
</a>

For more information, please the documentation here [Further Documentation](https://docs.google.com/document/d/1m9cylL7gV9A_O8qL0TEiIkZxqiASeFQYGpKJxjiVFTM/edit?usp=sharing)



### PROGRESS 
I have been able to produce flood hazard maps using grass gis. I have prepared a document that describes step by step how to produce flood maps using grass gis
I have been able to create a python script that can initialize grass session(environment) and hence being able to access grass modules without explicitly starting grass gis. Therefore being able to produce flood maps without using grass gis directly


### CHALLENGES
The most big challenge is the computer processing ability and RAM, this has lead to difficulties in running analysis in maps of size more than 500MB.this has made me rely on sample data set which I obtained from grass gis official website. The data set has raster files with size less than 400MB which my computer could process.
