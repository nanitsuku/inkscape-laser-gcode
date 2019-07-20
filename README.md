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
 * for processing need a specified label explicitly
    * for cut path, label shoud end with 'cut'
    * for engrave object, label should end with 'engrave'
 
## how it wokrs
 * path is converted to native gcode using original code
 * bitmap is converted to gcode via web service
 * concate them into one gcode file and save that

## preparation
 * for cut, convert object( e.g. rect, ellipse ) into path
    * and change label 'cut' or append 'cut' to existing label
 * for engrave, change label 'engrave' or append 'engrave' to exisiting label
 * internet capable to get rasterized gcode
    * to get rasterized gcode from bitmap, uses web service https://img2gco.appspot.com/
    * without bitmap document, no need internet

 ## known issue
 * engrave object should belong to layer
    * use "Layer > Move Selection to Layer..." 