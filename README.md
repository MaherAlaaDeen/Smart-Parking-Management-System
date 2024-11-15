# Smart-Parking-Management-System
## Abstract
The purpose of this project is to design and implement a Smart Parking Management System integrating Arduino and MATLAB technologies. This inventive smart system aims to solve parking management problems and challenges by proposing an intelligent, cost-effective solution. With the help of MATLAB GUI, the system would be controlled and monitored, allowing the optimization of parking space utilization while minimizing costs. This project serves as a useful demonstration of the microcontroller technology in enhancing real-life problems, offering smart and efficient solutions.

## Introduction and Objectives
Nowadays almost every family own a car or two to be used in the transportation needs. Widening and generalizing this scope to describe for example big cities will definitely cause serious problems that start with traffic jam, unnecessary accidents and the decrease and unorganized parking of parks in the streets. In order to find a practical solution, a Smart Parking Management System is designed and explained in this report. The objectives of the system can be summarized in the following:
1.	Design a Low-cost and effective solution using Arduino.
2.	Integrate MATLAB to create a Graphical user Interface to control the system and receive feedback.
3.	Implement a prototype of the design to be tested in a small real-time simulation to assess the effectiveness of the Control system.

## Requirements
Hardware Requirements:

1.	Arduino Uno R3 x1                                                                                            
2.	Test Board x1
3.	IR Sensor x2
4.	Green LED x1
5.	Red LED x1
6.	Yellow LED x1
7.	Jumper Wires
8.	Servo Motor x1
9.	Resistor 220 Ω x3

Software Requirements:

1.MATLAB

## Project Development Procedures
This project consists of two parts, the GUI using MATLAB design and the system design and implementation with Arduino microcontroller. We will start by preparing and programming the GUI with MATLAB.
MATLAB enables us to create a graphical user interface that should first of all contain two buttons in order to start and stop the system as needed. In addition to that, the window should also show the status of the system if either “ON” or “OFF”. We can never forget that the GUI will definitely show the vacant and occupied spaces in the parking lot and a text label to indicate the number of free remaining parking lots. This will enable the user to visualize and read the free spaces as the free space will be colored in green and when occupied the slot will turn color into red.

![GUI](GUI.png)

The second part of the system consists of the hardware part. With the help of the Arduino that is a programmable microcontroller that has analog and digital pins that can be configured as inputs or outputs. A servo motor will be attached to the controller acting as the parking barrier that will remain closed until a car enters or leaves the parking. For the purpose of detecting leaving and entering cars, we’ll be using 2 Infrared Sensors that are positioned respectively before and after the barrier, so we’ll be expecting 2 scenarios:
1. Entering Cars:
   If sensor 1 detects then the barrier will open and won’t close until the second sensor detects which means that the car has passed the barrier and is already in the         parking.  If the parking spaces left are equal to zero, the barrier won’t open until a car leaves the parking.
2. Leaving Cars:
   When leaving the parking, it is logical that the 2nd sensor IR sensor will be detecting first. So similarly, when it detects the barrier will open and won’t close until the 1st IR sensor detects the car.

Three LEDs are also implemented: a Green LED stating that the system is ON, a red LED 
Indicating that the system is OFF and finally a Yellow LED turns ON when there are free parking lots inside the parking and will turn OFF if the parking is full.

## Schematic Representation

![Schematic](schematic.png)

## Flow Chart

![Flow Chart](Flowchart.png)

## MATLAB Code

```matlab
fig = figure('Name', 'Smart Parking Management System', 'NumberTitle', 'off', 'Position', [100, 100, 350, 250]);
```
