# ComMANYcator
An esp32 based project, capable of communicating with IR, and RF

**Hello, and welcome to my project, ComMANYcator. This project is made for Hack Club's Half-life event.**
## Why did I make this project?
For years, i have been in war with the many remotes I have in my home. So I decided to make a change, and fabricate this project, wich uses IR blasters and recievers, and two RF moudles (on 433Mhz and 868Mhz)

The project uses the main parts below:
- ESP32 C6 DevboardC-1
- 2x CC1101 RF modules from alliexpress
- TSAL 6100 & 6400 IR leds
- TSOP 38438 & TSMP 58000 IR recievers
- TPS 62130 5v to 3.3v converter

## The Schematic design

<img src="images/FINAL WIRE.png" alt="Schematic" width="600">
This is the final scmeatic for the pcb. In the top left corner is the usb-c and 5v to 3.3v converter region (so power region.)
In the bottom left corner are the IR LEDs and an external port for commercial IR blasters.
In the middle, is the brain of the project, the esp32 c6.
Below and right of the esp are the RF modules.
Above the esp are the IR recievers.

## The pcb layout & wiring
<img src="images/PCB FINAL.png" alt="PCB layout" width="600">
This is the final layout design, and the routing done. 

### Broken down:
<img src="images/led layout.png" alt="LED layout" width="600">

