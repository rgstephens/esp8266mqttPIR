This is an example sketch for the esp8266 with a PIR motion sensor that sends an MQTT message when motion occurs to the configured MQTT broker.

It is a fork of my basic esp8266 MQTT example sketch.

## Hardware

For this project I'm using a NodeMCU esp8266 board. The [HiLetgo](https://www.amazon.com/gp/product/B010O1G1ES/ref=oh_aui_detailpage_o00_s00?ie=UTF8&psc=1) board. There's a good pinout diagram for the ESP8266 [here](http://www.kloppenborg.net/blog/microcontrollers/2016/08/02/getting-started-with-the-esp8266)

I'm using the [HC-SR501](http://henrysbench.capnfatz.com/henrys-bench/arduino-sensors-and-input/arduino-hc-sr501-motion-sensor-tutorial/)  

## Settings in Header

Variable|Use
---|---
ssid | WiFi SSID
password | WiFi Password
MQTT_SERVER | MQTT server IP address or name
MQTT_PORT | MQTT server port
MQTT_TOPICBASE | String pre-pended to the topic of all MQTT messages
delayMS | default main loop delay in milleseconds
ipInterval | default number of intervals between sending IP address, zero to never send

## MQTT Configurable Parameters

The following parameters can be configured via MQTT.

Topic|Use
---|---
esp8266/config/delay | main loop delay in milleseconds
esp8266/config/ipinterval | number of intervals between sending IP address, zero to never send

## Wiring photo

![Photo of Wiring](https://github.com/rgstephens/esp8266mqttPIR/pirWiring.jpg)