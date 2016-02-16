# HE3D-DLT180-Kossel-delta-3d-printer-firmware
Firmwre and some basic tips for the HE3D DLT-180 Kossel delta 3d printer

This firmware is distributed ready for compilation and upload by the Arduino IDE.  As the Arduino IDE requres that the sketch name be the same as the containing folder name I was required to implement that structure in this repository.

The files that should concern most users are the Configuration.h and COnfiguration_adv.h files and they will need to be modified to suit your printer settings.

The primary values tht you need to cocnern yourselves with are as follows:

#define BAUDRATE 115200
#define MANUAL_Z_HOME_POS 203   //This should be the actual height of your nozzle from the hot bed.

#define PLA_PREHEAT_HOTEND_TEMP 180
#define PLA_PREHEAT_HPB_TEMP 70
#define PLA_PREHEAT_FAN_SPEED 255   // Insert Value between 0 and 255

#define ABS_PREHEAT_HOTEND_TEMP 225   //Nozzle extrusion tempereture (usually between 210C and 240C)
#define ABS_PREHEAT_HPB_TEMP 110      //Hotbed tempreture (Usually between 90C-120C)
#define ABS_PREHEAT_FAN_SPEED 255

Another value tht you may be affected by is the "DELTA_RADIUS".  The Delta radius can be used to compensate for variations in your hot bed straightness.  The rule is as follows:

If the nozzle touches the centre point but not the outside points = The hot bed is CONVEX - Adjust down the DELTA_RADIUS e.g.: from 2.0 to 1.0

If the nozzle touches outside points but not the centre point = CONCAVE - Adjust up the DELTA_RADIUS e.g.: from 2.0 to 3.0

Best of luck,

Rick Ruggiero
email: rick.ruggiero@gmail.com
