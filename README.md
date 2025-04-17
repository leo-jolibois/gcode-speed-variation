# gcode-speed-variation

This is a small Python script I made to try and find a solution for reducing the effect of transition phases on glue lines made using a 3D printer modified to be a gluing machine.

The main idea is to be able to  progressively accelerate and decelerate the movements on the XYZ axis of the "printing head" following an acceleration curve in order to balance for the slower pace of glue when starting to push glue down the tube and when releasing pressure.

As of writing this readme, the script is able to break down G0/G1 commands in multiple sub-commands that each have their own speed to allow for modulation of acceleration, while still keeping a constant extrusion speed by breaking down the total amount of extrusion in multiple parts that are proportional to the speed of each sub-command.
