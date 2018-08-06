# ＤＣＺＩＡ ２０１８

```
 ___   ___ _____        ___ __  _ ___
|   \ / __|_  (_)__ _  |_  )  \/ ( _ )
| |) | (__ / /| / _` |  / / () | / _ \
|___/ \___/___|_\__,_| /___\__/|_\___/

 _________
| DCZ ■■ ⧻|
| □ □ □ □ |
| □ □ □ □ |
| □ □ □ □ |
|_□_□_□_□_|

```
**News**
August 2018
* FINAL INO is up use that for use with the final board.  
* ProtoDos is frozen for now. Library changes + board layout changes mean Final and Dos aren't really interchangable.

July 2018 Update 1
* ProtoDos code updated with BLE Code working and advertising to DC26 with 0X5050 Manufacturing ID
* Some ProtoDos code cleanup 


June 2018 Update
* Final board revision in the works. Expecting proto tres boards soon.
* Possibly switching OLED Libraries to U8G2 (https://github.com/olikraus/u8g2)
* Screen will likely be a 0.91" 128x32pixel OLED ala https://www.aliexpress.com/item/0-91-Inch-128x32-IIC-I2C-Blue-OLED-LCD-Display-DIY-Module-SSD1306-Driver-IC-DC/32793415973.html
	
May 2018  Update
* Proto Tres Board revision has begun.
* Please write down your ideas for lighting / BLE in the Google Doc for badge development.

March 2018 Update
* Proto Dos boards are in, working, and off to Lithochasm for redistribution with the keys

Feb 2018 Update
* Dev boards have been made by Hamster. He identified an issue with the footprint of the leds, and is working on a fix.
* Clear keycaps have begun printing by Litho. Switches and LED's for a dev board test have been ordered as well.
* Software developemt has not begun. 
* Goals for Feb, get dev boards up and in the hands of folks. 
* Ideas for software features
* Laynard Design


**What is the DCZia 2018 Badge**

This year we want to keep up with the tradition of our past badge which contained mechanical keyswitches on it to give it a retro look and feel. We decided on a 4x4 grid of mechanical keyswitches with an rgb led underneath and transparent keycaps to make an interactive display of sorts.

We also will be adding a small oled at the top center of the badge for more ovbious visual output. Board will be powered by an ESP32 and will talk BTLE and possibly Wi-Fi if we can find something cool to do with it.


Defcon2018 Style Guide: https://defcon.org/html/defcon-26/dc-26-theme.html


**Technical Notes**
* ESP32 Microcontroller
* SSD1306 OLED Screen
* Gatreon Blue Keyswitches
* Neopixel Mini RGB LEDs
* 2x or 3x AA power
* Shitty / Minibadge Addons supported

**DevKit Setup Instructions**

- Follow the [ESP32 Setup Instructions](https://github.com/espressif/arduino-esp32#installation-instructions) to get the latest board version. (NOTE: This is required to use BLE as there are recent updates)
- Compile and upload to your Proto-Dos board
- Enjoy all the fun menu settings, light show and BLE experience. 

To Test: 
- Use Nordic's nRF utility for the phone. 
- Review #badgelife's doc for BLE communication.  Compare to last year's badge to see the correct manufacturer ID and appearance.


**Old Notes**
* ESP32 - [Wemos Lolin ESP32 OLED Module For Arduino ESP32 OLED WiFi + Bluetooth](https://forum.arduino.cc/index.php?topic=495555.0)
* Keyswitches - SMD RGB Type Needed (They have clear casings allowing for SMD leds to shine through.
	* Gateron Blues / Whatevers - Clear top, white bottom. Supposedly the white bottom ones have the smd cutout $0.25ea[Gateron Blue (60G) Tactile Click Switches (Pack of 10) by Mechanical Keyboards Inc](https://mechanicalkeyboards.com/shop/index.php?l=product_detail&p=1272)
* Keycaps
	* DIY 3D Printed. STL File is now in repo.	
* Power - Lipo // AA’s? - Thinking AA's for ease of sourcing, and no need to fuss with lipo packs.

Prototype Board OLED Notes:
WeMos OLED 
I2C Data 5, Clock 4
[u8g2setupcpp · olikraus/u8g2 Wiki · GitHub](https://github.com/olikraus/u8g2/wiki/u8g2setupcpp#ssd1306-128x64_noname)

Constructor:  U8G2_SSD1306_128X64_NONAME_F_SW_I2C u8g2(U8G2_R0, 4, 5, U8X8_PIN_NONE);

#dczia
