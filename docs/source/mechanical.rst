Mechanical Notes
================

Mechanical covers various conventions on the physical interfaces and assembly points for modules.
My modules are typically sized for `Eurorack <https://www.midisoft.de/EuroRackDimensions/EuroRack_Dimensions.html>`_
which determines the size of the face plate and its mount points. Additionally, this document will cover

.. contents:: 
    :depth: 1
    :local:

Sizing Considerations
---------------------

All PBCs have a height of 100mm:

* they can be fabricated at `JLC <https://jlcpbc.com>`_ or `PCBWay <https://www.pbcway.com>`_ using the most 
  economical option
* Standard 2020 extruded aluminium can be used as rails (however this won't work for commercial modules, which
  typically have PBCs with heights greater than 100mm)

All PBCs should have a minimum 0.5mm clearance to the extent of the faceplate, with a 1mm clearance prefered. 
For vertically mounted external connections (jacks, pots, etc.), this implies a PCB width 1-2mm narrower than 
the faceplate.

The minimum width for a module (jacks only) is 2HP, which is equivalent to a 10mm wide faceplate & 9mm wide PCB. 
This can be achieved with vertical jacks (e.g. WQP-PJ301M) and a 2x5 IDC header, but likely requires SMT components
on the PCB.

A 4HP (20mm wide faceplate) module can be built with horizontally mounted external connections, reducing size 
constraints on the width of the PBC (see next section).

Horizontal vs. Vertical
-----------------------

* multi-layer Horizontal
* skiff depth for vertical

Potentiometers
--------------

Potentiometers 


