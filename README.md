
# Building a small scale autonomous driving car using machine learning. 

This project is based on the open source [DIY Robocars](https://diyrobocars.com/) project so first of all, a huge thank you to that community and its contributors.

What I am going to build is a self-driving car at a 1/16 scale. The overall cost of the project will be around £250, depending on where you purchase parts and how good you are at shoplifting.

The DIY Robocar will navigate itself around a track autonomously without any input from its owner, using computer vision and machine learning running on a tiny onboard computer, the Raspberry Pi.

I'll look at each of the following steps in turn:

1. The overall goals
2. Hardware
3. Software
4. Training the model
5. Racing

## 1. Overall goals

The main goal of this project is to focus on the learning experience as a whole. The objective is to make and race pro-level autonomous car on a budget. That means it's smaller than the regular car (from go-kart size, down to 1/16th scale) and can be used indoors.

But just because it's small and cheap doesn't mean that it can't run real autonomous car software on them. As a matter of fact, both the Robocar and the real autonomous driving cars like the Google Waymo, Tesla, etc  are both on the kind of thesame continuum. They both use thesame technology, from Tensorflow to OpenCV to sensors and the cloud. But the cost of the robocar is roughly $200 while that of Google Waymo? $150,000? 

[![Compare](https://github.com/udohsolomon/Robocars/blob/master/Images/Robocar_compare.PNG)]()

**Why do we do this?** We do this because we always do things they don't do. We crash all the time and that helps us to iterate really fast and nobody gets hurt. Secondary, we race wheel-to-wheel and that is something no autonomous driving car manufacturers does. We race wheel-to-wheel every weekend. This is how some of the best automobile makers innovate. They race wheel-to-wheel. 

Rather than doing all processing on-board, this DIY Robocar tends to transmit the data from its on-board sensors (cameras, sonar, lidar, radar, GPS or whatever else I have) via Wifi to a laptop that runs pro-grade AI and robotics software, including TensorFlow, ROS and the rest of the Udacity Self-Driving Car nanodegree toolchain.


## 2. Hardware

Here is the *bill of materials* for the robocar


| Supplier     | Approximate Cost (£) | Tag  | Qty | Part description                                                                                                                                                       |
|--------------|-------------|----------------|-----|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Amazon     | 31          | R Pi           | 1   | Raspberry Pi 3 Model B Quad Core CPU 1.2 GHz 1 GB RAM Motherboard                                                                                 |
| Amazon     | 11          | SD             | 1   | SanDisk Ultra 32GB microSDHC Memory Card + SD Adapter with A1 App Performance up to 98MB/s, Class 10, U1 FFP                                                                         |
| Amazon     |  9          | Servo Driver   | 1   | HALJIA 16-Channel 12-bit PWM Servo Motor Driver I2C Module Board PCA9685 For Arduino / Robot / Raspberry Pi HALJIA                                            |
| Amazon     | 22          | Pi power       | 1   | Portable Charger iMuto 20000mAh Compact Power Bank External Battery with Smart LED Display Battery Pack for iPhone 7 6 6S Plus, Nintendo Switch, iPad, Samsung Galaxy, Smart Phones and More (Black) |
| Amazon     | 27          | Camera         | 1   | Raspberry Pi New Wide Angle Fish-Eye Camera   |
| Amazon     |  6	   | Jumper cables  | 1   | Elegoo 120pcs Multicolored Dupont Wire 40pin Male to Female, 40pin Male to Male, 40pin Female to Female Breadboard Jumper Wires Ribbon Cables Kit for arduino      						|
| HobbyKing    | 97          | Car            | 1   | Basher 1/16 4WD Mini Monster Truck V2 - Bad Bug (ARR)                                                                                                                  |
| HobbyKing    | 17          | Batteries      | 2   | Turnigy 1800mAh 2s 20c lipo-pack 
| HobbyKing    | 10          | Charger        | 1   | Turnigy E3 Compact 2S/3S Lipo Charger 100-240v (UK Plug)         |
| HobbyKing    |  2          | Battery Bag    | 1   | Turnigy® Fire Retardant LiPoly Battery Bag (190x68x50mm) (1pc)  |
| **Total**   | **232**     |                |     |

The Exceed Magnet as recommended on [DIY Robocars](https://diyrobocars.com/) is basically sold out in the UK, so I spent some good time trying to figure out an alternative. From ebay to aliexpress to amazon to hobbyking untill I found the 1/16 truck chassis. You may be lucky to find one if you carry out your search deligently but most RC cars with the almost ready to ride (ARR) will work just fine.
Here's what I came up with;

|  [![car](https://github.com/udohsolomon/Robocars/blob/master/Images/Car1.jpg)]() |  [![Chassis](https://github.com/udohsolomon/Robocars/blob/master/Images/Chassis.jpg)]() | 
|:---:|:---:|
| Car | Chassis |

There are two models selling with the same chassis. The AAR version ships from Europe, other variants may not. 

Here's the marketing video;

[![Video](https://img.youtube.com/vi/GdtnAzs16lQ/0.jpg)](https://www.youtube.com/watch?v=GdtnAzs16lQ)

The Raspberry Pi model 3 is the central computer of the Robocar. Robocar use Model B ( A1.2GHz 64-bit quad-core ARMv8 CPU, 1GB RAM), a small but powerful computer.

[![car](https://github.com/udohsolomon/Robocars/blob/master/Images/raspberry.jpg)]()

Next steps: 
- **Mounting:** Obviously the stock 3D printed parts are not going to fit, so will need to improvise. I am considering using a cardboard. I want to make a design with flexibility for mounting more sensors and also good compactment for placing the power bank. I will wait until the car arrives to make measurements. 
- **Software Installation**

## 3. Software









