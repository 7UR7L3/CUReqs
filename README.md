# CUReqs
CU Course Prerequisite Viewer

https://7ur.it/CUReqs/ \
~~(try with https://htmlpreview.github.io/?https://github.com/7UR7L3/CUReqs/blob/master/index.html)~~ \
^ apparently htmlpreview doesn't load javascript or something damn.


---

## what this is:

Prerequisite viewer for i.e. easier planning of courses. Directly sources from i.e. https://catalog.colorado.edu/courses-a-z/csci/ for a given department, parses the requirements of the classes in that department, and uses https://github.com/magjac/d3-graphviz with some custom css / javascript to present the requirements interactively.

![preview image](https://i.vgy.me/dxDNhc.png)


## to implement:

- selection of department
- different colours for each _and_ section
- improve highlighting to fully pass through _or_'s
- clicks popup with more information i.e. descriptions
- include toggles for what info is displayed in each bubble
- style _or_'s to be smaller and styled differently
- exporting as svg or png of a given size
- include toggle for only showing classes taught in a given term (maybe possible to query classes.colorado.edu)


## to optimize:

- merge dom elements into reqsparsed
- set properties / data attributes of dom elements to avoid query selectors
- trust .children tbh if setting properties is too expensive or something