This is an example sketch for the esp8266 with a PIR motion sensor that sends an MQTT message when motion occurs to the configured MQTT broker.

It is a fork of my basic esp8266 MQTT example sketch.

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


## ESP8266 Boards

Review of [ESP8266 boards](https://openhomeautomation.net/choose-esp8266-module/)

## MQTT Libraries

- PubSubClient.h, [Arduino Client for MQTT](http://pubsubclient.knolleary.net/)
- Adafruit_MQTT.h, [Arduino MQTT Library](https://github.com/adafruit/Adafruit_MQTT_Library)
- MQTTClient.h, [256dpi Library](https://github.com/256dpi/arduino-mqtt) Paho based (limited ESP8266 boards)
