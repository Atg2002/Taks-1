
# 1)Biometric Attendence system

The main objective of the project to build a Biometric attendence system, one which is commonly found in offices, schools, etc. and is an effective time saving way for registering a persons attendence.


## Componenets
+ Arduino Uno
+ Fingerprint sensor - R305(Optical Fingerprint senor)
+ RTC module
+ Pushbuttons
+ LEDS
+ LCD
+ Jumper Wires

## Description
We will be suing R305 sensor to register or authenticate a fingerprint. We will be using 4 pushbuttons
for :

+ Register/Back Button – Used to either enroll new fingerprint / Go Back
+ Delete/OK Button –  Used to delete or access an earlier stored fingerprint.
+ Forward Button – Used for moving forward while selecting the memory location for storing or deleting fingerprints.
+ Reverse Button – Used for moving backward while selecting memory location for storing or deleting fingerprints.

The RTC module wil be used to store the scanning, entry or exit time.
LCD shall be used to print out various commands or display whats going on.

## Circuit
![image](https://user-images.githubusercontent.com/94821815/174437430-3b0cbdec-8cae-44e3-822f-e4cb0a1b70fe.png)

## Improvements
Interface the current project with a web server to display attendence record along with entry and exit time.


# 2)Soil Moisture Monitoring

The main objective is to obtain data regarding LoRa Soil Moisture sensor and upload it to a webserver.

## Componenets
+ LoRa Soil Moisture sensor
+ LoRa ESP32 Gateway shield
+ USB Data-Cable
+ FTDI module( CP2104 USB-TTL Module used)
+ Battery
+ MakePython ESP32 Board

## Description
The LoRa Soil Moisture sensor regularly (every 5 seconds, this time can be modified) sends data using Radio.
It consists of AHT10 Sensor which collects local air temperature & humidityand Capacitive Soil Moisture Sensor which detects the soil humidity.It also uses 555 timer.
The LoRa module RFM95 is used to send data to the gateway.To program the sensor we would need a
USB-TTL convertor.

The receiver is also made ESP32(coded in micropython) and LoRa Module. The receiver collects the data from theSensor Nodes. Then receiver creates a local Web Server using 
the ESP32 inbuilt library function. You can access the web page using the IP Address that appears on the OLED display on ESP32.

## Working 
![Project 6](https://user-images.githubusercontent.com/94821815/174439407-efabc1b5-bb96-4632-ad2b-24973a86b099.gif)
## Improvements
+ The microcontroller part of Soil moisture sensor is not waterproof, severly limiting capabilities during monsoon.Need a waterproof box or equivalent which would not effect the transmission.
+ Couble this project with automated irrigation system to automatically irrigate fields as the need comes.


# 3)Home Automation system
The main objective is to recive data from a local webserver using a ESP8266 wifi module and use a PIC to control the speed of the fan.
We would also use a buzzer to indicate as to when the speed is being changed. In addition the project has also introduced automatic speed control using temperature sensor.
## Componenets
+ ESP8266-01 Wifi Module - 1
+ PIC12F675 Microcontroller - 1
+ DHT11 Temperature and Humidity Sensor - 1
+ MB10S Bridge Rectifier  - 1
+ PC817 Optocoupler - 1
+ BT136 Triac - 1
+ MOC3021 Triac Driver - 1
+ HLK-PM03 Hi-Link - 3.3V - 1
+ MMBT2222A Transistor - 1
+ Buzzer 12mm - 1
+ 10uF Capacitor - 1
+ 1K Resistor - 1
+ 47R Resistor - 2
+ 470R Resistor - 1
+ 102pF,2KV Capacitor - 1
+ 10K Resistor - 1
+ 100K Resistor - 2

## Description
We will be using 2 microcontrollers so as to not overburden.The ESP8266 will be used to host a local webserver , control the buzzer, obtain temperature via DHT11 Temperature and Humidity Sensor and mainly generate a PWM for the PIC.
The PIC will be used to control the Triac circuit which would then control the speed of the fan.Also an intrupt circuit has been introduced with the help of bridge rectifier so as to reduce the noise and smoothly change the speed.

## Circuit Diagram

![image](https://user-images.githubusercontent.com/94821815/174350387-da290960-9e00-4632-b8d0-34e163f6297b.png)

# 4)Raspberry Pi Twitter Bot to post Jokes
The main objective is to use twython library and Twitter api's to automate a bot(using Raspberry Pi) to tweet, which could later on the programmed to post pictures, jokes, polls,etc.

## Componenets
+ Raspberry Pi
+ Micro SD Card
+ Power Supply
+ Wifi or similar connection

## Description
We will be using twython library and twitter's apis to create a bot that 'lives' in a Raspberry pi.
For this first we would need a twitter account, followed by which we would need to create an app on ''https://developer.twitter.com/en/app/new''.This would provide us access_tokens and keys which would be used for api calls.
The rest part is simple coding in python and using different libraries. For instance using pygame library of python for posting images.

# 5)Self Driving Car using Arduino
The objective of this project is to model a self driving car capable of object detection using Ultrasonic sensors.Ultrasonic sensors works on the principle of reflection of sound waves. By calculating the time taken for emmitted wave to reflect back, we can know the distane of the object.

## Componenets

+ Arduino
+ Breadboard
+ Motor Driver
+ Ultrasonic Sensors
+ 9v Battery
+ On-off switch
+ 100uF capacitors
+ 0.1uF capacitors
+ Car Chasis
+ Gear Motor
+ Car Chassis
+ Car Tire
+ 360° Wheel
+Remote control+IR receiver

## Description
We would used 3 Ultrasonic sensors to detect the distance of the obstacle.Depending on the proximity we will use the motor driver to control the motors to go left, right or backward.We will use the IR receiver to on and off the model.

## Circuit Diagram
![image](https://user-images.githubusercontent.com/94821815/174439481-94af93fc-23c7-4d45-b412-50799bba9381.png)

## Working 
![Project 6](https://user-images.githubusercontent.com/94821815/174439647-06b8ab3d-b528-4ef6-ae35-a4496de45274.gif)

## Improvements
+ As it is the model randomly chooses paths. I would like to provide it a map of entire room so as to make it choose shortest path.
+ The model wont be able to detect stairs or holes, making it venerable to them.
