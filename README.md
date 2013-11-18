koo5 fixes what:
CNC-CLUB.ru (.com) Presents
===========================

Component to scan the surface and add compensation
to Z axis to eliminate surfase inflattness.  

Find details at http://www.cnc-club.ru 
(http://cnc-club.ru/forum/viewtopic.php?f=15&t=521&start=220&p=19525#p19525)


Install
===================

Save files to your ini directory. 
Change custom_postgui.hal signal names if needed. 

Add these lines to ini file: 

Into [HAL] section:
POSTGUI_HALFILE = custom_postgui.hal

Into [DISPLAY] section:
PYVCP = comrensation_pyvcp.xml

Operate
===================

1. Scan the surface using Gcode like in scan-surface.ngc
2. Reset component's height map by pressing Reset button at pyvcp panel or throught Gcode
M65 P1 (Reset compenstation)
G4 P1
M64 P1 (Reset compenstation)
G4 P4 (Wait for 4 seconds, just in case)

3. Turn on the compensation by checking Enable check box and prepare to see the magick :)!
Or:
M64 P0  (Turn on the compensation)
