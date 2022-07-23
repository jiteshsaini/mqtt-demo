# MQTT Network - Raspberry Pi & ESP32 Microcontrollers

The code for this project is created to demonstrate data exchange mechanism between Raspberry Pi & ESP32 Microcontrollers using MQTT network. 
In a MQTT network, the communication between devices takes place using a Publish & Subscribe mechanism. Messages can be published on a specific topic by a device. 
The devices that are subscribed to that topic can receive the message. Devices can send and receive data through a MQTT broker.

No sensor is required to be interfaced for this project. 

## The Code

### rpi_mqtt_clients
There two Python scripts in this folder. Both connects the broker as clients with following functionality

#### client_pub.py
khkd

#### client_sub.py
kjkj

### esp32_clients
This folder contains the C code written in Arduino IDE for 02 ESP32 microcontrollers.
The code for both the ESP32 is completely identical. The only difference in the two codes is the name of the client and the topic to which it publishes.

## The Information Flow

The task of Python scripts running in Raspberry Pi and C code running in ESP32 can be summarised by the following diagram

<img src='https://github.com/jiteshsaini/files/blob/main/img/mqtt-network.jpeg'>
