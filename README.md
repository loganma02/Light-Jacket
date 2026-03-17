# Spec-tr0 Light Jacket

![Person wearing light jacket glowing green while standing in alley](Images/outside.jpg)

In this project I set out to make a jacket for a costume with which I could change colors and pulse lights in a pattern,
[WLED](https://github.com/WLED/WLED) allowed for app-based control and minimal fiddling once powered on.

## <ins>PCB Update March 2026 </ins>
![PCB 2D View](PCB/Images/2D%20View.png)
Currently awaiting delivery of a prototype PCB board for this jacket. Using an ESP32-S3 and a digital microphone to make audio reactivity possible with WLED.
Chose to use USB-C for programming and power due to availability of cables, and the USB-A plug (but not the full standard) for the connection to the lights. Exploring USB-C plug or magnetic connectors for this purpose.
Gerber files can be found [here](PCB/LightJacketV0.1.zip).
![PCB 3D View 1](PCB/Images/3D%20View%201.png)
![PCB 3D View 2](PCB/Images/3D%20View%202.png)


## Jacket Construction
![Jacket unfurled showing strip and circuit board](Images/open.jpg)
<img src="Images/open.jpg" width="400" alt="Jacket unfurled showing strip and circuit board">

The strip runs hidden along the inside next to the zipper for an ambient lighting effect, and visible around the collar for the exposed design choice.
The battery and circuit board tuck into an existing pocket on the inside.

![Inside of jacket showing LED strip sewn in](Images/sewing.jpg)
I decided to sew in the strip for durability rather than use adhesive, and tried to match existing seam lines.

## Circuitry
I used an ESP8266 and a single color RGB LED strip as that's what I had on hand, but opting for a ESP32 increases options available for WLED, and addressable LED strips allow for more impressive patterns to be displayed.
WLED has an option to control single color strips with PWM signals for each RGB channel, and I fed signal each into a transistor to boost the power for that channel.
Power is supplied by a phone battery bank connected by a USB cable spliced to provide 5V to the ESP as well as each transistor. 
![3 transistors visible on perfboard with wires visible leading to power bank and LED strip](Images/transistorSide.jpg)
*Transistor side of perfboard*

![ESP8266 soldered to perfboard](Images/boardSide.jpg)
*ESP8266 on perfboard*

## Next steps
I would like to upgrade the microcontroller to an ESP32 and add a microphone, as WLED has better support for audio reactivity on that board.
Ultimately want the jacket to react to sounds, such as pulsing along to the beat of music on a dancefloor, or visually alerting the user to a dangerously loud environment.

## Images
![Jacket worn, illuminated green](Images/green.jpg)
![Jacket worn, illuminated blue](Images/blue.jpg)
![Light Jacket illuminated blue laid out on table](Images/closedCrop.jpg)
