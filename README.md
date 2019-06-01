# Under construction

# My Smart Home
In 2017 I still lived at home, and I had a small electric heating to heat my room on cold winter days. When I went to my room in the evening, it was always way too cold. So I turned my electric heating on. But then while being too busy on my computer, I noticed that my analogue thermometer suddenly reached 25°C. So the time has come to being too busy on my computer with all comfort.

My first home assistant setup was born: a Raspberry Pi with a DHT22 temperature sensor plugged in, and a ESP8266 based Sonoff smart socket flashed with firmware of ![Tasmota](https://github.com/arendst/Sonoff-Tasmota). Since then I kept adding features to my setup. From a wake up alarm via my old school stereo, to my bedroom lights and fan, to voice control with google home.

Now I live on a small appartment with my girlfriend, and I have some sort of mission to eliminate all repetitve tasks that could easily be automated. For example the central heating is coupled to my alarmclock which is set by voice with google home. And when I open the door when coming home from work, my stereo and lights will be turned on. In this document I will give an overview how everything is coupled, which hardware is used and how I made my home smart with automations.

## Overview
Nowadays there are a lot of brands which bring out their own smart home platform with their own hardware, software and cloud. One brand can't take it all, and managing a bunch of different apps to control your home isn't working either. So there is Home Assistant to integrate them all in one highly customizable platform .

My home assistant setup is split over an Intel Core i5 Mini-ITX build which runs Ubuntu and a Raspberry Pi 3 which runs [HassOS](https://github.com/home-assistant/hassos). My RPI handles the Z-Wave communication via Z-Wave Gateway from [Aeotec](https://aeotec.com/z-wave-usb-stick), and Bluetooth communication which is built-in. All the data from the wireless sensors is pushed via MQTT to my Ubuntu server. In this setup my RPI which has a slow reboot rarely has to be restarted, and my Z-Wave network stays alive. My server is quite overpowered and has an high enough clock rate to trigger my automations in a blink and minimizes down time during development restart cycles.

The following schematic shows high level architecture of my smart home.

![My Home Automation Setup](https://raw.githubusercontent.com/steinmaerivoet/home-assistant-config/master/Documentation/Topology/homeassistant_topology.png)

## Hardware
### Processing Power
<table>
<tr>
    <td>
    <a href="http://amzn.to/2pTWaNm"><img src="https://raw.githubusercontent.com/skalavala/skalavala.github.io/master/images/lifx-bulb.jpg" alt="Lifx Light Bulb" /></a><br/>
        Lifx Light Bulb
    </td>
    <td>
    <a href="http://amzn.to/2DI7i4P"><img src="https://raw.githubusercontent.com/skalavala/skalavala.github.io/master/images/lifx-led-strip.jpg" alt="Lifx LED Strip" /></a><br/>
        Lifx LED Strip
    </td>
    <td>
    <a href="http://amzn.to/2DLfuBi"><img src="https://raw.githubusercontent.com/skalavala/skalavala.github.io/master/images/philips-hue-bulbs.jpg" alt="Philips Hue Bulbs" /></a><br/>
        Philips Hue Bulbs
    </td>
    <td>
    <a href="http://amzn.to/2mH7bi8"><img src="https://raw.githubusercontent.com/skalavala/skalavala.github.io/master/images/philips-hue-hub.jpg" alt="Philips Hue Hub & Bulbs" /></a><br/>
        Philips Hue Hub & Bulbs
    </td>
</tr>
<tr>
    <td>
    <a href="http://amzn.to/2qeilPx"><img src="https://raw.githubusercontent.com/skalavala/skalavala.github.io/master/images/tplink-smart-switches.jpg" alt="TP-Link Smart Switches" /></a><br/>
        TP-Link Smart Switches
    </td>
    <td>
    <a href="http://amzn.to/2pairYc"><img src="https://raw.githubusercontent.com/skalavala/skalavala.github.io/master/images/wemo-light-switches.jpg" alt="Wemo Switches" /></a><br/>
        Wemo Switches
    </td>
    <td>
    <a href="http://amzn.to/2DK11G5"><img src="https://raw.githubusercontent.com/skalavala/skalavala.github.io/master/images/wall-mote.jpg" alt="ZWave Wallmotes" /></a><br/>
        ZWave Wallmotes
    </td>
    <td><img src="https://raw.githubusercontent.com/skalavala/skalavala.github.io/master/images/blank.jpg"/><br/>&nbsp;</td>
</tr>
</table>


### Zwave Sensors

### Heating
Nest (explain with Junkers)

### Control
tablet, Smartphones, aeotec multisensor
The puprpose is to use this as minimal as possible. Everything should go automatic.


### Multimedia
Sonos Beam, Sony Bravia, Google Home, Broadlink


## Automations
House mode and different sub topics
