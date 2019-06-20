# Under construction

# My Smart Home
## Overview
Nowadays there are a lot of brands which bring out their own smart home platform with their own hardware, software and cloud. One brand can't take it all, and managing a bunch of different apps to control your home isn't working either. So there is Home Assistant to integrate them all in one highly customizable platform .

My home assistant setup is split over an Intel Core i5 Mini-ITX build which runs Ubuntu and a Raspberry Pi 3 which runs [HassOS](https://github.com/home-assistant/hassos). My RPI handles the Z-Wave communication via Z-Wave Gateway from [Aeotec](https://aeotec.com/z-wave-usb-stick), and Bluetooth communication which is built-in. All the data from the wireless sensors is pushed via MQTT to my Ubuntu server. In this setup my RPI which has a slow reboot rarely has to be restarted, and my Z-Wave network stays alive. My server is quite overpowered and has an high enough clock rate to trigger my automations in a blink and minimizes down time during development restart cycles.

The following schematic shows high level architecture of my smart home.

![My Home Automation Setup](https://raw.githubusercontent.com/steinmaerivoet/home-assistant-config/master/Documentation/Topology/homeassistant_topology.png)
