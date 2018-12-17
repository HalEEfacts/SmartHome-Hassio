
This is my Smart Home. It uses Home Assistant to bridge and automate all my home automation products. It runs on a [Raspberry Pi Model B+](https://www.amazon.com/dp/B07BDR5PDW/ref=psdc_1048424_t2_B07BFH96M3) running [Hass.io](https://www.home-assistant.io/hassio/). Related repositories: Arduino for DIY sensors/lights/switches etc,  "NextCloudPi" for the NAS.

# Table of contents
1. [Devices](#devices)
2. [Security](#security)
3. [Automations](#automations)
4. [Screenshots](#screenshots)
5. [Information](#information)
6. [Configuration](#configuration)
    - [Official Add-ons](#official-add-ons)
    - [Third Party Add-ons](#third-party-add-ons)
# Devices
## Cloud Devices

| Device  | Quantity | Connection | Home Assistant | Notes |
| ------------- | :---: | ------------- | ------------- | ------------- |
| [Amazon Echo Dot](https://www.amazon.com/All-New-Amazon-Echo-Dot-Add-Alexa-To-Any-Room/dp/B01DFKC2SO) | 1 | Wifi | https://www.home-assistant.io/components/alexa/ | Used for voice commands to turn devices on/off using the [Emulated Hue Component](https://home-assistant.io/components/emulated_hue/) |
| [Google Mini](https://store.google.com/product/google_home_mini) | 1 | Wi-Fi | [Assistant](https://www.home-assistant.io/components/google_assistant/) | also for voice control, vie build in cloud service or DIY.|

## Wifi Devices
### Outlets
| Device  | Quantity | Connection | Home Assistant | Notes |
| ------------- | :---: | ------------- | ------------- | ------------- |
| Wemo Outlet | 1 | Wifi |       |
| [Sonoff S31](http://a.co/d/dNYEOzi) | 2 | Wifi | mqtt |  not set up yet |
| [Jinvoo Outlets](http://a.co/d/0ra1sZJ) | 2 | Wifi | [Tuya component](https://www.home-assistant.io/components/tuya/) | not set up yet

### Lights
| Device  | Quantity | Connection | Home Assistant | Notes |
| ------------- | :---: | ------------- | ------------- | ------------- |
| [Hue Colored lights](http://amzn.to/2l2viGK) | 2 | wifi/zigbee | Hue | |
| [Ikea TRÅDFRI LED Bulbs](http://www.ikea.com/us/en/catalog/products/20318267/) | 1 | Wifi/zigbee | Hue |
| [Ikea TRÅDFRI Remote](http://www.ikea.com/us/en/catalog/products/20303317/) | 1  Wifi/zigbee | | - add thru Hue via [1](https://redsilico.com/blog/ikea-tradri-remote-with-hue-hub)
### Multimedia
| Device  | Quantity | Connection | Home Assistant | Notes |
| ------------- | :---: | ------------- | ------------- | ------------- |
| IP/Android Cameras | 1 | Wifi | [IP Webcam](https://www.home-assistant.io/components/android_ip_webcam/) | 
| [Amazon Fire 8HD](http://amzn.to/2tqlMCW) | 1 | Wifi | | [FloorPlan Blog post](http://www.vmwareinfo.com/2017/07/visualizing-smart-home-using-home.html)</s> dont have yet, may go with Pi Screen
| [LG WebOS TV] | 1 | LAN | [WebOS](https://www.home-assistant.io/components/media_player.webostv/) |
| [Sonos] | 2 | Wifi | [Sonos](https://www.home-assistant.io/components/sonos/)
### Etc
| Device  | Quantity | Connection | Home Assistant | Notes |
| ------------- | :---: | ------------- | ------------- | ------------- |
| PI Zero | 1 | Wifi | |
| [NodeMCU Development Boards](http://amzn.to/2ou0NON) | 8 | Wifi/mqtt| |  Act as [DIY Motion Sensors](http://www.vmwareinfo.com/2017/11/yet-another-inexpensive-motion-sensor.html). Scenes are activated via IFTTT/HA integration.
| [Pi 2 B](http://amzn.to/B01CD5VC92) | 2 | Wifi | | Runs as home computer (Raspbian, etc) with WebCam (installed via [1](https://blog.kalavala.net/smarthome/camera/), [CUPS](https://www.cups.org/) for Printer connection via MQTT, and NAS

*Technically Zigbee based, but added through Hue they dont require a zigbee hub.

## Hardwired Devices
| Device  | Quantity | Connection | Home Assistant | Notes |
| ------------- | :---: | ------------- | ------------- | ------------- |
| [Philips Hue Hub Gen 2](http://amzn.to/2eoQTJy) | 1 | LAN | Hue |
| [Pi B+](http://amzn.to/B01CD5VC92)__ Hub, See above (Hass.io)
| [Ikea TRÅDFRI Gateway](http://www.ikea.com/us/en/catalog/products/00337813/) | 0 | LAN | | 

#### Outdoor Landscaping
| Device  | Quantity | Connection | Home Assistant | Notes |
| ------------- | :---: | ------------- | ------------- | ------------- |
| [Rachio Sprinkler system](http://amzn.to/2eoPKBW) | 0 | Wifi | | |
| [GE ZWave Outdoor Power Module](http://amzn.to/2q17R4S) | 0 | | |
|[Phyn Smart Water Main ShutOff/Leak Detector](http://www.phyn.com/) | 0 | | |
| [Outdoor LED Lighting](http://www.vmwareinfo.com/2017/08/diy-outdoor-smart-home-led-strips.html) | 0 | | |


#### Outdoor LED Accents
| Device  | Quantity | Connection | Home Assistant | Notes |
| ------------- | :---: | ------------- | ------------- | ------------- |
| [LED RGB Wifi Controller - flux_led compatible](http://amzn.to/2jUBSBE) | 0 | | |
| [LED Strip kits](http://amzn.to/2gJYfZ5) | 0 | | |
| [Aluminum light Diffusers](http://amzn.to/2CIId82) | 0 | | |
| [Outdoor Housing](http://amzn.to/2m2dG0X) | 0 | | |


#### Sensors
| Device  | Quantity | Connection | Home Assistant | Notes |
| ------------- | :---: | ------------- | ------------- | ------------- |
| [Pi Zero](http://amzn.to/2ougZQ3) | 0 | | |
| [Zigbee2mqtt "hub"](https://github.com/Koenkk/zigbee2mqtt) | 0 | | |
| [MX350 Printer]( http://a.co/d/1GxbxER) | 1 | | |
| [Xiaomi motion sensors](1) | 0 | | |
| [Xiaomic Button](2) | 0 | | |

# Security
These are the steps I have taken to add some level of security to my Home Assistant instance.
- Simple protections like enabling a [password](https://github.com/HalEEfacts/SmartHome/blob/master/config/configuration.yaml#L132) and limiting the number of incorrect [login attempts](https://github.com/HalEEfacts/SmartHome/blob/master/config/configuration.yaml#L133).
- Anything that doesn't need an internet connection is blocked from any inbound or outbound traffic at the router level.
- Running [PiVPN](http://www.pivpn.io/) on a spare Raspberry Pi, any external traffic runs through this one port only, needs a cert to access.
- Failed login attempts to the Home Assistant Front end generate a [notification](https://github.com/HalEEfacts/SmartHome/blob/master/config/automations.yaml#L1) to me with the source IP.
- Frontend log-ins are tracked using a [Custom Component](https://github.com/custom-components/sensor.authenticated)
- My Home Assistant Traffic is encrypted with [Let's Encrypt](https://letsencrypt.org/).  I used [this guide](https://www.splitbrain.org/blog/2017-08/10-homeassistant_duckdns_letsencrypt) to get it setup.

# Automations

A detailed description of each of my automations and a link to the yaml file is located [HERE](https://github.com/HalEEfacts/SmartHome/tree/master/config/automations)

Typical Automations in use (or planned to be) include

- Turn on / off outside lights at sunset
- Turn on / off indoor light when door opens / closes
- Turn off lights after no activity / motion
- Grouping of lights for use with Alexa/Google for commands
- Perform actions based on people leaving home / arriving home
- Update location for user based on geolocation zones (Work, School, Church, Home)
- Enable holiday color lights on outside lights via scenes
- Turn on lights based on motion / ring front door and return to previous theme after
- Send Text notification and flash lights if water detected in basement
- Send Text notification and flash lights if water detected by washing machine
- Cut power to washing machine if water detected by washing machine
- Send Text notification and flash lights if CO / Smoke detectors go off
- Send alert if power is lost at the house
- Enhance security system through extra sensors and motion reading

# Screenshots

## Home
![Home](/images/homescreen.png)

## Links
* [HA cheat sheet](/HASS%20Cheatsheet.md) for miscellaneous tips and tricks.
* [YouTube Series](https://www.youtube.com/playlist?list=PLgtGAtCt_hGTc_GAEmMhQ_XVs80mZoBIG). 
* [Home Assistant Docs](https://home-assistant.io/docs/).
* [Home Assistant Forum](https://community.home-assistant.io/) 
* Thanks to [SilvrrGIT](https://github.com/SilvrrGIT/HomeAssistant), most of this page is based on his. Thanks to [mertenats](https://github.com/mertenats/Open-Home-Automation), most of the Arduino pages are based of his.
* [Awesome-HA](https://www.awesome-ha.com/)
* [Lovelace Gallery](https://home-assistant-lovelace-gallery.netlify.com/#)
*

| [![TravisCI](https://travis-ci.org/HalEEfacts/SmartHome.svg?branch=master)](https://travis-ci.org/HalEEfacts/SmartHome) | [![LastCommit](https://img.shields.io/github/last-commit/HalEEfacts/SmartHome.svg?color=blue&style=plasticr)](https://github.com/HalEEfacts/SmartHome/commits/master)|
|:---:|:---:|
| This shows whether the configuration in this repo is valid. [Version I'm running.](/.HA_VERSION) | This shows how up to date this repo is |
| [![GitHub stars](https://img.shields.io/github/stars/HalEEfacts/SmartHome.svg)](https://github.com/HalEEfacts/SmartHome/stargazers) | [![GitHub issues](https://img.shields.io/github/issues/HalEEfacts/SmartHome.svg)](https://github.com/HalEEfacts/SmartHome/issues) |
| Please :star: this repo if you find it useful, like these people have. | This is like my TODO list |
|[![License: Unlicense](https://img.shields.io/badge/license-Unlicense-blue.svg)](http://unlicense.org/)| [![contributions welcome](https://img.shields.io/badge/contributions-welcome-blue.svg?style=flat)](https://github.com/HalEEfacts/SmartHome/pulls) |
| This tells you you can use anything you like from this repo for your project, gratis! | If you have any ideas, they're always welcome.  Either submit an issue or a PR, or drop me a message! |
| [![Uptime Robot status](https://img.shields.io/uptimerobot/status/m780352466-da3a90fa1da0e09f6f0ee745.svg)](https://uptimerobot.com/) | [![Buy Me A Beer](https://img.shields.io/badge/BuyMeABeer-Paypal-blue.svg)](https://paypal.me/HalEEfacts) |
| I use Uptime Robot to monitor my instance from outside in case of crashes - Guide coming soon. | Sometimes people want to buy me a beer when I've been helpful, now it's as easy as clicking the badge! |

# Confguration

<p><font size="3">

This is the main directory of the Repo.  You will find more helpful ReadMe files in the directories as you browse them.  I  use a configuration type called split configuration, so my main configuration.yaml file is broken out into many different files located in the directories. I also use packages to combine related items (media players, their automations etc).</p>
<div align="center"><a name="menu"></a>
  <h4>
    <a href="https://github.com/HalEEfacts/SmartHome#links">
      Links
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome#devices">
      Devices
    </a>
    <span> | </span>
    <a href="https://github.com//HalEEfacts/SmartHome/issues">
      Todo List
    </a>
    <span> | </span>
    <a href="https://twitter.com/BearStoneHA">
      Smart Home Stats
    </a>
    <span> | </span>
    <a href="https://www.facebook.com/BearStoneHA">
      Facebook
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/tree/master/config">
      HASS
    </a>
    <span> | </span>
    <a href="https://github.com//HalEEfacts/SmartHome#diagram">
      Diagram
    </a>
  </h4>
</div>

# Installation Process:
I'm currently running [Home Assistant](https://home-assistant.io) version __0.81__. My preferred installation method is the [HASS.io Method](https://www.home-assistant.io/hassio/). Simply download, and install on SD card via [Etcher](https://etcher.io/).  Install addons: see below.

### Official Add-ons

 I am running the following Hass.io add-ons:

* [DuckDNS](https://www.home-assistant.io/addons/duckdns/) - Updates your Duck DNS IP address and generate SSL using Let's Encrypt.
* [HASS Configurator](https://www.home-assistant.io/addons/configurator/) - Browser-based configuration file editor.
* [Mosquitto](https://www.home-assistant.io/addons/mosquitto/) - Fast and reliable MQTT broker.
* [Samba](https://www.home-assistant.io/addons/samba/) - Access your configuration files using Windows network shares.
* [NGINX SSL proxy](https://www.home-assistant.io/addons/nginx_proxy/) - Reverse proxy with SSL termination.

### Third Party Add-ons

* [SSH & Web Terminal](https://github.com/hassio-addons/addon-ssh) - SSH and Web-based terminal with tons of pre-loaded useful tools, including Git, configure via [this guide](https://www.home-assistant.io/docs/ecosystem/backup/backup_github/).
* [Pi-hole](https://github.com/hassio-addons/addon-pi-hole) - Network-wide ad blocking.
* [UniFi Controller](https://github.com/hassio-addons/addon-unifi) - The UniFi Controller allows you to manage your UniFi network using a web browser.
* [Node-RED](https://github.com/hassio-addons/addon-node-red) - Flow-based programming for the Internet of Things.
* [Plex Media Server](https://github.com/hassio-addons/addon-plex) - Your recorded media beautifully organized and ready to stream.
* [zigbee2mqtt](https://github.com/danielwelch/hassio-zigbee2mqtt) - Zigbee to MQTT bridge, get rid of your proprietary Zigbee bridges.
* [Dropbox Sync](https://github.com/danielwelch/hassio-dropbox-sync) - Upload your backup snapshots to Dropbox.
* [Log Viewer](https://github.com/hassio-addons/addon-log-viewer) - Browser-based live log viewing utility.
* [Tautulli](https://github.com/hassio-addons/addon-tautulli) - Monitor and get statistics from your Plex server.
* [motionEye](https://github.com/hassio-addons/addon-motioneye) - Simple, elegant and feature-rich CCTV/NVR for your cameras.
* [TasmoAdmin](https://github.com/hassio-addons/addon-tasmoadmin -  Easy managment of tasmota flashed devices

# Configuration/Components

[Split up](https://www.home-assistant.io/docs/configuration/splitting_configuration/) into sections, including  [packages](https://www.home-assistant.io/docs/configuration/packages/) for weather/media players, 

* [Weather](https://community.home-assistant.io/t/add-an-active-weather-radar-map/1315/34)
* [GTFS Halifax Transit](https://www.home-assistant.io/components/sensor.gtfs/) https://www.halifax.ca/home/open-data/halifax-transit-open-data
* Google Home https://console.actions.google.com/u/0/, https://www.browserling.com/tools/random-string
##Possible Components for the future
* [Feedreader](https://www.home-assistant.io/components/feedreader)


## Custom Cards
https://github.com/custom-cards

* https://github.com/custom-cards/surveillance-card
* mini media player, thank you https://github.com/JamesMcCarthy79/Home-Assistant-Config/tree/master/config
