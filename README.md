# Nissan-LEAF-Inverter-Upgrade ⚡
Software for extracting more power from LEAF inverter upgrades. Enables 110kW and 160kW inverters to function with the older LEAF

## Disclaimer ⚠️
Tuning electric vehicles can be very dangerous. I take no responsibility (see license) for any damages that this firmware might cause. You are entirely on your own when using this software. Respect your local legislation.

## How to use ❓
Now that we got that out of the way, here's what you need to get started.
- A 2013-2017 Nissan LEAF (AZE0 model)
- Some Nissan spec coolant might be a good idea, or distilled water. When removing the inverter some coolant can be lost!
- A newer inverter from a 2018+ ZE1 LEAF (see this video for installation: https://www.youtube.com/watch?v=VGBA8VPWwIg )
- Leafspy Pro to code in the new resolver offset (see this video for howto: https://www.youtube.com/watch?v=K0v269B0xqo )
* A CAN-bridge with the firmware in this repository flashed onto it. The CAN-bridge attaches anywhere between the VCM and INV on EV-CAN. The following CAN bridges have compatibility
    * 2-port [AliExpress "MB CAN Filter 18 in 1](https://www.aliexpress.com/item/1005003112723581.html?)
    * 3-port Muxsan CAN-bridge https://www.tindie.com/products/muxsan/can-mitm-bridge-3-port-rev-25/
* Pre-compiled binaries are available in the [Releases](https://github.com/dalathegreat/Nissan-LEAF-Inverter-Upgrade/releases) Flashing instructions:
    * 2-port, see https://github.com/dalathegreat/Nissan-LEAF-Battery-Upgrade/tree/main#software-needed-to-flash	 
    * 3-port https://youtu.be/eLcNSo2Vn6U?t=167

## FAQ 🔍
- Q: Why doesn't this work on my 2011-2012 LEAF? A: The early leaf has EM61 motors. These aren't compatible with the EM57 inverter style.
- Q: Will this work on my 2018+ 40kWh 110kW LEAF? A: Yes, the 160kW inverter can be fitted to this model. It is mechanically plug and play. Pair in the resolver offset with Leafspy. To get full power out of the upgrade, a CAN bridge is needed (otherwise the 160kW inverter will be operating as a 110kW inverter)
- Q: What is resolver offset coding? A: See this video for more info: https://www.youtube.com/watch?v=Of2vCYgblY4
- Q: Are there any weight savings? A: The 110kW inverter is 3.5kg lighter than the 80kW

## Part numbers 🔢
Here are the part numbers so you know what to get when ordering inverters
ZE1 inverters (2018-2022)
- 291A0-5SA1A - 110kW inverter
- 291A0-5SA1B - 110kW inverter
- 291A0-5SA0A - 110kW inverter
- 291A0-5SN0A - 160kW inverter
- 291A0-5SN1A - 160kW inverter

22-pin Yazaki wiring part number: 7283-8750-30
Buy link: https://nl.aliexpress.com/item/1005003344398420.html?spm=a2g0s.9042311.0.0.25994c4doh13qv

Temperature sensor (no link yet, just use butt-crimp connectors)

Don't get these, just listed so you know what they are.
AZE0 inverters (2013-2017)
291A0-3NF1B - 80kW 
291A0-3NF1A - 80kW
291A0-3NF0A - 80kW
ZE0 inverters (2011-2012)
291A0-3NA0A - 80kW

## Example installation pics and wiring info 👉
Here's where the CAN-bridge attaches, behind the glovebox on the left connector going into the VCM. The EV-CAN is a twisted pair green/blue cable. Cut it and install the CAN-bridge wires there.
The other two wires that the CAN-bridge needs is +12V constant(red wire) and GND(black wire). +12V constant can be taken from many places, e.g. OBD2port.

![name-of-you-image](https://github.com/dalathegreat/Nissan-LEAF-Inverter-Upgrade/blob/main/Pictures/CAN-bridge1.jpeg)
![name-of-you-image](https://github.com/dalathegreat/Nissan-LEAF-Inverter-Upgrade/blob/main/Pictures/CAN-bridge2.jpeg)
![name-of-you-image](https://github.com/dalathegreat/Nissan-LEAF-Inverter-Upgrade/blob/main/Pictures/CAN-bridge3.jpeg)

Here are the differences in wiring. Please note that one wire is different color, all the rest matches!
![name-of-you-image](https://github.com/dalathegreat/Nissan-LEAF-Inverter-Upgrade/blob/main/Pictures/Wiring.png)
![name-of-you-image](https://github.com/dalathegreat/Nissan-LEAF-Inverter-Upgrade/blob/main/Pictures/Wiring2.png)

## Like this project? 💖
Leave a ⭐ If you think this project is useful. Consider hopping onto my Patreon to encourage more open-source projects!

<a href="https://www.patreon.com/dala">
	<img src="https://c5.patreon.com/external/logo/become_a_patron_button@2x.png" width="160">
</a>
