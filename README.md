# inkscape-laser-gcode
inkscape plugin: gcode generation for laser cut/engrave machine


based on J TECH Inkscape Laser Tool Plug-in

https://jtechphotonics.com/?page_id=1980

## this software can,
convert inkscape document into gcode
 * path -> native gcode
 * bitmap -> rasterized gcode

## difference from original one
 * bitmap rasterization function added
 
## how it wokrs
 * path is converted to native gcode using original code
 * bitmap is converted to gcode via web service
 * concate them into one gcode file and save that
