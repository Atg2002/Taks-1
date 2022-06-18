# Pipelines for Projects
Here we will discuss pipelines for 2 projects , comparing advantages and disadvantages of each module or step.
## Projects:
+ Biometric Attendence system
+ Self Driving Car using Arduino

## 1) Biometric Attendence system
### AIM 
+ Build a webserver to host details of students.
+ Use R305(Optical Fingerprint senor) to register, identify or delete fingerprints.
+ Use RTC module to store entry and exit time.
+ Programme arduino to manage the above tasks and perform required operation when corresponding pushbutton is pressed.

### Pipeline

|Part of Pipeline|Feasibility|Advantages|Disadvantages|
|----------------|:---------|:--------|:------------|
|Micro-controller(ESP8266)| Easy to programme and cheap|Cheap, can be used to control multiple operation and peripherals, comes with built in wifi module and can  access webservers| Limited memory capacity and computation speed, need good understanding of wifi libraries|
|Fingerprint Sensor(R305)|Cheap and readily available|Cheap to develop and use,good image processing,Low power consumption |Less secure and difficulty in capturing images if finger is oily or dirty|
|RTC Module| Easy to use and cheap|cheap, can accurately register time|Requires knowledge of RTClib|
|Webserver-hosting| Tools such as xamp can be used |Anytime anywhere access of data| Need to purchace website domains or use webserver hosts |

### Choosing a Pipeline
We could work on the webserver part. Since it is mostly software it is possible to use google docs to present the data in a read only format, saving costs.

# 2)Self Driving Car using Arduino

### AIM 
We create a car which is self driving and avoids obstacles.We use 3 ultrasonic sensors for proximity detection and motor controllors to control direction of motors.

### Pipeline

|Part of Pipeline|Feasibility|Advantages|Disadvantages|
|----------------|:---------|:--------|:------------|
|Arduino| Easy to programme and cheap|Cheap, can be used to control multiple operation and peripherals| Limited memory capacity and computation speed|
|Motor Driver|Cheap and readily available, easy to use and control upto 2 motors|Relatively simple electronics||
|Ultrasonic Sensors| Easy to use and cheap|cheap, easy to programme and effective for calculating approximate distances |Less effective compared to LIDAR sensors|
|DC Motors| Cheap and readily available |Speed and torque can be controlled with varying voltage levels| Lower liftime due to high contact components, need Motor driver |

### Choosing a Pipeline
We could replace the three Ultrasonic sensors with a LIDAR based sensor. This would increase accuracy but at same time would increase cost.For making the car choose shortest path we could provide it with a map based algorithm which it modifies realtime by mapping against obstacles.

