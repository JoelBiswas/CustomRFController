# Custom Star Wars RF Controller
This repository contains the files to build a custom RF controller in the shape of the Rebel Alliance Logo from Star Wars. The controller consists of two joysticks, six buttons, and is controlled by an ESP32. This project was created entirely by me for Hack Club's Highway to Undercity event. My plan is to test this device by using to control an [R2-D2 droid that I designed](https://github.com/JoelBiswas/r2d2/tree/main) for the same Hack Club event earlier this summer.

![TopView](https://github.com/user-attachments/assets/143f9d58-209f-4534-bad4-7e8569faec4b)

## Bill of Materials
View the Bill of Materials [here](https://docs.google.com/spreadsheets/d/1eimf_XqeCwkksVUzqHQLZJRxSmD6-AT-35apM8Ljc3Q/edit?usp=sharing)

<img width="1220" alt="Screenshot 2025-06-19 at 11 42 58 AM" src="https://github.com/user-attachments/assets/1d4440ea-4282-4e6d-875e-3e4d190041e1" />



## The Beginning
The idea for this project came after finishing my last project, an R2-D2 droid controlled with a PS3 controller. I thought that it would be interesting to make my own Star Wars-themed RF transmitter to control the droid with. I hoped that this would provide the robot with much greater range than a Bluetooth-based controller. This project felt perfect as I was looking to start a project that expands my electrical skills. My last project was heavily focused on CAD, so I wanted this project to be more focused on wiring schematic and PCB design. Like the droid, this project is also made for Hack Club's Highway to Undercity event, which provides high school students with grants to build their dream projects.

## About the Controller
The controller consists of two main parts: the PCB and the case. The PCB consists of an ESP32, two MP1584 buck converters, two KY-023 Joystick Modules, six push buttons, and an nRF24L01+ PA/LNA RF Module. It is powered by a 2S LiPo battery that connects to the PCB using a Deans Connector. The case is 3D-printable and houses the battery and PCB. The two joysticks are labeled LS and RS, and the buttons are labeled A, B, X, Y, 1, and 2. An antenna on the PCB extends up through a hole in the top of the case in order to transmit the RF signals.

## Overview of this Repo
**CAD** - Contains the CAD files for the controller, along with images taken from OnShape. <br>
**STLs** - Contains files for each part that needs to be 3D printed <br>
**Print** - Contains the 3d print files for the Flashforge Adventurer 5M <br>
**Electrical** - Contains files from KiCAD for the controller's wiring schematic, custom symbols, custom footprints, and PCB <br>
**Code** - Currently empty but will eventually contain the code for sending RF signals <br>
**JOURNAL.md** - Contains an overview of exactly how I designed and built this robot <br>
**BOM.csv** - A bill of materials for this project in CSV format <br>

## Designing the Robot
Click [here](https://cad.onshape.com/documents/af772411fd2681a1311b7be6/w/e5e3a94108ce63d65661e1b4/e/943c3c2dcbac8496e1ce6b2c?renderMode=0&uiState=685208efd1f4554e80aaa1d0) to view the Onshape document for this project. The electronic design was done in KiCAD.

![CAD](https://github.com/user-attachments/assets/7fa022fe-0a6a-4016-999e-9c11c06d1726)
![PCB](https://github.com/user-attachments/assets/af27cc4c-65ff-477b-8f1e-f8973b74a2fd)

## General Steps for Assembly
1. 3D print each of the files in the STLs folder. The case top and bottom should be printed in orange PLA, and the button should be printed six times in black PLA.
2. Place the LiPo battery into the inserts in the case
3. Place the PCB over the battery on the standoffs. Plug the battery into the Deans connector on the PCB
4. Bolt in the top of the case using an M3 bolt on each side
5. Hot glue the 3D printed button onto the PCB buttons
