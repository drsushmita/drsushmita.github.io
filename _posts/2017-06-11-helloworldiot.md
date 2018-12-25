---
bg: "p3.png"
layout: post
title:  "Immuno-Localization"
crawlertitle: ""
summary: ""
date:   2017-11-28 20:09:47 +0700
categories: posts
tags: ['.Net', 'IOT', 'Azure']
author: Mohan Kodali
---
This is a quick intro to IOT. We will talk about basics of IoT, the individual components and various applications of IoT. Let’s first try to understand what IoT is by definition. It’s an inter-network of things and thing can be a person, a pet, a car, a cell phone, a Blood Glucose monitoring device or any other natural or manmade object that can connect to a network and exchange data.

By definition it is very clear that the concept of IoT is not something new and it’s been there for a while. It is getting that needed attention because of improvement in various fields (but not limited to).

- The Communication technology
- Internet Protocol Version 6
- The wide coverage of cellular networks
- The Emergence of Cloud and cost of data storage
- World understanding the power of data and analytics.
- The concept of open source hardware i.e. Arduino, Raspberry PI, etc.
- Tremendous growth of Smart Phones and their usage. 
- Great Communities and startups.

[![IOT Components]({{ site.images }}/iot1/1.png)]({{ site.images }}/iot1/1.png)

To understand the concept, let’s look at the components of IoT. This is how I think the components can be broadly classified in to. We will go deep in to individual components as we go on.
## Nodes
Nodes are the basic components of IoT that comprises of sensors / actuators, low power signal processing units like microcontrollers, power supplies, and storage and low power transceivers for communications. These nodes are the primary source of data. Based on the application and need few nodes will have built-in processing power to execute steps based on the data that they collect, other just pass the information to the Gateway and receive instructions from it. The best example for a node is Nest Thermostat. Is a powerful node though. It has algorithms built in to interpret data from the following sensors and take actions. Nest is a node and can also be considered as a gateway (built-in) for all the sensors mentioned below.
[![IOT Components]({{ site.images }}/iot1/2.png)]({{ site.images }}/iot1/2.png)
##### Sensors
- Temperature
- Humidity
- Near-field activity
- Far-field activity
- Ambient light

## Gateways
Gateways are considered to be very important components of IoT. The main purpose of the Gateway is to interpret / collect sensor data based on the communication protocol of the sensors and translate the data to an understandable format before sending it to the cloud. Let’s try to understand Gateways by an example.
[![IOT Components]({{ site.images }}/iot1/3.jpg)]({{ site.images }}/iot1/3.jpg)
Let’s say there are bunch of sensors in your room like temperature sensor, humidity sensor, smoke detector, door lock senor and proximity sensor. As listed below let’s say each sensor uses different protocol to connect 
- Bluetooth
- Ethernet
- Serial / USB
- MQTT
- ZigBee
With all these different protocols and considering the fact that these are low power sensors it is not possible to directly connect to the backend systems or the cloud. In some scenarios based on the data from these sensors we might have to control something else and it will become very difficult to do that as they use different protocols. This is a simple use case, but in real time there may be hundreds / thousands of nodes and it gets very difficult to manage.

There are very other important reasons apart from just Protocol translation and data interpretation (but not limited to).
- Only passing meaningful data to the backend
- Security
- Device Management (Updating the sensors firmware)
- Control Systems logic closer to sensors

## Services & Data Stores
Services are nothing but web services and API that will be used by the gateways to send data to cloud. Depending on the domain these services can trigger multiple actions. Considering the volume of data that these devices send, usually we use NoSQL / Big data databases. Once we have the data we can do all sort of analytics that will provide us with meaningful insights.


