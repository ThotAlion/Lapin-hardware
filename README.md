# Lapin-hardware
---
# Hardware of the lapin biped robot

Here is gathered the hardware of the robot, and the BOM. This can change during the search on this robot
![Overview](https://raw.githubusercontent.com/ThotAlion/Lapin-hardware/master/photo1.jpg)

---

## Mechanical constraints and golden rules

**Golden rule 1 :** A dynamic biped robot shall fall without breaking. Systems which hold the robot for security disturb the dynamics

**Golden rule 2 :** A dynamic biped robot shall be stable around twist axis. If a torque is applied around the vertical axis while the robot is standing, the gripping of the feet shall prevent turning

**Golden rule 3 :** A dynamic biped robot shall have the gravity center the higher to increase the natural period of the balancing.

---

## Bunch of material

Here is the bunch of material for my robot but it can be adapted for yours.

### Motors

The robot need high torque and high quality motors for research purpose.Maybe later it can be useful to reduce motor costs but for now, make it walk. Moreover, these motors can be used for others future projects.

- 2 x Dynamixel [MX-64AT](http://www.robotis.us/dynamixel-mx-64at/) 262€ each
- 6 x Dynamixel [MX-28AT](http://www.robotis.us/dynamixel-mx-28at/) 203€ each
- 2 x U frame for MX-64 with bearing [FR05-H101 Set](http://www.robotis.us/fr05-h101-set/) 25€ each
- 6 x U frame for MX-28 with bearing [FR07-H101 Set](http://www.robotis.us/fr07-h101-set/) 24€ each
- 4 x plates for MX-28 [FR07-S101](http://www.robotis.us/fr07-s101-set/) 10€ each
- 2 x plates for MX-64 [FR05-S101](http://www.robotis.us/fr05-s101-set/) 13€ each
- Dynamixel USB controller [U2D2](http://www.robotis.us/u2d2/) or [USB2AX](https://www.generationrobots.com/fr/401584-usb2ax-pour-servomoteurs-dynamixel.html)
- 2 x sets of 100mm Dynamixel [3P cables(x 10)](http://www.robotis.us/robot-cable-3p-100mm-10pcs/)
- 1 custom Y dynamixel cable from the dynamixel controller to the two legs (avoid dynamixel hub because of the schocks)
- 2 x custom dynamixel cables of 350mm from MX-64 knee to MX-28 ankle

### Power
- 1 x 3S LIPO battery
- 1 x [kit of male/female T-connectors](https://fr.aliexpress.com/item/4001351319074.html)
- 1 x 10A Emergency stop button
- 1 x [25W switching regulator](https://www.robotshop.com/eu/fr/regulateur-de-swadj3-dimension-engineering.html?utm_source=google&utm_medium=surfaces&utm_campaign=surfaces_across_google_eufr&gclid=EAIaIQobChMIvMvWnPz06wIViPdRCh0y1wcxEAQYBCABEgKcp_D_BwE)

### Computer

- 1 x Raspberry Pi 3 or 4
- 1 x 16Go SDCard

### Sensors

The robot is sensitive to ground contact and inertial measurement with a high rate and high speed (approach 100Hz). All is gathered around a dedicated Arduino.

- 1 x Arduino 
  - [Nano 3.0](https://store.arduino.cc/arduino-nano)
  - [Nano Every](https://store.arduino.cc/arduino-nano-every-with-headers) even if I have problem of I²C stability on this card to be investigated with respect to MPU6050 (spurious freeze)
- 1 x I²C IMU 
  - for the moment I use [INVENSENSE MPU6050](https://fr.aliexpress.com/item/32670910753.html) but I have software stability issue using the embedded DMP 
  -  [BOSCH BNO055](https://fr.aliexpress.com/item/4000686420656.html) on its way to test

- 4 x [5kg force sensor beams with HX711 A2D converter](https://fr.aliexpress.com/item/33046501052.html)
- 2 x [3D printed HX711 housing](https://cad.onshape.com/documents/89773ebe7e884f666a84c098/w/31c162daa679029f3b9fda3b/e/070fb8623ed9564c90b82de8)
- 1 x [band of 15 Neopixel WS2812 - 1M 60 IP30](https://fr.aliexpress.com/item/2036819167.html)

### mechanical leg structure

All 3D printed parts are designed on OnShape in [this project](https://cad.onshape.com/documents/fe91fe1ed7270e269f4c2873/w/a1669b9394a00a6c775fa6e8/e/9fc7b1788347e23db4327b82).
STLfiles have been exported in this repo.

- 2 x [1m long Makerbeam XL](https://www.makerbeam.com/1000mm-1p-makerbeamxl-15mmx15mm.html)
- 1 x [kit of Makerbeam bolts](https://www.makerbeam.com/openbeam-button-head-socket-bolt-6mm-100p-for-open.html)
- 1 x [kit of slot nuts](https://www.makerbeam.com/t-slot-nuts-for-makerbeamxl-50p.html)
- 12 bearings Inner diameter : 6mm, outer diameter 19mm, thickness : 6mm
- 6 x 6mm diameter 40mm long steel axes
- 4 x 3D printed makerbeamXL outerhinge
- 6 x 3D printed makerbeamXL innerhinge
- 2 x 3D printed makerbeamXL outerhingeplate
- 4 x 3D printed makerbeamXL headplate
- 1 x kit of standard kitchen rubber bands diameter : 50mm, thickness : 5mm

### foot

work in progress

### around
- 1 x [spiral wire protection 6mm diameter x 15m long](https://fr.aliexpress.com/item/4001090365450.html) to handle schocks and prevent wire cut during fall
- 1 x [kit of female connectors over PCB](https://fr.aliexpress.com/item/32983464320.html)
- 1 x [kit of female/male connectors over wires](https://fr.aliexpress.com/item/32960322306.html)
