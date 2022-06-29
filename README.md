# ByranTK-Alpha

# Note: New 3D Printed Version of the case added! First prototype working!!

*The ByranTK-Alpha is an 80 key custom mechanical keyboard, designed to be made with any material.*
<br>
<br>
*"All the keys you need and no more."*

### V1.1 is confirmed to be working with firmware from https://github.com/Hello9999901/zmk-config-btk-alpha

# What is it:
The ByranTK-Alpha is an ongoing open-source keyboard project. It is extremely simple and utilizes a nice!nano from Nice Keyboards as the MCU. The battery life is estimated to be around 3 months of continuous usage (varies extremely depending on battery capacity, tested with 500mah battery from Adafruit). The keyboard is designed in KiCAD and FreeCAD, with the renders made with Blender.

# Features:
 - ZMK Firmware
 - Pro Micro Form Factor *
 - Wireless First Design
 - Split Spacebar
 - Low Profile (relative to other keyboards)
 - Hotswap Sockets
 - South facing (supports cherry profile)
 - Exploded 75% (ish) layout
 - Highly Customizable

# Why?
Because nobody has done such thing yet. I have always wanted a simple-looking, customizable (software-wise and hardware-wise), exploded 75% layout keyboard. In addition, it had to be under a certain price point. I estimate for it to cost less than 100 dollars for all the parts and all the machining, though that is subject to change. If you want CNC alu, then that'll cost you a couple cold hard Benjamins (tldr; a lot).

# Image Gallery
(subject to change as design alters)
<div style="display: flex;">
<img src="images/v1_1_render.jpg" style="width: 49.9%; height: auto">
<img src="images/pcb.jpeg" style="width: 49.9%; height: auto">
</div>

# Build Guide
### This build guide is very vague and will be improved on in the near future
### Parts:
> Note that these part links are only for reference. Some products can be found for cheaper (especially the hotswap sockets).

> The SPDT and SPST switches have specific footprints that match on the board. You can alter them if they're out of stock.

> You don't need to buy diodes if you are using SMT assembly. I used JLCPCB.
  - PCB
  - [Kailh Hotswap Sockets](https://shop.keyboard.io/products/kailh-hotswap-sockets-for-mx-style-keyswitches-x-25)
  - [Diodes (1N4148 SMT SOD-123)](https://www.adafruit.com/product/5099)
  - [SPDT Switch](https://www.adafruit.com/product/805)
  - [Battery (can be different capacity) with JST-PH 2 Pin Header](https://www.adafruit.com/product/1578)
  - [SPST Switch](https://www.adafruit.com/product/1489)
  - [JST-PH Right Angle Connector](https://www.adafruit.com/product/1769)
  - [Swiss Socket Headers (Female)](https://www.adafruit.com/product/3646)
  - [Swiss Socket Headers (Male)](https://www.adafruit.com/product/3647)

1. Order all the parts
   - I ordered everything off of JLCPCB, with SMT assembly for the diodes because I'm lazy. The pick and place/bom files are in the bom folder, ready for upload to JLCPCB. It is highly suggested you use SMT assembly because it is extremely cheap and saves a lot of time.
   - Apparantly, you can also get smt hotswap sockets assembled too, though I did not do that.
2. Solder it all together
   - Solder on the hotswap sockets and the nice!nano. This will take a while (perhaps an hour or two) depending on your soldering experience. Note that if you choose not to use SMT assembly on the PCB, the diodes will be very hard to solder. I socketed the nice!nano using Swiss machine pins off of Adafruit.
3. Build and flash the firmware onto the nice!nano
   - Build the firmware and put the nice!nano into bootloader (DFU) mode (short GND and RST twice in rapid succession). Drag the UF2 file into the nice!nano "storage device". The firmware can be made with my zmk-config directory.
4. Laser cut the case or 3D print
   - This step is pretty self explanatory. It's a sandwich design, so lasercut many pieces and adhere them together. The plate must be 1.5mm (+- 0.1mm). The rest can be any height as long as when everything is stacked together, it is taller than 15mm, and the height between the bottom of the plate and the top of the bottom pice is taller than 12mm.
   - Alternatively, you can 3D print the case. I decided to 3D print because it was faster to prototype. 2 file types, one split and one full depending on your bed size. It also looks really cool.
5. Put everything together
   - Glue it, screw it together, I don't really know. I screwed into a 3D printed case with some screws found in a bin of hope. Just make sure the entire thing fits. If you're that type of person, the more FLeX the better. Nylon should get you that. Plug in the battery (you might need to switch the battery wiring to make sure the GND goes into GND and RAW goes into RAW). You don't need screws to hold the PCB and plate together; the hotswap sockets and the plate should hold itself together. Get some 5mm foam and put it as dampener under the PCB. Make sure to keep the battery isolated when dampening so it doesn't short/blow up.
6. Use it
   - You've made it! Congrats! Customize the keymap, change the case material, it's all up to you. That's the beauty of open source hardware and software. I hope you enjoy the ByranTK-Alpha.

# License
Unless stated otherwise, the parts are licensed under the MIT License. Parts that are identified as (GPL) are licensed under the GPLv3 License.

\* The nice!nano v2 is used in this design. It has 3 extra pins in the center of the PCB, two of which the ByranTK-Alpha utilizes
