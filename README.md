# Steepness in San Francisco: Wheelchair Acccessible?
This project was done for USP4 at UCSD, using the GIS (Geographic Information Systems) software ArcGIS. 

# Summary

![](https://havengroupsf.com/wp-content/uploads/2016/02/12132783813_6b2e77890a_z.jpg)

San Francisco is well known for its hilly geography and steep inclines. Thus, assessing the city's topography is crucial to understanding the pedestrian wheelchair accessibility in certain parts of the city. This project is intended to provide maps that can be useful for the tourists who have difficulty navigating on steep terrain, such as the elderly, or wheelchair users. 

This project uses several complex methods in terms of spatial joining and conversion of contour line to gradients.
![](sidewalk_steepness.png)

# Introduction
San Francisco is well-known for its hilly geography and steep streets.
Maps about its steepness will give insight about how to navigate it for tourists who have difficulty with steep terrain, like the elderly and handicapped people.

* https://data.sfgov.org/Energy-and-Environment/Elevation-Contours/rnbg-2qxw
  * An elevation contour line map of San Francisco

![](pictures/sf3Dstreethill.png)
# Process - Base Map
* All maps were re-projected as NAD_1983_StatePlane_California_III_FIPS_0403
* Made a discrete steepness map 
  * Steepness raster conversion 
    * Topo-to-Raster
    * Slope
    * Int, Raster_to_Polygon
    * Field calculator
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




