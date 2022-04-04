# Simumatik IoT Coffee Machine

## Description

This is a Node-RED project intended to remotely control via MQTT a coffee machine simulated by Simumatik platform. 

## Prerequisities

Nodes used in this project and required to be installed: 
- node-red-dashboard
- node-red-contrib-ui-led-fork
- node-red-contrib-ui-media

## Installation

1. Import flows.json to Node-RED.
2. Upload the logo inside the node named as "simumatik logo", at the end of the flows. 
3. (Optional) Interface apparence is designed for dark style theme. Set the dark style in dashboard/theme menu. 

## Introduction to software/hardware used

Programming of the functions and the interface is done by using the Node-RED platform. Communication with the IoT Coffee Machine is made through the public MQTT broker service “test.mosquitto.org”. Because of its public type, in order to prevent any possible MQTT-topic conflict relating to this challenge, I have changed the default topic prefix to the new one “coffee_mac_iot_lab_2022/”. 
This Node-RED project can be loaded locally or in any cloud instance. In my [example](https://evisvasiu.com/ui/#!/3?socketid=pUpuodymT3KdQSsNAAIW), I have loaded Node-RED in a cloud virtual machine, by using the Oracle Cloud service.

### Interface

By using the provided inbuilt MQTT topics, I have built an interface (fig.1) with a total of nine inputs and five commands. 
List of the commands are as follows: 
-	Two manual “Coffee” and “Milk” buttons. Pouring coffee or milk happens if any of the buttons is pressed once and it stops pouring when the relevant button is pressed again. 
-	Three recipes of coffee, double-coffee and macchiato.  Recipes consist on the pre-programmed quantities of coffee and milk. 
List of the feedbacks are as follows: 
-	LED lamp. It turns green when the connection is successfully and it turns red when there is no connection
-	Each button background color. Each button background turns red when the command is received successfully by the machine. 

 
![Fig. 1. Cloud interface of the machine](/ui-media/interface.jpeg)

-	Text display. There are several text feedback which provide main informations about the machine status. Text messages feedbacks are: “Ready”, “Pouring coffee”, “Pouring milk” and “Enjoy”.
-	Milk and coffee quantities left on the tank. 


