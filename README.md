# DE1-projekt

Topic 1: Smart Parking System with Ultrasonic Sensors

Description: Design and implement a smart parking system using VHDL on the Nexys A7 FPGA board. The system will utilize multiple ultrasonic sensors (HS-SR04) connected to the Pmod connectors for detecting the presence and distance of vehicles within parking spaces. Develop algorithms to analyze sensor data and determine parking space availability. Visualize parking space occupancy status using LEDs, while displaying distance measurements on the 7-segment display.
![image](https://github.com/Falconer546/DE1-projekt/assets/114109685/959aafb0-10b1-4fa5-93ed-fb0b40ed43ce)

# Team members

Jan Božejovský, Tomáš Fešar, Roman Knížek, Jiří Vašulín

[Link to GitHub project folder](https://github.com/Falconer546/DE1-projekt)
# Hardware used

Nexys A7-50T

FPGA
|![FPGA](https://github.com/Falconer546/DE1-projekt/blob/main/nexys-a7-obl-600.png)|
|:--:| 
|*Nexys A7-50T*|
https://digilent.com/reference/programmable-logic/nexys-a7/start



HC-SR04
Ultrasonic distance sensor
|![sensor](https://github.com/Falconer546/DE1-projekt/blob/main/sensor.jpg)|
|:--:| 
|*Sensor HC-SR04*|
https://navody.dratek.cz/navody-k-produktum/meric-vzdalenosti-ultrazvukovy.html



# VHDL modules description

#### Ultrasonic sensor utilizes two blocks
The 'echo_triger' block directly tells the HC-SR04 sensor to emit a pulse.
The 'distance_measure' block processes the returned distance, which it converts to 16 levels, which are then used in other modules.

Code for echo_triger module
https://github.com/Falconer546/DE1-projekt/blob/main/echo_triger

Code for distance_measure module
https://github.com/Falconer546/DE1-projekt/blob/main/distance_measure

#### PS_availability module description

PS_availability module decides if the Parking Space is empty or not and controls LED signaling.
https://github.com/Falconer546/DE1-projekt/blob/main/PS_availability

#### Bin2seg module description

Bin2seg module translate binary output from distance_measure for seven-segment display.
https://github.com/Falconer546/DE1-projekt/blob/main/bin2seg

#### Top_level module description

Top_level module contains all above modules. It connects them together with hardware components.
https://github.com/Falconer546/DE1-projekt/blob/main/top_level





