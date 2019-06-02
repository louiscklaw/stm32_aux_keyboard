# Build Guide

## Parts
### Required
| Item | Count | Remark |
|:-|:-|:-|
| PCB                   | 2      | |
| Plate                 | 2 sets | |
| ProMicro              | 2      | |
| TRRS Jack             | 2      | |
| TRS(3 pole) cable     | 1      | TRRS(4 pole) cable works too. |
| Tact switch           | 2      | |
| Diode                 | 42     | You need SMD for low profile. |
| Key Switch            | 42     | |
| Key Cap               | 42     | 1u x 40,  1.5u x 2 |
| Spacer M2 6mm         | 10     | use 3mm for low profile |
| Spacer M2 8mm or 10mm | 4      | |
| Screw M2              | 28     | |
| Rubber foot           | 10     | |

### Optional
| Item | Count | Remark |
|:-|:-|:-|
| OLED Module           | 1 or 2 | |
| 4x1 Pin Male Header   | 2      | For OLED |
| 4x1 Pin Female Socket | 2      | For OLED |
| SK6812MINI            | 54     | Front side x 42, back side x 12 |
| Addressable LED Strip | 2      | exclusive with SK6812MINI |

![image](https://user-images.githubusercontent.com/736191/40734610-e1ca0136-6473-11e8-8ac7-7bfa4b843f93.png)

## Soldering

PCB is reversible; use one for the left hand side and the other for the right.

### Diodes
__For non Low Profile keyswitches__

Solder diodes as indicated in the picture. You can place it on either side, but front side is recommended if you implement under-glow LED. You can use SMD diodes too.

![image](https://user-images.githubusercontent.com/736191/40736513-306a0976-6479-11e8-8f98-a88073919a71.png)


Diode has polarity; make sure to match the polarity with PCB silkscreen.

<- Before | After ->

![image](https://user-images.githubusercontent.com/736191/40735282-bac94180-6475-11e8-96f9-1d1cc43b1ee9.png)

__For Low Profile Keyswitches__

If you use low profile keyswitches, you have to implement SMD diodes __on the back side__.
Otherwise, diodes will interfere with top plate.


### LEDs (Optional)

Implement LEDs under keyswitches (No. 7 through 27) upward facing, and others (No. 1 through 6) on the back side(under-glow), as indicated in the picture.

![image](https://user-images.githubusercontent.com/736191/40731604-62cee61e-646c-11e8-865f-829a48fa6be0.png)

For No.7 to 27 LEDs, __Install LEDs from the back side__ as shown below.
Note the '**o**' silkscreen marking and use them as a guide to implement LEDs in the direction.

![image](https://user-images.githubusercontent.com/736191/40731605-62f840a4-646c-11e8-99d5-b3bdff709e9d.png)


For No. 1 to 6 LEDs, solder the pattern on the side of the device (highlighted in pink on the picture) and the PCB pattern(blue on the picture). Apply flux and take small amount of solder with a soldering iron and press it on the edge of the patterns.


![image](https://user-images.githubusercontent.com/736191/40733058-c0558402-646f-11e8-9718-e579fab4aaf5.png)

LEDs are connected in the order of the number on the picture above. If it turns on only halfway, it is likely that first LED that doesn't turn on or the last LED that turns on is not implemented correctly.


### Jumpers for OLED modules (optional)
To use OLED modules, short circuit the jumper patterns.
__Only short circuit the front side__

![image](https://user-images.githubusercontent.com/736191/40734778-56ded514-6474-11e8-8da7-3ebba048d62d.png)

### TRRS socket, reset switch, OLED header sockets.

Install TRRS sockets and reset switches as in the picture.
For OLEDs, also implement pin sockets.

![image](https://user-images.githubusercontent.com/736191/40736856-1bda2b84-647a-11e8-988b-dc45f2c76a38.png)

### ProMicro

Implement pin headers in the white frame, then install ProMicro with its backside up. (The picture is the right hand side, but it's the same for the left hand side - pins into the through holes in the white frame, backside up.)


![image](https://user-images.githubusercontent.com/736191/40737973-3f404de4-647d-11e8-84fe-37f3a34e4c53.png)

### OLED Module
Implement pin header onto the OLED modules, then insert them into the pin sockets.

![image](https://user-images.githubusercontent.com/736191/40888530-7420d1aa-6793-11e8-8813-9681c1411a21.png)

Adjust the height of the spacer accordingly to the height of pin header.
Most common pin header/socket and 10mm spacers are used in the picture.


### Use socket to Mount ProMicro

With using sockets for mounting ProMicro, you can replace it easily when it breaks. Two methods are introduced here.


#### Using Spring Loaded Header

Refer to [Helix Buildguide](https://github.com/MakotoKurauchi/helix/blob/master/Doc/buildguide_en.md#pro-micro)

ProMicro kit with spring loaded headers is available at Yusha-Kobo

https://yushakobo.jp/shop/promicro-spring-pinheader/

Using OLEDs available at Yusha-Kobo which come with low profile header, together with and 8mm spacers, you can build them think and gap-less.

![img_4141](https://user-images.githubusercontent.com/736191/41304818-2b65511e-6eac-11e8-9357-999ff14080ed.png)

#### Using Pin Sockets
Low profile pin sockets are available from Akizuki Denshi etc. Requires some work.

http://akizukidenshi.com/catalog/g/gC-03138/

Install a couple of 12x1 pin sockets on a breadboard.

![img_4130](https://user-images.githubusercontent.com/736191/41305246-4d63b7a0-6ead-11e8-8dbe-16c75d8b55e3.png)

Using male 12x1 pin headers, fixate ProMicro onto the pin sockets.

![img_4131](https://user-images.githubusercontent.com/736191/41305247-4fbd3e5e-6ead-11e8-8c4d-5feea5a026d3.png)

Remove plastic pin holders, solder the pins to ProMicro, and then cut extra pins.

![img_4132](https://user-images.githubusercontent.com/736191/41305251-5198439a-6ead-11e8-80f4-bd1769915bc9.png)

#### Comparison

Spring loaded headers can make the height lower.

![img_4134](https://user-images.githubusercontent.com/736191/41305254-53bc4522-6ead-11e8-83ed-c4c7c2787828.png)


Comparing pin-headers in the picture. Headers come with OLED available at Yusha-Kobo are lower.

![img_4137](https://user-images.githubusercontent.com/736191/41305263-57e53dac-6ead-11e8-9b5d-5667bca5599e.png)


### Testing
It is recommended to test the ProMicro and OLED modules before installing key switches because rework would be difficult after that.

First, build QMK Firmware for built for Crkbd and install on ProMicro.

![image](https://user-images.githubusercontent.com/736191/40888832-0d793c3a-6798-11e8-93b4-55ec7e180748.png)

Using the default keymap, OLED will show information on the keyswitches being pressed. Check the connections by short-circuiting key-switch soldering pads with tweezers. Check all of them.
If you have mounted LEDs, also make sure all of them are turned on.

![image](https://user-images.githubusercontent.com/736191/40888868-73028d36-6798-11e8-8246-0c9ca32711d6.png)

### Keyswitches and Top Plate
Sandwich top-plate with PCB and key-switches.

![image](https://user-images.githubusercontent.com/736191/40888597-8a5bf7a0-6794-11e8-89e2-535c3f8381b9.png)


### Bottom Plate
Use 3mm spacers for low-profile,
Attach bottom plate to the PCB using 6mm (3mm for low-profile) spacers.
Then attach six rubber feet.


![image](https://user-images.githubusercontent.com/736191/40888724-2892c24a-6796-11e8-8f38-a0a3d5e5440e.png)

### Keycaps
Lastly install keycaps.

![lrg_dsc03895](https://user-images.githubusercontent.com/736191/40888756-c371e264-6796-11e8-8fc5-e842e8baf2b8.png)


## Firmware
Setup firmware build environment following the instructions here:
https://docs.qmk.fm/#/newbs_getting_started

Then build firmware for Crkbd with this command:

```
make crkbd:default
```

To flash the firmware image you have just built, execute this:

```
make crkbd:default:avrdude
```

You will see `.` after a message like below.
While you see `.` is being printed on the screen, push the reset switch __twice__.

```
(snip)

Checking file size of crkbd_rev1_default.hex                                                        [OK]
 * File size is fine - 27328/28672
Copying crkbd_rev1_default.hex to qmk_firmware folder                                               [OK]
Detecting USB port, reset your controller now........
```

Flash the firmware to the other side as well.


That's it.
