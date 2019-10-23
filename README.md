If you like this project, or you wants to support the development, you can send me a Shelly device, that is not already supported, but you wish. :)

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/I3I514LLW)

# ShellyMQTT - Domoticz Python Plugin
Python plugin for Shelly relay devices using MQTT protocol

MQTT parts based on heavily on the [zigbee2mqtt] project (https://github.com/stas-demydiuk/domoticz-zigbee2mqtt-plugin) 
big thanks for it!

## Prerequisites

Tested and works with Domoticz v4.x.

If you do not have a working Python >=3.5 installation, please install it first! ( https://www.domoticz.com/wiki/Using_Python_plugins )

Setup and run MQTT broker and an MQTT capable Shelly device. (http://shelly-api-docs.shelly.cloud/#mqtt-support-beta)

## Installation

1. Clone repository into your domoticz plugins folder
```
cd domoticz/plugins
git clone https://github.com/enesbcs/Shelly_MQTT.git
```
2. Restart domoticz
3. Go to "Hardware" page and add new item with type "ShellyMQTT"
4. Set your MQTT server address and port to plugin settings
5. Remember to allow new devices discovery in Domoticz settings

Once plugin receive any MQTT message from Shelly it will try to create appropriate device.

## Plugin update

Warning: if you use this method, Domoticz may duplicate devices after it! Download only plugin.py if you have a lot of shellies and do not want to risk it!

1. Stop domoticz
2. Go to plugin folder and pull new version
```
cd domoticz/plugins/Shelly_MQTT
git pull
```
3. Start domoticz

## Supported devices

Tested and working with:
 - Shelly 1 Open Source (relay)
 - Shelly 1PM (relay)*
 - Shelly Plug (relay)*
 - Shelly Plug S (relay)*
 - Shelly2 Switch (relay and roller shutter mode, positioning)
 - Shelly4 Pro (relay)*
 - Shelly H&T
 - Shelly RGBW2
 - Shelly Flood

*Power consumption can be enabled in the plugin settings page manually, it's an optional feature without any further support

**I would like to thank [Allterco Robotics](https://allterco.com/en/Shelly) for providing me with samples of Shelly Plug/Shelly2/Shelly4/Shelly RGBW2 to support the development of this plugin.**
