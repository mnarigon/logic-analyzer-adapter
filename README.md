## An S-100 Bus Logic Analyzer Adapter Board.

![completed prototype board](images/IMG_1605.png)

#### Description

This is an S-100 bus logic analyzer adapter board.
It simplifies the connection to the S-100 bus of common 40-pin pod cables like
those for older HP/Agilent/Keysight logic analyzers.

#### Features:
- Connectors and isolation networks for 40-pin pod cables.
- Oscilloscope test points for S-100 bus signals.
- Test points for logic analyzer clock inputs and unused channels.

See the Keysight document, [Probing Solutions for Logic Analyzers](https://www.keysight.com/us/en/assets/7018-06707/data-sheets/5968-4632.pdf),
for more information on the pod interface.

Note that the photo is of the prototype board.

The design files are revision A, and have some changes based on my experience
with the prototype board. I haven't had the revision A boards manufactured
since the prototype is working for my purposes.

#### Revision A Changes:
- Surface mount components moved to back of board to provide additional
connector clearance.
- Location of pod connectors adjusted to provide more clearance to each other
and to the card ejectors.
- Added test points for unassigned logic analyzer channels.
- Silkscreen for test points moved for visibility.

#### Logic Analyzer Adapter Design Files

The revision A logic analyzer adapter design files in KiCad 7 are in the kicad
directory.

The generated revision A logic analyzer adapter Gerber and drill files are in
the file la-adapter-gerbers.zip.

The bill of materials is in the bom directory.

#### Design Notes

The BOM calls out the 3M connectors described in the Keysight
document. There are probably cheaper, non-3M connectors that would work.

The design files define front and back gold layers to specify hard gold on
the S-100 bus card edge connector. Hard gold is expensive, and few prototype
board houses offer it, so for the prototype I just specified ENIG treatment
for the copper layers and card edge connector.

#### Hand-soldering the Capacitors and Resistors

I use a fine tip soldering iron (Weller with an ETU tip) together with tacky SMD
flux to apply a very light amount of solder to the component pads.
Remove excess solder by reheating with a clean soldering iron and/or using
solder removing wick.
You want just a small pillow of solder on each pad.
After the solder has cooled apply an additional, small amount of flux.
The flux will keep the components in position while they are being soldered with
the hot air rework station.

Then, position the component on the pads using an awl from a desoldering tool
set with a small amount of flux on it.
The tacky flux on the awl will let you transfer and position the component on
the board.

Finally, use a hot air rework station set at a low air velocity to reheat the
solder, flux, and component to solder the component to the board.
Too high an air velocity will blow off the component from the pads.
You can tell when the solder melts because the capillary action of the molten
solder will cause the component to align with the pads.
After the solder melts apply hot air for a slow count of five to ensure that
the flux activates and the solder wets the component and pad.
