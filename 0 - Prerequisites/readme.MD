# A320 boards and panels

> [!IMPORTANT]
> Vorsicht beim ADIRS. Version prüfen

<!-- Spickzettel
- Lights und ECAM jetzt mit Pro Micro statt AtMEGA 2560
- Verbindugen zwischen den Boards beschreiben
-->

## KiCAD

In the KiCAD boards you can find additional layers.
<table>
<tr><th width="30%">Layer</th><th width="70%">Usage</tr>
<tr><td>Front Marker</td><td>Focus in the middle of a Button, Switch, Encoder or a display</td></tr>
<tr><td>Front Panel</td><td>Edges, Holes and Cutouts for the objects in the Front layer</td></tr>
<tr><td>Mid Panel</td><td>Edges, Holes and Cutouts for the object in the Mid layer</td></tr>
<tr><td>Engrave</td><td>Text, Symbols, etc. for engraving in Front layer</td></tr>
<tr><td>Engrave Green</td><td>Text, Symbols, etc. for engraving the green part in some of the Front layer</td></tr>
<tr><td>Color Mask</td><td>Prevent color on the colorless board when painting the edges</td></tr>
</table>

These Layer can be exported in KiCAD as SVG-File.

Front Panel, and Mid Panel files can be used for milling with a CNC machine or cut with a laser cutter.

> [!NOTE]
> I have made no good experience with a diode laser trying to cut 3mm acryl.
> Use a CO2 laser or a CNC machine instead.

<details>
<summary>See how to deal with SVG files for Engraving</summary>  

In the following part I try to describe the handling of Engrave-SVG files. As an Example I use the LIGHTING panel

![Example](SVG_Example1.JPG)

First the SVG files have to be maintained that they fit for laser engraving or carving.

Step 1: Open the file in Inkscape. 
    ![Step 1](SVG_Example2.JPG)
Step 2: Open, if not already done, the "Layers and Objects" tab in the upper right corner
    ![Step 2](SVG_Example3.JPG)
Step 3: Filter only objects which have a text inside by typing "text" in the filter (upper right corner). 
        The list of objects will shrink. Expand all Objects to see the text items.
    ![Step 3](SVG_Example4.JPG)
Step 5: Remove all text items. You can see them vanishing in the main window.
    ![Step 5](SVG_Example5.JPG) 

Save the file again in SVG format ! 

Text elements are already well formatted as you can see in the following picture.
    ![Step 6](SVG_Example6.JPG) 

But the lines are very thin and have to be thickened. For his I use Lightburn. 
There might be other tools like CorelDraw but I do not have it.

<b>IMPORT</b> the SVG file into Lightburn.

Mark the line you want to make thicker. Press ALT+O (Offset).*
    ![Step 8](SVG_Example7.JPG) 

Choose the parameter which fits to your needs.
    ![Step 8](SVG_Example8.JPG) 

When changing the mode to "Fill" you can see already the result for laser engraving.
    ![Step 9](SVG_Example9.JPG) 

If you want to carve the items with a CNC machine <b>EXPORT</b> this file again as SVG.

I use ESTLCAM for the CNC. Open the SVG file.
Select a carving tool, the carving mode, all items and start carving.
    ![Step 10](SVG_Example10.JPG) 

In the lower left corner of the picture you can see the lower left edge of the front panel.
This could be used for setting the reference point for engraving.
</details>
<br>
For both panels I found material at "Acrylics-shop" (NO! I'm not an affiliate to this company).<br>
For the Front Panel I used Makrolon® UV 2130 weiß opal 3mm, Artikelnummer (articel number): 70600.<br>
This is white and 30% translucent. After milling or cutting it can be painted.<br>
And for the Mid Panel I used Makrolon GP099 standard 3mm, farblos (colorless).
<br><br>
For a few boards a Color Mask (see above) is already defined. 
Cut them with a laser using some cardboard and fix it temporary on the panel when painting.

## MobiFlight Modules
For better readability all definitions are following this sequence and the naming convention:

<table>
<tr><th width="20%">I/O</th><th width="40%">Device<th width="40%">Name</tr>
<tr><td>Output</td><td>LED / Output</td><td>OUT BRT BACK</td></tr>
<tr><td></td><td></td><td>OUT BRT LED</td></tr>
<tr><td></td><td></td><td>LED &#060;name&#062;</td></tr>
<tr><td></td><td>LED 7-Segment</td><td>7SEG x</td></tr>
<tr><td></td><td>LCD Display</td><td>DIS x</td></tr>
<tr><td></td><td>Servo</td><td>SERVO x</td></tr>
<tr><td></td><td>Stepper</td><td>STEP x</td></tr>
<tr><td></td><td>Shift Register</td><td>OSH x</td></tr>
<tr><td>&#032;</td><td>&#032;</td><td>&#032;</td></tr>
<tr><td>Input</td><td>Button</td><td>BTN &#060;name&#062;</td></tr>
<tr><td></td><td></td><td>SW &#060;name&#062;</td></tr>
<tr><td></td><td></td><td>RSW &#060;name&#062;</td></tr>
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
