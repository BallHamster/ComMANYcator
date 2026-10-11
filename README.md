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
<img src="images/3d.png" alt="3d render" width="600">

### LEDs:
<img src="images/led layout.png" alt="LED layout" width="600">
Blue represents TSAL6400 at 45°, Red represents TSAL6100 at 0° in the middle, and 15° in the middle

## Software
Software is based on ESPhome, and it is hypothetical, as I cannot test it.

**Installation guide**
1. Install esphome device builder (https://esphome.io/install/)
2. Create and name a new project
3. Edit the .yaml file to match DEMO.yaml (change pins, codes, passwords etc)
4. Write to esp

# IMPORTANT
- I did not make Esphome.
- I cannot test the software, so this is hypotethical. When i recieve it, I'll make a v2!!!!

### BOM
|Ref no      |Part                 |Pcs|Min order|Importer|MPN                    |Link                                                                                                   |Price for minimum/needed($)|
|------------|---------------------|---|---------|--------|-----------------------|-------------------------------------------------------------------------------------------------------|---------------------------|
|D1-D4       |IR LED 940 nm        |4  |5        |LCSC    |TSAL6100               |https://www.lcsc.com/product-detail/C111836.html                                                       |0.99                       |
|D5-D6       |IR LED 940 nm, 25 fok|2  |5        |LCSC    |TSAL6400               |https://www.lcsc.com/product-detail/C94857.html                                                        |0.99                       |
|U5          |IR vevo 38 kHz       |1  |1        |LCSC    |TSOP38438              |https://www.lcsc.com/product-detail/C145271.html                                                       |1.27                       |
|U2          |IR vevo tanitashoz   |1  |2        |Ebay    |TSMP58000              |https://www.ebay.com/itm/285265795138                                                                  |2.00                       |
|U6          |Buck szabalyzo 3 A   |1  |1        |Farnell |TPS62130RGTR           |https://ie.farnell.com/en-DK/texas-instruments/tps62130rgtr/dc-dc-conv-sync-buck-2-5mhz-vqfn/dp/3121894|1.82                       |
|L1          |Induktor 2,2 uH      |1  |1        |LCSC    |XFL4020-222MEC         |https://www.lcsc.com/product-detail/C122469.html                                                       |4.22                       |
|Q1-Q2       |N-MOSFET SOT-23      |2  |2        |LCSC    |AO3400A (Alpha & Omega)|https://www.lcsc.com/product-detail/C20917.html                                                        |0.45                       |
|J1          |USB-C 16P            |1  |1        |LCSC    |HC-TYPE-C-16P-01A-R    |https://www.lcsc.com/product-detail/C2997433.html                                                      |0.82                       |
|J2          |3,5 mm jack          |1  |1        |LCSC    |SJ1-3533NG             |https://www.lcsc.com/product-detail/C4992459.html                                                      |1.66                       |
|C3          |100 nF 50 V X7R THT  |1  |10       |LCSC    |CT4-0805B104K500F1     |https://www.lcsc.com/product-detail/C168753.html                                                       |0.47                       |
|R8, R11, R13|100 kOhm 1%          |3  |50       |LCSC    |MF1/4W-100K 1% (CCO)   |https://www.lcsc.com/product-detail/C119369.html                                                       |0.56                       |
|C1          |3,3 nF 50 V X7R THT  |1  |10       |Farnell |K332K15X7RF5TL2        |https://ie.farnell.com/vishay/k332k15x7rf5tl2/cap-3300pf-50v-mlcc-radial/dp/3289405                    |1.17                       |
|C2          |10 uF 16 V radialis  |1  |1        |Farnell |ECE-A1CKS100           |https://ie.farnell.com/panasonic/ecea1cks100/cap-alu-elec-10uf-16vdc-radial/dp/1901997                 |0.27                       |
|C4          |22 uF 25 V X5R 1206  |1  |5        |Farnell |CC1206KKX5R8BB226      |https://ie.farnell.com/yageo/cc1206kkx5r8bb226/cap-22uf-25v-mlcc-1206/dp/3873451                       |2.80                       |
|C5, C6      |4,7 uF radialis      |2  |2        |Farnell |ECE-A1EKS4R7           |https://ie.farnell.com/panasonic/ecea1eks4r7/cap-4-7-f-25v-20/dp/1902002                               |0.51                       |
|R1-R6, R12  |22 Ohm 0,6 W         |7  |10       |Farnell |MRS25000C2209FCT00     |https://ie.farnell.com/vishay/mrs25000c2209fct00/res-22r-1-600mw-axial-metal-film/dp/9466126           |1.29                       |
|R7          |316 kOhm 1%          |1  |10       |Farnell |MRS25000C3163FCT00     |https://ie.farnell.com/vishay/mrs25000c3163fct00/res-316k-1-600mw-axial-metal-film/dp/9467238          |1.29                       |
|R9, R10     |5,1 kOhm 1%          |2  |10       |Farnell |MRS25000C5101FCT00     |https://ie.farnell.com/vishay/mrs25000c5101fct00/res-5k1-1-600mw-axial-metal-film/dp/9469184           |1.30                       |
|R14, R15    |100 Ohm 1%           |2  |10       |Farnell |MRS25000C1000FCT00     |https://ie.farnell.com/vishay/mrs25000c1000fct00/res-100r-1-600mw-axial-metal-film/dp/9463909          |1.29                       |
|R16-R18     |10 kOhm 1%           |3  |10       |Farnell |MRS25000C1002FCT00     |https://ie.farnell.com/vishay/mrs25000c1002fct00/res-10k-1-600mw-axial-metal-film/dp/9463976           |0.80                       |

