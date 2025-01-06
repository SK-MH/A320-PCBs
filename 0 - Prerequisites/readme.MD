# A320 boards and panels

> [!IMPORTANT]
> Vorsicht beim ADIRS. Version prüfen

<!-- Spickzettel
- Lights und ECAM jetzt mit Pro Micro statt AtMEGA 2560
- Verbindugen zwischen den Boards beschreiben
-->

## KiCAD

In most of the KiCAD boards you can find additional layers.
<table>
<tr><th width="30%">Layer</th><th width="50%">Usage</tr>
<tr><td>Front Marker</td><td>Focus in the middle of a Button, Switch, Encoder or a display</td></tr>
<tr><td>Front Panel</td><td>Edges, Holes and Cutouts for the objects in the Front layer</td></tr>
<tr><td>Mid Panel</td><td>Edges, Holes and Cutouts for the object in the Mid layer</td></tr>
<tr><td>Engrave</td><td>Text, Symbols, etc. for engraving in Front layer</td></tr>
<tr><td>Color Mask</td><td>Prevent color on the colorless board when painting the edges</td></tr>
</table>

These Layer can be printed out in KiCAD as SVG-File. 
With Inkscape you have to remove the TEXT objects.
Otherwise they will be twice in the final version.

The final SVG files could be milled with a CNC machine or cut with a laser cutter.
> [!NOTE]
> I have made no good experience with a diode laser trying to cut 3mm acryl.
> Use a CO2 laser or a CNC machine.

For both the panels I found some at "Acrylics-shop" (NO! I'm not an affiliate to this company).
For the Front panel I used Makrolon® UV 2130 weiß opal 3mm, Artikelnummer (articel number): 70600.
This is white and 30% translucent. After milling or cutting it can be painted.
And for the Mid Panel I used Makrolon GP099 standard 3mm, farblos (colorless).

For a few boards the Color Mask (see above) is already defined. 
Cut them with a laser using some cardboard and fix it temporary on the panel when painting.

## MobiFlight Modules
For better readability all definitions are following this sequence and the naming convention:

<table>
<tr><th width="20%">I/O</th><th width="40%">Device<th width="40%">Name</tr>
<tr><td>Output</td><td>LED / Output</td><td>OUT BRT BACK</td></tr>
<tr><td></td><td></td><td>OUT BRT LED</td></tr>
<tr><td></td><td></td><td>LED &#060;name&#062;</td></tr>
<tr><td></td><td>LED 7-Segment</td><td>7SEG</td></tr>
<tr><td></td><td>LCD Display</td><td>DIS x</td></tr>
<tr><td></td><td>Servo</td><td>SERVO x</td></tr>
<tr><td></td><td>Stepper</td><td>STEP x</td></tr>
<tr><td></td><td>Shift Register</td><td>OSH x</td></tr>
<tr><td>&#032;</td><td>&#032;</td><td>&#032;</td></tr>
<tr><td>Input</td><td>Button</td><td>BTN &#060;name&#062;</td></tr>
<tr><td></td><td>Encoder</td><td>ENC &#060;name&#062;</td></tr>
<tr><td></td><td>Analog Input</td><td>POT &#060;name&#062;</td></tr>
<tr><td></td><td>Input Shift Register</td><td>ISH x</td></tr>
<tr><td></td><td>Digital Input Multiplexer</td><td>MUX x</td></tr>
<tr><td></td><td>Custom Devices</td><td>CUST x</td></tr>
</table>

> [!TIP]
> All &#060;names&#062; are in CAPITALS, x is representing a number 1..9

## MobiFlight Connector

tbd.
