# Dremel_3D45_Level_Sensor
KiCAD project, schematic, and gerbers of a Printed Circuit Board (PCB) replacement for The Auto_LevelBoard PCB for the Dremel 3D45 (and possibly the Dremel 3D40)
![PCB Rendering](./images/3D_Rendering.png "Rendering of the PCB")  **NOTE** Using this PCB will likely void any warranty provided with the printer.  An entire replacement leveling arm assembly can be [purchased directly from 3PITech](https://3pitech.com/products/3d45-leveling-sensor)

# Getting the Gerbers
If you only want to have the PCBs manufactured, navigate to the [releases page](https://github.com/timmehtimmeh/Dremel_3D45_Level_Sensor/releases/) and download the zip file of the gerbers

# Cloning the repo
This repository references the KiCAD symbol and footprint libraries stored in [Tims-KiCad-Library](https://github.com/timmehtimmeh/Tims-KiCad-Library) to properly clone this repo please type the following into a git command window:

```git clone --recurse-submodules https://github.com/timmehtimmeh/Dremel_3D45_Level_Sensor.git```

# Parts required

The following parts are required to replace the PCB

| Part | Qty | Link | Notes|
|------|-----|------|------|
| PCB | 1 | I had the gerbers successfully manufactured at [JLCPCB](https://jlcpcb.com/) as well as [OSHPark*](https://oshpark.com/shared_projects/k3kUrSLB) | * **NOTE:** The original Dremel PCB is 1mm thick.  OshPark only makes standard thickness 1.6 mm boards, but the thicker 1.6mm board worked fine in the printer. JLCPCB has options for 1mm thick boards |
| Switch | 1 | The OEM seems to be a [Panasonic ESE-31R15T](https://www.digikey.com/en/products/detail/panasonic-electronic-components/ESE-31R15T/3163183) | An alternate can be the [TE Connectivity JJJHRGG200NOPMRTR](https://www.digikey.com/en/products/detail/te-connectivity-alcoswitch-switches/JJJHRGG200NOPMRTR/9452492), but in testing the Panasonic part was less prone to getting stuck in the housing |
| Jumper Wire | 2  | [Wire](https://www.amazon.com/dp/B089CWGQKW) |  The OEM is 26 AWG stranded wire, 90 mm, 1 red, one black Outer Diameter (O.D) 1mm. I used the 1.2 mm O.D. 28 AWG silicone coated wire linked, and it still fits inside the cable routing cutouts on the level arm. |
| 2 Position JST-PH 2mm Connector | 1 | [JST Kit](https://www.amazon.com/dp/B0F485CN38) | I used the kit linked, however you can also buy pre-assembled wires  |

Additionally Soldering equipment (iron, solder), and either Silicone glue, or Hot Glue are needed to complete the job.

# Assembly Instructions

Tools Needed
1.  2mm Hex bit or Hex wrench (Allen key)
2.  T10 Torx (star) screwdriver
3.  T7 Torx (star) screwdriver
4.  Replacement PCB

Once you have gathered the necessary components, assembly is relatively straightforward.
1. Place the switch onto the PCB such that the alignment holes in the bottom of the switch mate with the holes in the PCB
2. Ensure that the switch is centered and square to the board
3. Solder on one of the four pads of the switch.
4. Check Alignment of the switch.  If it's moved heat up the one pad and move the switch until it's square with the board and then let the solder cool
5. Solder the remaining three pads of the switch
6. (Optional) Solder the two jumper pads such that the jumpers make contact. This connects the switch housing to one leg of the switch.  If using the TE Connectivity switch there is no metal housing and this step can be skipped.  If using the Panasonic switch then the circuit will work with or without the jumpers connected together.
7. Strip approximately 2mm of insulation off of one end of each of a black and red wire.
8. Crimp JST-PH connectors onto each of the wires
9. Push the crimped end into a two position JST-PH connector (the red/black orientation doesn't matter, but I kept mine the same as the original board)
10. Cut the wires such that they're both equal in length, and the same length as the OEM wire (approximately 90mm)
11. Strip 2-3mm of insulation off the cut end of the wire
12. Solder the red wire onto the PCB where the silkscreen indicates the red wire should go
13. Solder the black wire onto the PCB where the silkscreen indicates the black wire should go
14. Place the board on something that will allow you to put some silicone or hot glue onto the wires & board
15. Put a blob of glue such that it covers the two soldered ends of the wire and travels a bit up the wire to provide some strain relief.  Be sure to not allow too much glue to blob on the back side of the PCB
16. Once the glue is set, follow Steps 1, 2, and 5 from [these instructions](https://cdn.shopify.com/s/files/1/0552/1797/9558/files/3d45-3d40-leveling-arm-replacement.pdf)
17. Unscrew the PCB from the leveling arm assembly on your printer, taking care to not lose the screw or washer that holds the PCB in place
18. Carefully pull the wires out of the plastic wire guide on the leveling arm assembly, and remove the old PCB from the assembly
19. Thread the JST-PH connector from the new PCB through the appropriate area in the 3D printer head assembly and attach it to the printer, re-attach the servo motor wire if it was disconnected
20. Place the PCB into the sensor arm such that the plastic locating pin holds the PCB in place.
21. Using the T7 torx screwdriver, attach PCB using the screw & washer that was taken out in Step 17.
22. Reassemble the Extruder by following Step 6 in [these instructions](https://cdn.shopify.com/s/files/1/0552/1797/9558/files/3d45-3d40-leveling-arm-replacement.pdf)
23. If necessary, calibrate the level arm up/down position by navigating to TOOLS>SETTINGS>SERVICE TOOLS>LEVELING SWITCH and set the level (Step 7 in the linked instructions)
24. Calibrate the nozzle gap by following [these instructions](https://www.dremel.com/binaries/content/assets/dremel/uk/digilab/how-to-self-repair/3d45/3d45-nozzle-gap-calibration.pdf)

**Notes** - After a few uses I found that the replacment switch was not rebounding as quickly as it should.  To fix this i used a little bit of nonconductive spray lubricant on the tip of the switch and moved the switch in and out a few times after which the switch rebounded much more quickly.

