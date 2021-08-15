# Steepness in San Francisco:
This project was done for USP4 at UCSD, using the GIS (Geographic Information Systems) software ArcGIS. 

# Summary
San Francisco is well known for its hilly geography and steep inclines. Thus, assessing the city's topography is crucial to understanding the pedestrian wheelchair accessibility in certain parts of the city. This project is intended to provide maps that can be useful for the tourists who have difficulty navigating on steep terrain, such as the elderly, or wheelchair users. 

This project uses several complex methods in terms of spatial joining and conversion of contour line to gradients.
![](sidewalk_steepness.png)

# Introduction
San Francisco is well-known for its hilly geography and steep streets.
Maps about its steepness will give insight about how to navigate it for tourists who have difficulty with steep terrain, like the elderly and handicapped people.

![](pictures/sf3dstreethill.png)
# Process - Base Map
* All maps were re-projected as NAD_1983_StatePlane_California_III_FIPS_0403
* Made a discrete steepness map 
  * Steepness raster conversion 
  * Steepness ranged from 0° to 52°
  * Categorized and Dissolved everything into 5 (multi-part) polygons for different steepness tier.
![](pictures/base_map.png)

# Process - Secondary Map
* Made 3 maps on using this base map and another shape-files, using Spatial Join
  * Landmarks (Polygons)
    * Spatial Join = “Have Their Center In”
  * Sidewalks (Poly-lines)
    * Spatial Join = “Intersect”
  * Public Transit (Points and Poly-lines)
    * Spatial Join = “Within”
![](pictures/landmark_steepness.png)
![](pictures/sidewalk_steepness.png)
![](pictures/transit_coverage_steepness.png)




