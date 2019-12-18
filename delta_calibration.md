# Klipper delta calibration:

## Basic with probe:
=================
V2 probe offset: 16.8 (Reference: https://github.com/MarlinFirmware/Marlin/tree/2.0.x/config/examples/delta/Anycubic/Kossel)

Add to the printer.cfg. After this, you can do basic delta calibration with the original probe.

[probe]
pin: ^ar18 #Original Trigorilla board
z_offset: 16.8
samples: 3

[delta_calibrate]
radius: 115
horizontal_move_z: 20

#To "printer" section (just for manual calibration, aka "paper test"):
minimum_z_position: -5


-------------------------------------------------------------------------------------------------------------------------------

## Enhanced:
=========
(Reference: https://github.com/KevinOConnor/klipper/blob/master/docs/Delta_Calibrate.md)
Print delta_calibrate.stl (low speed, eg.: 40), and measure it CCW, started from A:

#Center and outer pillars distance
DELTA_ANALYZE CENTER_DISTS=
#Outer pillars distance
DELTA_ANALYZE OUTER_DISTS=
#Center pillar widths
DELTA_ANALYZE CENTER_PILLAR_WIDTHS
#Outer pillar widths
DELTA_ANALYZE OUTER_PILLAR_WIDTHS=
DELTA_ANALYZE SCALE=1.0
DELTA_ANALYZE CALIBRATE=extended
SAVE_CONFIG
