# Extruder calibration

printer.cfg extruder section: max_extrude_only_distance: 100	#This will allow extrude 100mm

Mark 120mm on filament, then:
Terminal:
```
M83
G1 E100 F100
```

Formula: (120-m)/100*c
m = measured filament length
c = step_distance

Example:
measured length: 21.5
step_distance: 0.0104166
(120-21.5)/100*0.0104166 = 0.010260351‬
New step distance: 0.010260351‬