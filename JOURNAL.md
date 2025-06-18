---
title: "Custom RF Controller"
author: "Joel Biswas"
description: "Custom RF controller with two joysticks, two triggers, and four buttons"
created_at: "2025-06-10"
---

**Total Time Spent:** 29 hours

### DAY ONE - June 11, 2025
I spent today creating a wiring schematic for this project, as making an RC controller is fairly electrically intensive. The schematic uses an ESP32-DevKitC for the microcontroller, two KY-023 modules for the joysticks, two MP1584 modules for the buck converters, an nRF24l01+ PA/LNA module for the RF transmitter, six buttons, and a Deans Connector for the battery. Because KiCAD does not include modules in its symbol libraries, I had to create custom symbols for the ESP32-DevKitC, the KY-023, the MP1584, and the nRF24L01. I used one buck convertor to reduce the battery's 7.4V to 5V, and a second buck convertor to convert the 5V to 3.3V.

<img src="https://github.com/user-attachments/assets/f783ed2a-6049-492f-ae0b-d9b525c104f8" alt="Day One Schematic" height="300"/>
<img src="https://github.com/user-attachments/assets/984a7c78-9517-4194-9075-0ddf7ee34ff8" alt="Day One Symbol" height="300"/>

**Time Spent:** 8 hours

### DAY TWO - June 12, 2025
Today, I created custom footprints for 5 different comonenents on my PCB. This was my first time creating footprints, so it took me longer than expected. The first one was the most difficult: a footprint for the Deans Connector. This connector would allow the battery to connect to the PCB. I also created a footprint for the ESP32-DevKitC, the MP1584 module, the nRF24L01+ PA/LNA module, and the KY-023 module. I then found 3D STEP models for each of these components on grabcad, and added the models into KiCAD.

<img src="https://github.com/user-attachments/assets/a480dcd4-bda7-4800-8cf6-c664cf602fdf" alt="Day Two Deans" height="300"/>
<img src="https://github.com/user-attachments/assets/707123ff-6d25-4457-84df-0916481dd952" alt="Day Two ESP" height="300"/>

**Time Spent:** 6 hours

### DAY THREE - June 14, 2025
Today, I finally designed the PCB! I made a sketch of the PCB outline in OnShape, then exported the sketch as a DXF file and placed it into KiCAD, in the Edge.Cuts later. I then began positioning the components where I wanted them to be on the final design. I placed the ESP32 in the center, one joystick on each side, four buttons in the middle, and two buttons on the bottom. I also placed the RF module in the middle, so that the antenna could could extrude from the middle of the case. I used a ground pour on both sides to make sure that all components are correctly connected to ground. I then added all the necessary traces to finish the PCB

<img src="https://github.com/user-attachments/assets/3f4cd480-b6be-442b-8109-4eccb07a5b20" alt="Day Three PCB" height="300"/>
<img src="https://github.com/user-attachments/assets/04cf4a6b-b6dd-450a-85aa-4e1c75919d5c" alt="Day Three 3D PCB" height="300"/>

**Time Spent:** 8 hours

### DAY FOUR - June 16, 2025
I spent today finishing the CAD model for the controller. I first imported the STEP file for the PCB from KiCAD into Onshape. I then designed a mount for the battery, standoffs for the PCB to be mounted to, and a top section to cover the electronics. I also designed 3D-printable buttons that could be hot-glued to the electronic buttons. These would allow the buttons to be pushed even when the electronics are covered up

<img src="https://github.com/user-attachments/assets/d933da8e-647f-4e0b-9904-76ed739f1bcd" alt="Day Four Battery + Case" height="300"/>
<img src="https://github.com/user-attachments/assets/f88cbae0-1811-4eb4-b524-ecdc657caca3" alt="Day Four Electronics + Case" height="300"/>


**Time Spent**: 5 hours

### DAY FIVE - June 17
Today, I finished setting up this GitHub repository. I added folders for the electrical files and design files. I also added an empty folder for code that will be added to after the controller is assembled. The project is noe ready to be shipped!

**Time Spent:** 2 hours
