# Exercise: Mapping Educational Attainment in New York

## Summary

This exercise is an introduction to QGIS. It focuses on mapping some of the educational attainment results from the previous exercise.

## Input Data

There are two input files on the Google drive for the course: **tl_2016_us_county_36.zip**, a shapefile giving the boundaries of New York counties, and **attainment.csv**, a file containing the results from the educational attainment assignment. Variables in the attainment file with prefix `'pct_'` give the percentage of the population in the group indicated by the suffix, such as `'<hs'`. The ratio variable is provided as well. For future reference, the country boundary file was constructed by filtering a Census TIGER/Line shapefile for all counties in the US down to just those in New York state.

## Deliverables

One QGIS project file called **attain.gqz** and two PNG images: one called **map_below_hs.png** that is a heat map of the `'pct_<hs'` variable in `attainment.csv`, and another called **map_ratio.png** that is a heat map of the `'ratio'` variable.

## Instructions

1. Start a new project in QGIS.

1. Add the layer with country boundaries.

1. Use Save As to save the project in the GitHub directory for the assignment under the name `'attain'`. The extension `'.gqz'` will be added automatically. Be sure the file ends up in the directory for the assignment so it will be pushed correctly.

1. Add county name labels and turn on the text buffer around the name. Use 8 point type and turn on show all labels (on the paintbrush tab at the far right of the labels menus).

1. Add the `'attainment.csv'` file.

1. Join `'attainment.csv'` onto the county layer using `'geoid'` as the join key and `'at_'` as the variable prefix.

1. Construct the heat map for `'at_pct_<hs'` using **equal intervals** and 5 classes. Equal intervals works well because the actual values are of interest, not just the relative ranking of the counties (as would be shown by quantiles). You can use any color scheme you like. One good option is RdYlGn on the *Other Color Ramps* menu but with the *Invert Color Ramp* option checked to make green lowest and red highest.

1. Save the project again.

1. Export the map as **map_below_hs.png** and save it in the directory for the assignment.

1. Change the heat map to show `'at_ratio'`. Use **pretty breaks** and 5 classes. Pretty breaks works well here because the divisions between categories fall at relatively round numbers and are hence relatively easy to interpret. You can use any color scheme you like. The RdYlGn color ramp is a good option here as well but without checking Invert Color Ramp so that green is highest

1. Export the new map as **map_ratio.png** to the directory for the assignment.

1. Save the project again.

## Submitting

Once you're happy with everything and have committed all of the changes to your local repository, please push the changes to GitHub. At that point, you're done: you have submitted your answer.

## Tips

+ If you want, you can create the second map by right-clicking on the first county layer, selecting 'Duplicate Layer', and then editing the new layer to match the second set of specifications. If you do that, you should rename the duplicated layer to something more meaningful than the original name with "copy" added. Right click on the name and look for the Rename Layer option. Once you've created the new layer you can switch back and forth between them by clicking on the check box next to the layer name in the Layers Panel.
