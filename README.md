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

Bottom variants (Ground plane option)
-----------

My original design uses the 1.27mm pattern on both sides. For some analog and RF circuits I wanted a better GND plane.
So I made a variant with a near-solid GND plane on the bottom side.

* Near solid copper plane on the bottom side
* Plated-through holes in 2.54mm raster
    * The holes have a minimal annular ring of 0.15mm
    * Around the ring is another 0.15mm space
    * After that the GND plane begins
* A hole just soldered on the top is not automatically connected to the GND plane because of the 0.15mm space
* Just put a blob of solder on the bottom to connect a hole to the GND plane

| <img src="https://github.com/electroniceel/protoboard/raw/master/photos/gndplane.jpg" width=350 alt="GND plane"> | <img src="https://github.com/electroniceel/protoboard/raw/master/photos/gndplane-detail.jpg" width=350 alt="GND plane detail"> |


How to get?
-----------

Chinese pcb manufacturing services became so cheap even for small quantities
that it's easiest for you to order the protoboards there for yourself.

When I began designing these boards, I ordered samples from Elecrow and JLCPCB and both came out fine. But
when ordering some new boards, JLCPCB now declined to manufacture them with (cheap) HASL surface finish and only
wanted to manufacture them if I switched to (more expensive) ENIG. They explained that the HASL process might leave small
solder blobs on the surface creating shorts. Elecrow continued to manufacture them without any issues.

So I recommend to order the boards from [Elecrow](http://www.elecrow.com/referral-program/MjA0ODlqMnQ=/).

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
* Set the grid to 1.27mm
* Take the base pattern and copy it as much as you like
* Draw the pcb edges (and maybe routed slots) around

For the variant with GND plane on the bottom:

* Use the "-oneside" footprints on the top side
* Use "tht-0.8-thin-bottom" on the bottom side

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

Similar projects
----------------

This layout might not fit everyones needs. Here are some other protoboard designs with a grid of 1.27mm or lower:

* [Black Mesa Labs BML 50MIL](https://blackmesalabs.wordpress.com/2017/12/03/bml-50mil-0-050-proto-boards-for-rapid-surface-mount-prototyping/), free to download sources & gerbers
* [Busboard 50x50mil SMTpads](https://www.busboard.com/surfacemountpcbs), commercial
* [FYD Open Source Hardware](https://www.aliexpress.com/item/32774106087.html), commercial

License
-------
![CC-BY](https://licensebuttons.net/l/by/4.0/88x31.png)

This work is licensed under a [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

Please link to http://git.io/vNUDX for attribution.
