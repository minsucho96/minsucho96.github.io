---
title: How to display ego and surrounding vehicles of CarMaker in ROS-Rviz
author: Minsu Cho
date: 2021-04-17 18:28:00 +0900
categories: [CarMaker, ROS]
tags: [CarMaker, ROS]
# pin: true
---

Overview
========

`Open_street_map`_ is a repository of ROS_ packages for working with `Open Street Map`_ information.

# Get Started


## How to get the open street map (OSM) of region of interest.
You can get your own OSM file in this [site](https://www.openstreetmap.org/).

Simply set interesting region and just export osm file!



## How to display your OSM file in ROS-Rviz.

### Prerequisites

- ROS melodic and Rviz


Step 1) Clone [this package](https://github.com/minsucho96/ROS-Rviz-OSM_Visualization) on your workspace

Step 2) `catkin_make`

Step 3) Store your own osm file in `osm_cartography/maps/`

Step 4) Modify the map file name in osm launch file that located in `osm_catorgraphy/launch/geo_planner.launch`

Step 5) Launch osm_cartography. `roslaunch osm_cartography geo_planner.launch`

# How to change the OSM file
If you want to replace the osm file to your own, put yours in `[YOUR_WORKSPACE]/src/open_street_map/osm_cartography/maps`. 

Then, change the `map_url` in `geo_planner.launch`. Also, you should modify the `tf` arguments  accordingly.

# Results

[Open Street Map of KAIST]
![Open Street Map of KAIST](/figures/osm_fig/osm_kaist.png)

<!-- {:width="350" .normal} -->

[Rviz Visualization]
![Rviz Visualization](/figures/osm_fig/rviz_result.png)

