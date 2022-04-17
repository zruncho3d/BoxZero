# BoxZero - a fully-boxed V0/T0/X0 mod

Simplify, strengthen, and seal your [Voron Zero](https://github.com/VoronDesign/Voron-0) or V0-derived printer ([Tri-Zero](https://github.com/zruncho3d/tri-zero), [Double Dragon](https://github.com/zruncho3d/double-dragon)) by ditching the tophat and moving to a full-box frame.

Mod an existing printer for ~$60 or build a BoxZero from scratch, keeping the 200mm extrusions of a stock V0 frame kit, at about the same cost.

Pairs exquisitely with [Tri-Zero](https://github.com/zruncho3d/tri-zero) (a triple-belted Z mod) and [ZeroPanels](https://github.com/zruncho3d/ZeroPanels) (clip-in, clip-out enclosure panels), both shown below, as well as [Double Dragon](https://github.com/zruncho3d/double-dragon).

![Front](Renders//iso_minias_2.png)

Three key parts make this all work:

| Front Idlers (new) | AB Blocks (V0 mods) | Top Corners (optional)
| - | - | - |
| ![Front](Images/front_idlers_2.jpg) | ![Front](Images/AB_block.jpg) | ![Front](Images/large_corner_3.jpg) |

It's real, tested, and reproduced:

| Zruncho's T0 Conversion | Iso View | Front Zoom |
| - | - | - |
|![Front](Images/front_bright.jpg) | ![Front](Images/iso_2.jpg) | ![Front](Images/front_zoom_2.jpg) |

Join us on the `#doomy-worx` channel on the [DoomCube Discord](https://discord.gg/doomcube) - to ask questions, or share your experiences with this mod!

## Updates

#### 2022-04-XX First Release!

Hello World, BoxZero.

See how it compares, visually:

| BoxZero +TriZero +ZeroPanels +MiniAS +12864 | BoxZero +ZeroPanels | Voron Zero with Tophat (stock V0.1) |
| - | - | - |
| ![Iso](Renders/front_minias_2.png)  | ![Iso with skirt](Renders/front_v0.png) | ![Iso with skirt](Renders/front_v0_stock.png)
| ![Iso](Renders/iso_minias_2.png)  | ![Iso with skirt](Renders/iso_v0.png) | ![Iso with skirt](Renders/iso_v0_stock.png)

## Why this mod?

The V0 tophat serves its function: to cover the top umbilical and enclose the printer.

But ask a bunch of V0 owners... and let's just say, few will express their undying love for the tophat.  Actual unsolicited quotes heard in just the last week:
>  "Yeah, the tophat is kind of the bane of my V0 experience"

> "Can you tell I really dislike the tophat? They started bugging me less after I added a hinged riser that is a solid square. It does not match well enough so it looks bad that way but the stiffness and hinges are what the original should have had."

The V0 tophat creates real quality-of-life issues in practice:
* It's a notoriously challenging print that requires the entire bed of a Voron Zero and good bed adhesion and leveling.
* The small trapezoidal panels are harder to source than rectangular parts.
* The design adds many small parts to print and many heatsets to add.
* To clear the umbilical with some toolhead mods (e.g. [Mini-AfterSherpa](https://github.com/KurioHonoo/Mini-AfterSherpa)), a tophat extension is needed, ideally a [hinged one](https://github.com/zruncho3d/VoronUsers/tree/hinged_tophat/printer_mods/zruncho/Hinged_Tophat_Riser).  But those "censor the view" and require even more parts to print and source.
* It doesn't scale easily.  You can add extensions ([X0 example](https://github.com/zruncho3d/double-dragon/blob/main/STLs/Optional/Tophat_Middle_Spacer_x2.stl)), but you really want to increase the beam thickness too, and not need extensions to fit a V0 plate.
* You can't mount stuff to it easily, at least compared to extrusions (like lights or a camera).

## How does it work?

This mod ditches the tophat by moving to a fully-boxed frame, then updates each part affected by the change to fit in the remaining space.

### Frame and Corners

You will need additional extrusions to box the frame and make a "fixed tophat".  Don't worry though, you can easily add a hinged top panel. Here is the extra extrusion content, visualized:

![Front](Renders/tophat_2.png)

You can keep your colored extrusions from a V0 frame kit by joining 100mm ones from the bed with 200mm ones in the front.

Or, you can use off-the-shelf 300mm-long 1515 extrusions and add the blind joint holes yourself, easily.  This repo includes a printed extrusion wrench to join extrusions without marring the surface, along with printer corners to add enough vertical clearance to clear the umbilical.

But these are optional.  You can use a full-blind-joints frame with taller extrusions (350mm or taller).  You can further strengthen the corners with smaller corner stiffeners too, which are recommended for larger sizes that V0-stock.

| Large Corner (adds 50mm height) | Small Corner Stiffener |
| - | - |
| ![Front](Images/large_corner_3.jpg) | ![Front](Images/small_corner_3.jpg) |

The V0 side and bed extrusions get lifted, then other extrusions take their place.  There are a few options:

* **Option A: Replace all verticals with 300s**.  Move 2 of the existing 200s to the top.
* **Option B: Replace the rear 2 verticals with 300s**.  Move 2 of the existing 200s to the top, then add 100mm extrusions to replace the ones for the bed and colorize the front.  
  * If you have a Kirigami bed or T0 mod, the 100s will be easily available.  
  * You'll still need an additional 200mm extrusion.
  * Add 100mm to the verticals.
  * Conjoin the extrusions with set screws an add 2 200mm extrusions to span the gaps.
* **Option C Mix of 100 and 200mm-length extrusions**.  Effectively, add a fixed tophat.
* **Option D: Go full-height with cut-to-size extrusions**.  Then use the smaller stiffeners, vs the full-size extrensions.

It all depends on what's easiest to source and what you think looks best.  You choose.


### AB Blocks

The packaging of the V0 is super-tight, so the big challenge with a full box is fitting the belt path around added frame extrusions.  The key insight was to add extra F623 bearings to redirect the belts around the rear frame, away from the rear corners.  To free space for the belt, the sliding motor block had to be chopped, but the 3 remaining screws are plenty to fully secure the motor.

![Iso](Renders/ab_drive.png)

| ![Iso](Renders/ab_drives_front.png) | ![Iso](Renders/ab_drives_rear.png) |
| - | - |

The belt is either redirected around the added idler, or passes to the main pulley and back around.  This early sketch gives a sense of how it works:

![Iso](Images/belt_path_sketch.png)

The new AB blocks are intentionally set back 3mm from the front, to support future mods to add extra Y travel from an offset gantry, so you'll want to add something to bridge that 3mm gap to the Y endstop.  [F0 MGN9 spacers](https://github.com/zruncho3d/f-zero/blob/main/STLs/Gantry/mgn9_spacer_x2.stl) are one easy to span it, especially if using a non-levered microswitch.

The hole positions have been moved too, so that all are aligned easily with 15mm No-Drop nuts.

### Front Idlers

At the front, this mod uses slightly modified [Double Dragon](https://github.com/zruncho3d/double-dragon) front Y idlers for the main belts.

![Front](Images/front_idlers_2.jpg)

### Enclosure

You can use the default V0 enclosure parts, or much better, can move to [ZeroPanels](https://github.com/zruncho3d/ZeroPanels), which clip in without screws, nuts, magnets, or tape. They're perfect for this application.

[Tecnologic's full boxed-frame enclosure](https://github.com/Tecnologic/ZeroPanels/tree/main/Mods/tecnologic/FlyingZero300), based on the original ZeroPanels, works perfectly here and even includes high-strength, 270-degree hinges.  What's not to love?  You can put the hinges on top too... BAM, and you have a fully accessible toolhead, without even needing 5 seconds to clip out a panel.

| Main Corners | Hinge Corners |
| - | - |
| ![Iso](Images/zeropanels_corners.jpg) | ![Iso](Images/zeropanels_corners_hinged.jpg) |


See a video of [ZeroPanels clipping in and out, and then in and out again](https://www.youtube.com/watch?v=L3nBHkO4VzE).

### Other changes

Actually, that's it.  The belt path is shorter, so you can reuse and then trim your existing belts.  The midplate and baseplate don't change.

## BOM

These are just the parts beyond those needed for a stock V0.  All assume that no parts comes from the tophat, so they may be really conservative.

| Category | Part | Qty | Notes | Link |
| - | - | - | - | - |
| Fasteners | M3x6 BHCS | 8 to 36 | For corners, depending on style, and how many you add. |
| Fasteners | M3 Nuts | 8 to 36 | For corners, depending on style, and how many you add. |
| Fasteners | M3x30 BHCS  | 2 | For additional bearing stacks in AB blocks |
| Fasteners | M3 Shims | 6 | 2 freed up from front idler conversions |
| Fasteners | M3 Heatset | 12 | For AB blocks
| Motion | F623 flanged bearing | 8 | For AB blocks
| Panels | 212x332x3mm panel | 3 | Side and front panels, clear acrylic
| Panels | 212x212x3mm panel | 1 | Top panel, clear acrylic

A sample panel order from SendCutSend, without any discount, looks like this:
![iso](Images/scs_panel_order.png)

For extrusions you have a few choices:

| Category | Part | Qty | Notes | Link |
| - | - | - | - | - |
| Extrusions | 300mm 1515 | 4 | Option A for extrusions | [MBXL 300mm](https://www.amazon.com/MakerBeam-XL-Anodized-300x15x15mm-Pieces/dp/B06XJ5G5QY) |
| Extrusions | 300mm 1515 | 2 | Option B for extrusions | [MBXL 300mm](https://www.amazon.com/MakerBeam-XL-Anodized-300x15x15mm-Pieces/dp/B06XJ5G5QY) |
| Extrusions | 200mm 1515 | 1 | Option B for extrusions | [MBXL 200mm](https://www.amazon.com/dp/B06XHQH9WH) |
| Extrusions | 100mm 1515 | 4 | Option C for extrusions | [MBXL 100mm](https://www.amazon.com/gp/product/B06XJ4T6TW/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1) |
| Extrusions | 200mm 1515 | 4 | Option C for extrusions | [MBXL 200mm](https://www.amazon.com/dp/B06XHQH9WH) |
| Extrusions | 350mm 1515 | 4 | Option D for extrusions | Misumi, other |
| Fasteners | M3x12 set screw | 1 per join | Option B/C: join exts; can chop a screw |

If making the ZeroPanels exclosure with hinges, you'll also need screws and locknuts for each hinge pair:

| Category | Part | Qty | Notes | Link |
| - | - | - | - | - |
| Fasteners | M3x50 SHCS | 2 per hinge pair |
| Fasteners | M3 locknut | 1 per hinge pair |
| Fasteners | M3 washers | 4 per hinge pair |

## What's in this repo?

In this repo are all of the STLs needed to do a BoxZero conversion, with just those parts which are not in the V0.1 repo.

All parts should be already be in print-ready orientation, with seam in the +Y dir, and no supports are needed.

Standard Voron settings, or lowered infill and fewer perims, should work fine for most parts:
- 4 perimeters
- 40% infill, depending on the part
- 0.2mm layer height

The AB blocks can be printed with much less infill (20%).

Print the corners (both types) with 3 perims, 10% infill or higher.  While this will print happily with zero infill, you don't want flexible edges.

### Printed Parts

Print all STLs in the quantites noted from this repo, along with STLs from:
- [ZeroPanels](https://github.com/zruncho3d/ZeroPanels)
  - Regular V0 ZeroPanels parts work fine.
  - [Tecnologic's full boxed-frame enclosure](https://github.com/Tecnologic/ZeroPanels/tree/main/Mods/tecnologic/FlyingZero300) are recommended for easier front sealing.
- [F-Zero](https://github.com/zruncho3d/f-zero): [No-drop nuts](https://github.com/zruncho3d/f-zero/tree/main/STLs/NoDropNuts) are highly recommended, specifically the no-grip flat-top ones

## Assembly Notes

### Frame

- Joining extrusions (typically for 100 mm + 200 mm --> 300 mm):
    - Print the 1515 extrusion wrench if you haven't.  It will protect the sensitive anodized finish of the extrusions, vs using an adjustable wrench or vise, both of which will damage the surface finish.
    - Use a 12mm m3 set screw or make one by chopping the end off of a screw. Tighten the set screw into the extrusion threads by 6mm or so, and then using an allen wrench, block it from screwing down further.  Then screw on the small extrusion.  Once you feel resistance, go slow, and use one or two extrusion wrenches to align to the next quarter-turn.  No loctite should be needed for the set screw, as the aluminum should slightly deform as you add pressure to get the final quarter-turn.  Don't go too hard and destroy the threads, though.  Don't fear.  The aluminum will yield before the steel does.

- To add a hole for a gantry horizontal extrusion into a 300mm vertical, put the 100mm extrusion against your V0 frame-drilling guide, where the guide has been screwed onto the end.  Then, use the hole in the extrusion wrench (see the `STLs/Tools` directory) for alignment to 7.5mm from the end of the 100mm vertical.  Don't forget to drill holes in the other ends of the frame joints, too, if these are fresh extrusions.  

- For the full-height verticals option, put holes in the ends, 7.5mm from the edge.  These are not needed with 300mm extrusions and the frame corners.

- Both corner block types are *designed* to be tight, and in fact, matched to fit your exact extrusions!
    - You will have to scrape away some of the plastic that goes into the extrusion slot to get them to fit.  This is fully intentional, so that extrusions that are nearly 3.0mm in slot width, up to much sloppier ones (3.6mm or so), can be accommodated, and so that screws become optional, and not even required.  The edge of an extrusion should be sharp enough to peel away a bit of the edge.  Go slow and apply pressure, then back off and clear out the peels.  **The extrusion should fit tightly, without screws, as a result of this.**
    - To get the exutrusion started into the corner, twist the extrusion into the inner corner to get started, and then keep it parallel.  If one side "escapes", start over and work inwards.  
    - Most corner screws are optional.  The top-most 12 on the frame are the most important (4 down, and 2 in each corner, sideways).  Beyond this, one or two per corner below should be plenty to add rigidity, but you can add an extra 4 per corner if you want.  If so, make sure to pre-load no-grip NoDropNuts first, in a visible location, so that you can slide them in.
- Build the top crown of extrusions and corner blocks: add NoDropNuts beforehand, pushed far enough down the extrusions.
- Make sure to add all the NoDropNuts you'll need before.  
  - Add for rear attachments like spool holders or filament guides.
  - Add two on the inner faces of the rear verticals, which will attach to the upper AB blocks.

### AB Blocks
* Build the modified AB blocks similarly to V0 AB blocks.  Press all heatsets flush and make sure to add washers around each F623 bearing stack, but not the 9mm spacers.
  * Protip from Red5: use M3 nuts to secure the bearing and washer stacks with the AB upper parts, temporarily, and then remove the temp nut right before building the full assembly.
* Access to the belts is easiest when the AB blocks are outside the frame.  Toothpicks work well to get the belt where you want it.  Route the belts, then add the blocks in.

### Front Idlers
* Note that one of the needed washers is built into each part.  Make sure to tighten the screw only when the idler unit is being pulled against the extrusion.  It will be under tension from the belt, and you don't want it shifting when that tension is added.

### Converting

If converting, note that you don't need to take the frame apart!  Verticals can slide up and out.  You can leave all the electronics, gantry, etc. in place.

## FAQ

### What do you mean by Alpha Release?

The parts actually work, and have been tested in a working printer.  But sizes and parts may change in future releases.

### What are the downsides?

- Potentially a less rigid frame when using ZeroPanels, since the panels float in the extrusion slots, vs more rigidly mounted enclosure panels.  This may be somewhat counteracted by closing the box and adding stiffening braces.  Perhaps some thumbscrews for the panel clips could be a nice middle ground.

- The belt path is a bit more twisty and tight around the motor pulleys, so it's more sensitive to alignment errors.  You'll know quickly if your pulley is not quite aligned, as it will make a sound when in motion on the side that's running.  You can have a pulley that's good enough for a regular V0, but then when converting to BoxZero, the shorter paths may reveal the alignment issue.

- A little more cost, at least compared to a V0.  Just a little.

### What is the cost?

It's almost a cost-neutral mod for new builds.  The outer enclosure panels get slightly larger, but then you don't need laser-cut trapezoid panels.  Add the cost of a few bearings and some extrusion.

### What if I have questions?

The renders and CAD should answer many questions first.

Then, go the DoomCube Discord and ask on the `#doomy-worx` channel.

### Convince me!

Still not convinced?  For a V0/T0/X0 build, here are the benefits:

**Simplicity**
* Rectangular panels are easy to source from anywhere.
* A full box is straightforward to seal.

**Maintainability**  
* You can build the frame first, then add the AB blocks (the ones with motor tensioners) later, or swap them for future mods.

**Rigidity**
* A metal front-top crossmember adds rigidity, vs nothing (V0), or a plastic tophat.  
* A metal box top adds rigidity in general.
* The added rigidity enables greater scalability, too, especially to +50 X/Y/Z, which can enable the use of commodity Prusa-Mini-size 180mm beds.  This is the super-secret ulterior motive of this mod...

## Related Work

- [Hartk1213 Hinged Hat for the V0](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/hartk1213/Voron0_Hinged_Top_Hat) - solves a real problem, but requires many printed and non-printed parts.
- [Zruncho Hinged Tophat](https://github.com/zruncho3d/VoronUsers/tree/hinged_tophat/printer_mods/zruncho/Hinged_Tophat_Riser) - a great implementation of the wrong solution :-)
- ... and many, many other tophat mods on VoronUsers.  It's almost a V0 rite of passage...
- [DooMini](https://github.com/TigranDesigner/Voron-Mods/tree/main/DooMini) - similar goal, different method, more filament used.
- [F0 Corner Blocks](https://github.com/zruncho3d/f-zero) certainly inspired the corner blocks here.  BoxZero ones are better.

## Credits

- Thanks to Red5 on Discord for being the first to print and providing useful feedback for the first release.
