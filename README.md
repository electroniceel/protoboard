Advanced protoboard layout with 1.27mm pitch for smd parts
==========================================================

| <img src="https://github.com/electroniceel/protoboard/raw/master/photos/sample1.jpg" width=350 alt="Sample 1"> | <img src="https://github.com/electroniceel/protoboard/raw/master/photos/sample2.jpg" width=350 alt="Sample 2"> |

Main Features
-------------

* Plated through holes in standard 2.54mm raster like on traditional protoboard
* Pads for smd parts in 1.27mm raster in between
* SOIC parts can directly be used without adapters
* SMD pads are not contacted to the other side:
  * Different tracks can either cross each other or connect
  * No wires to solder in like on non-plated-through protoboard
* Allows for much more dense layout

Supported Packages
------------------

<img src="https://github.com/electroniceel/protoboard/raw/master/photos/packages.jpg" width=400 alt="Supported Packages">

These packages can be directly used without adapter:

* DIP (Through hole, 2.54mm pitch)
* SOIC (SMD, 1.27mm pitch)
* SOT-23-3 (SMD)
* SOT-23-6 (SMD)
* SOT-323 (SMD)
* SOT-89 (SMD)
* SOT-223 (SMD)
* TO-252/DPAK (SMD)
* All 2 pin packages like for resistor and diodes known to me

Adapters to 1.27mm pitch smd are provided for these packages:

* TSSOP-14
* TSSOP-16
* SOT-363/SC-70

How to get?
-----------

Chinese pcb manufacturing services became so cheap even for small quantities
that it's easiest for you to order the protoboards there for yourself.

I ordered these boards from [Elecrow](https://www.elecrow.com/) and [JLCPCB/EasyEDA](https://jlcpcb.com/), 
they both turned out fine and ordering was smooth.

Finished gerber zips ready for ordering can be found in the ["gerber" directory](https://github.com/electroniceel/protoboard/tree/master/gerber).

If you prefer another layout, see below.

Production options
----------------

* Color doesn't matter as there is next to no soldermask on the boards
* I found 1.2mm thickness a good compromise between rigidity and ease of cutting
* But I'd go down to 1mm thickness if you prefer one big board without slots and want to cut it for each project to fit

Making your own layout
----------------------

* All neccessary KiCAD source files are provided in the ["kicad" directory](https://github.com/electroniceel/protoboard/tree/master/kicad)
* Open the layout in pcbnew
* Set the grid to 2.54mm
* Take the base pattern and copy it as much as you like
* Draw the pcb edges (and maybe routed slots) around

Soldering tips
--------------

Populating this protoboard needs obviously a bit more care than regular protoboard. Here are
some tips to get you started.

Use a smaller soldering tip than usual, I prefer a 1.2mm chisel type (JBC C245-906).

Reduce the soldering temperature to drag traces. I prefer 295°C for Sn60Pb40 solder
with my JBC station, other stations may need it slightly hotter.

The lower temperature makes the solder flow less liquid and so it is a bit easier to control where
it should flow and where not. So you can drag the solder blobs around a bit. If the solder doesn't
want to make the connection you need, take the tip away and let the spot cool for about 5 seconds. Then
try again.

This needs a bit of getting used to as it is completely different than populating boards with pads etched
to match the circuit where you usually want heat transfer as fast and even as possible.

License
-------
![CC-BY](https://licensebuttons.net/l/by/4.0/88x31.png)

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

Please link to http://git.io/vNUDX for attribution.
