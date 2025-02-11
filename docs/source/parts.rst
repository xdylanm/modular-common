Parts
=====

Here is a listing of common/useful parts in categories. It's easier to design around standard component types.

.. contents::
    :depth: 1
    :local:

Potentiometers
--------------

Potentiometers ("pots") can be categorized by application:

* Internal adjustment: Trim pots are used for internal adjustments and are not accessible through the panel. Trim pots may be single
  turn or multi-turn for more precise adjustment.
* External control: regular pots are used for external control. They are typically single turn (usually about 270 degrees),
  and may have different features

  * Taper: Audio (A) and linear (B). With an A taper, the resistance changes quasi-exponentially (e.g. for volume control matching our perception of loudness); B tapers change resistance linearly (e.g. for control/tuning)
  * Gangs: multiple equivalent pots can be controlled by the same actuator, e.g. volume for left and right channels.
  * Detents: a tactile reference for the actuator, e.g. for feeling where the mid-point is.
  * Bushing: can have a thread below the actuator to mount on a panel.

Internal Adjustment
^^^^^^^^^^^^^^^^^^^

For coarse adjustment, the standard THT 6mm single turn pots are used. These can be used on a breadboard (lateral pin
pitch is 2.54mm). "RM065" is the generic part number on AliExpress.

For fine adjustment, a multi-turn trim pot is used. The "3296W" is common and breadboard-ready. 

**Part Numbers**

* 6mm single-turn 

  * Amphenol Piher PT6KV-104B2020: (V)ertical, 104=100k, (B)-taper, 2020=+/-20% tolerance
  * Search for "6mm potentiometer assortment kit" on Amazon
  * Search for "RM065" on AliExpress

* Multi-turn

  * Bourns 3296W-1-104LF: W=vertical style; 104=100k
  * Search "3296W" on Amazon or AliExpress

**KiCad Footprints**

* Potentiometer_THT/Potentiometer_Piher_PT-6-V_Vertical (works for generic RM065 pots, too).
* Potentiometer_THT/Potentiometer_Bourns_3296W_Vertical (works for generic 3296W pots, too)

External Control
^^^^^^^^^^^^^^^^

The common form factor for THT pots is "RV09" -- 9mm wide, 6mm diameter shaft. These can be found on AliExpress in 
a wide variety of configurations for about $0.05/ea. DigiKey and other suppliers offer these from Bourns in the 
`PTV09 <https://www.bourns.com/docs/Product-Datasheets/PTV09.pdf>`_ series for about $1.00/ea. Kits with
an assortment of values are available on AliExpress and Amazon.

* Taper: A or B depending on application
* Orientation: Horizontal or vertical
* Actuator: Prefer 18mm shaft length (13mm OK); Use D/flatted shaft; Shaft diameter is 6mm nominal.

  * *Note*: some lengths (Bourns) are measured from the back side (against the PCB). The distance from the rear 
    mount face (PCB side) to the top face is about 8mm, so a L=25mm pot will have a 17mm shaft (18mm equivalent).
  * Can also use shaft with 18 teeth (more common with RV09 & various knobs). This also matches the shaft type 
    for the panel mount pots

* Height: 8mm from PCB to top of the case standoffs 
* Width: the "09" designation (RV09, PTV09) indicates a 9mm width. Otherwise this dimension can vary.

For more features (detents, multi-gang) it's likely easier to find in a Bourns model on DigiKey, although they have a
more limited selection of lengths, etc. 

**Part Number Examples**

* Bourns

  * PTV09-4025F-B104: type 40=vertical, no bushing, no detents; L=17mm (25-8mm); Flatted shaft; B-taper; 100k
  * PTV112-4420A-A104: 112 = dual gang; type 44= vertical, no bushing, no detents; L=12mm (20-8mm); Flatted shaft; A-taper; 100k

* AliExpress

  * Search "RV09" with e.g. "D shaft" for flatted shaft. Shaft lengths include 13mm (20mm equiv.), 18mm (25mm), 23mm (30mm)

**KiCad Footprints**

*Warning* check the ordering of the pins in the layout, pin 3 is on the left.

* Potentiometer_THT/Potentiometer_Bourns_PTV09A-1_Single_Vertical
* Potentiometer_THT/Potentiometer_Bourns_PTV09A-1_Single_Horizontal
