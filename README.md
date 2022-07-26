# MQTT Network for data Exchange - Raspberry Pi & ESP32 Microcontrollers

<p align="left">
Read the :- <a href='https://helloworld.co.in/article/mqtt-raspberry-pi-esp32' target='_blank'>
   complete article here.
</a> 
Watch Video :- <a href='https://youtu.be/ebsXSCKsHeQ' target='_blank'>
   on Youtube.
</a> 


</p>

The code for this project is created to demonstrate data exchange mechanism between Raspberry Pi & ESP32 Microcontrollers using MQTT network. 
In a MQTT network, the communication between devices takes place using a Publish & Subscribe mechanism. Messages can be published on a specific topic by a device. 
The devices that are subscribed to that topic can receive the message. Devices can send and receive data through a MQTT broker.

No sensor is required to be interfaced for this project. 

## The Code

### rpi_mqtt_clients (Raspberry Pi code)
There two Python scripts in this folder. Both connects the broker as clients with following functionality

#### client_pub.py
This file publishes a simple counter value on a topic 'rpi/braodcast' every 02 seconds. This topic is subscribed by all other clients on the network.

#### client_sub.py
This file subscribe to all the 03 topics (one as mentioned above and other two topics are used by ESP32 to publish thier data). The data received by other clients is printed on the terminal.

### esp32_clients (ESP 32 code)
This folder contains the C code written in Arduino IDE for 02 ESP32 microcontrollers.
The code for both the ESP32 is completely identical. The only difference in the two codes is the name of the client and the topic to which it publishes.
Both the ESPs do the publish & subscribe simultneously. One ESP publishes to the topic 'esp/sensor1' and the other publishes to 'esp/sensor2'. 
They both subscribe to 'rpi/broadcast' and receive data from this topic.

## The Information Flow

The task of Python scripts running in Raspberry Pi and C code running in ESP32 can be summarised by the following diagram

<img src='https://github.com/jiteshsaini/files/blob/main/img/mqtt-network.jpeg'>

You can replicate this demo code on your devices and understand the MQTT communication. Later you can modify it for practical use by interfacing sensors and actuators as per your requirement.
