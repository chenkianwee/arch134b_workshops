# Multi-Zone-Part 1: 

## Setting Multiple Zones
Bring up a Brep component. Right click on the Brep component to reveal a dropdown and select "Set Multiple Breps."
```{image} ../_static/multizone/multizone2_1.png
:width: 100%
:align: center
```
<br/><br/>

In Rhino, select the closed polysurfaces you wish to be your desired zones. Then press Enter when done.
```{image} ../_static/multizone/multizone2_2.png
:width: 100%
:align: center
```
<br/><br/>

The zones referenced in the Brep will show up red. Check if the Brep is set by clicking on the Brep (turns green), hovering mouse over Brep (list of referenced Breps), or clicking on "Manage Brep collection."
```{image} ../_static/multizone/multizone2_3.2.png
:width: 100%
:align: center
```
<br/><br/>

Connect the Brep to a new component called "HB Intersect Solids." For multi-zone/room energy models, this is a must have. It takes in a list of HB Rooms closed Breps (polysurfaces) and recognizes 
