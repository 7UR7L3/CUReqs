# CUReqs
CU Course Prerequisite Viewer

https://7ur.it/CUReqs/?dept=csci \
~~(try with https://htmlpreview.github.io/?https://github.com/7UR7L3/CUReqs/blob/master/index.html)~~ \
^ apparently htmlpreview doesn't load javascript or something damn.


---

## what this is:

Prerequisite viewer for i.e. easier planning of courses. Directly sources from i.e. https://catalog.colorado.edu/courses-a-z/csci/ for a given department, parses the requirements of the classes in that department, and uses https://github.com/magjac/d3-graphviz with some custom css / javascript to present the requirements interactively.

![preview image](https://i.vgy.me/dxDNhc.png)


## to implement:

- selection of department (make more explicit with a text field)
- add hovering over edges to highlight that edge and the courses at either end
- add option to highlight descendents too
- clicks popup with more information i.e. descriptions
- include toggle for loading full out-of-department prereq trees too
- include toggles for what info is displayed in each bubble
- have keys dedicated to these toggles, also keys for zoom (or access keys)
- also let the info displayed in each bubble change depending on hover / highlight
- style _or_'s to be smaller and styled differently
- click or double click or a course to focus it / hide everything outside its prereq tree
- exporting as svg or png of a given size
- buttons for zooming in and out
- include toggle for only showing classes taught in a given term (maybe possible to query classes.colorado.edu)
- a way of searching for the courses required of a major / minor if possible (i have no idea how)
- render prereqless courses as a subgraph cluster https://graphviz.gitlab.io/_pages/Gallery/directed/cluster.html (or see packMode and smoothing and repulsiveforce and remincross?)
- different styles
- fix bug in math 1150. dunno how tbh. maybe split into multiple "Requires " sections first
- proper efficient search to focus on a class and only render nodes before and after it (if not even more focussed)
- [ improve highlighting to fully pass through _or_'s ]
- [ support recommended reqs for i.e. atoc ]
- [ different colours for each _and_ section including arrows ]
- [ increase the depth you can zoom in ]
- [ fix the bug of hovering over the or below csci3022 (probably easier to do after optimization/restructuring) ]


## to optimize:

- set properties / data attributes of dom elements to avoid query selectors
- trust .children tbh if setting properties is too expensive or something
- [ see if there's a more efficient mouseover / hover (maybe jquery is worth it) ]
- [ merge dom elements into reqsparsed ]
- [ set styles directly per element ]