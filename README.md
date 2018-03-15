# openscad-extrusionProfiles

This package provides aluminium extrusion profile modules for usage with OpenSCAD.

## Usage Instructions

Follow the [Openscad-Modules](https://github.com/RobertFach/Openscad-Modules) howto use the Openscad-Modules registry.

### Installing the module
```
npm --registry https://registry.openscad-modules.tk install extrusion-profiles
```

### Including the module
```
module XXX {
   include <node_modules/extrusion-profiles/extrusionProfile.scad>
   
}
```

### Parameters
* module extrusionProfile
  * type:
    * positive: draw profile outline
    * boundingBox: draw profile outline bounding box
    * tools: draw profile hammernut screws
  * size
    * "2020": 2020 aluminium extrusion profile
  * length
    * double: length of profile in mm
  * screwDiameter
    * "M4": metric 4mm screw for screw clearance
    * double: diameter of 4mm screw

### Drawing a profile outline for 2020 profile with length 50
```
extrusionProfile(type="positive", size="2020", length=50);
```

### Drawing a bounding box around the module
```
extrusionProfile(type="boundingBox", size="2020", length=10);
```
### Drawing a clearance shape for hammernut screws
```
extrusionProfile(type="tools", size="2020", length=10);
```
