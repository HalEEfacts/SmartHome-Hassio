# Automations

<div align="center">
  <h4>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/blob/master/config/automations#TTS">
      TTS
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/blob/master/config/automations#Pushbullet">
      Pushbullet
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/blob/master/config/automations#Visual">
      Visual
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/blob/master/config/automations#Lights">
      Lights
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/blob/master/config/automations#Doorbell">
      Doorbell
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/blob/master/config/automations#Media">
      Media
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/blob/master/config/automations#Sonos">
      Sonos
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/blob/master/config/automations#Occupancy">
      Occupancy
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/blob/master/config/automations#Sleep">
      Sleep
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/blob/master/config/automations#System">
      System
    </a>
    <span> | </span>
    <a href="https://github.com/HalEEfacts/SmartHome/blob/master/config/automations#VacationClimate">
      Vacation/Climate
    </a>
  </h4>
</div>

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

### <a name="TTS"></a>Notification Audio ([TTS](https://home-assistant.io/components/tts.google/))
* TTS "Welcome home _User_" notification over all Sonos speakers.
* TTS notification when _User_ arrives at specific [Zones](https://home-assistant.io/components/zone/).
* TTS notification when _User_ leaves specific zones which includes travel time home.
* TTS test notification

### <a name="Pushbullet"></a>Notification Text ([Pushbullet](https://home-assistant.io/components/notify.pushbullet/))
*  Pushbullet notification when new Home Assistant version is available on PyPI.
* [Notify Me if a Critical Device is offline ](https://github.com/HalEEfacts/SmartHome/blob/master/automation/deviceoffline.yaml)
* Pushbullet notification test.
* Pushbullet when SSL certificate expiration sensor <= 10 days.
* Pushbullet when any battery sensor falls below 20%
* Pushbullet for a failed login attempt.
* Pushbullet if new network device is detected.

### <a name="Visual"></a>Notification Visual
* [LG WebOS TV Notification](https://home-assistant.io/components/notify.webostv/) when [Ring Pro Doorbell](https://www.amazon.com/gp/product/B01DM6BDA4/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01DM6BDA4&linkCode=as2&tag=ntalekt0c-20&linkId=5faec88af320aeb157fbb45fa954efc3) detects motion or is pressed.
* Google Home Hub Notification when...
* Lighting (flash/color) notification when...

### <a name="Lights"></a>Lights
* Exterior lights ([GE Z-Wave Plus Dimmer 14294](https://www.amazon.com/gp/product/B01MUCZA1C/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01MUCZA1C&linkCode=as2&tag=ntalekt0c-20&linkId=0dfbcad4a9df3b81570623f0e23b562a)) on 5 minutes before sunset.
* Exterior lights ([GE Z-Wave Plus Dimmer 14294](https://www.amazon.com/gp/product/B01MUCZA1C/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01MUCZA1C&linkCode=as2&tag=ntalekt0c-20&linkId=0dfbcad4a9df3b81570623f0e23b562a)) off 30 minutes after sunrise.
* Exterior lights ([GE Z-Wave Plus Dimmer 14294](https://www.amazon.com/gp/product/B01MUCZA1C/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01MUCZA1C&linkCode=as2&tag=ntalekt0c-20&linkId=0dfbcad4a9df3b81570623f0e23b562a)) dim to 35% at 9:00pm
* Interior Media Center lights ([Yeelight WIFI RGB Strip](https://www.amazon.com/gp/product/B01LRT0B56/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01LRT0B56&linkCode=as2&tag=ntalekt0c-20&linkId=34a9570cd0c747f448092913ac2dae60)) using [Amazon Echo Dot](https://www.amazon.com/gp/product/B01DFKC2SO/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01DFKC2SO&linkCode=as2&tag=ntalekt0c-20&linkId=bb902528d5689ae4e1163dd31b7c646d) via [Emulated Hue Bridge](https://home-assistant.io/components/emulated_hue/).
* Interior loft lights ([Hue White Bulb](https://www.amazon.com/gp/product/B073SSK6P8/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B073SSK6P8&linkCode=as2&tag=ntalekt0c-20&linkId=97fe4a915d8f531a8ce6697ee55f056c)) using [Amazon Echo Dot](https://www.amazon.com/gp/product/B01DFKC2SO/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01DFKC2SO&linkCode=as2&tag=ntalekt0c-20&linkId=bb902528d5689ae4e1163dd31b7c646d) via [Emulated Hue Bridge](https://home-assistant.io/components/emulated_hue/).
* Holiday interior lighting leveraging [Google Calendar Event](https://home-assistant.io/components/calendar.google/) to define the holiday.
* Holiday interior lighting using [Amazon Echo Dot](https://www.amazon.com/gp/product/B01DFKC2SO/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01DFKC2SO&linkCode=as2&tag=ntalekt0c-20&linkId=bb902528d5689ae4e1163dd31b7c646d) via [Emulated Hue Bridge](https://home-assistant.io/components/emulated_hue/).


### <a name="Doorbell"></a>Doorbell
* Exterior lights to 100% if [Ring Pro Doorbell](https://www.amazon.com/gp/product/B01DM6BDA4/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01DM6BDA4&linkCode=as2&tag=ntalekt0c-20&linkId=5faec88af320aeb157fbb45fa954efc3) detects motion or is pressed after 9:00pm.
* Exterior lights back to 35% after 30 minutes after doorbell motion or press.

### <a name="Media"></a>Media
* Start [Harmony Hub](https://www.amazon.com/gp/product/B00BQ5RYI4/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B00BQ5RYI4&linkCode=as2&tag=ntalekt0c-20&linkId=ef1edfe63776ff2e3b5b4e7fdf8e3488) activity if user selects from HA UI `input_select`.
* Update `input_select` status if physical [Harmony Hub](https://www.amazon.com/gp/product/B00BQ5RYI4/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B00BQ5RYI4&linkCode=as2&tag=ntalekt0c-20&linkId=ef1edfe63776ff2e3b5b4e7fdf8e3488) remote is used to start activity.
* Start playing music on [Sonos PLAY:1](https://www.amazon.com/gp/product/B00EWCUK1Q/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B00EWCUK1Q&linkCode=as2&tag=ntalekt0c-20&linkId=b90ba9470832833ea363027daabf948a) speakers if user selects music station from `input_select`.
* Start playing music on [Sonos PLAY:1](https://www.amazon.com/gp/product/B00EWCUK1Q/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B00EWCUK1Q&linkCode=as2&tag=ntalekt0c-20&linkId=b90ba9470832833ea363027daabf948a) speakers if user starts music station using [Amazon Echo Dot](https://www.amazon.com/gp/product/B01DFKC2SO/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01DFKC2SO&linkCode=as2&tag=ntalekt0c-20&linkId=bb902528d5689ae4e1163dd31b7c646d) via [Emulated Hue Bridge](https://home-assistant.io/components/emulated_hue/).
* Start [Harmony Hub](https://www.amazon.com/gp/product/B00BQ5RYI4/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B00BQ5RYI4&linkCode=as2&tag=ntalekt0c-20&linkId=ef1edfe63776ff2e3b5b4e7fdf8e3488) activity using [Amazon Echo Dot](https://www.amazon.com/gp/product/B01DFKC2SO/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01DFKC2SO&linkCode=as2&tag=ntalekt0c-20&linkId=bb902528d5689ae4e1163dd31b7c646d) via [Emulated Hue Bridge](https://home-assistant.io/components/emulated_hue/).
* Power off [Harmony Hub](https://www.amazon.com/gp/product/B00BQ5RYI4/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B00BQ5RYI4&linkCode=as2&tag=ntalekt0c-20&linkId=ef1edfe63776ff2e3b5b4e7fdf8e3488) activity using [Amazon Echo Dot](https://www.amazon.com/gp/product/B01DFKC2SO/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01DFKC2SO&linkCode=as2&tag=ntalekt0c-20&linkId=bb902528d5689ae4e1163dd31b7c646d) via [Emulated Hue Bridge](https://home-assistant.io/components/emulated_hue/).
* Turn on SleepTime mode if [Xiaomi Aqara Smart Wireless Switch](https://www.gearbest.com/access-control/pp_626695.html) is pressed.
* Pause [Deluge](https://home-assistant.io/components/switch.deluge/) if internet data usage > 90%.

### <a name="Sonos"></a>Sonos
* Reset/Regroup all [Sonos PLAY:1](https://www.amazon.com/gp/product/B00EWCUK1Q/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B00EWCUK1Q&linkCode=as2&tag=ntalekt0c-20&linkId=b90ba9470832833ea363027daabf948a) speakers at 6:00am every morning.
* Group all Sonos' button.

### <a name="Occupancy"></a>Occupancy
* If motion is detected via [BRUH Automation multisensor](https://github.com/bruhautomation/ESP-MQTT-JSON-Multisensor) or [Amcrest  cameras](https://www.amazon.com/gp/product/B077DPWQCV/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B077DPWQCV&linkCode=as2&tag=ntalekt0c-20&linkId=ac62ed590e7bb7ab3e4aca12348c1db1) turn on `input_boolean` (used in `binary_sensor` for occupancy tracking).
* If no motion is detected after certain period of time turn off `input_boolean`.

### <a name="Sleep"></a>Sleep time
* Turn off master TV after 30 minutes via [Harmony Hub](https://www.amazon.com/gp/product/B00BQ5RYI4/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B00BQ5RYI4&linkCode=as2&tag=ntalekt0c-20&linkId=ef1edfe63776ff2e3b5b4e7fdf8e3488).

### <a name="System"></a>System
* Run script to collect Internet usage hourly.
* Clean the TTS cache weekly.
* Nightly (3AM) [snapshot](https://github.com/HalEEfacts/SmartHome/blob/master/config/automations.yaml#L8).

### <a name="VacationClimate"></a>Vacation/Climate
* Turn vacation mode on when household is gone for 24 hours.
* Toggle office fan on/off based on occupancy using * [Wemo Insight Smart Plug](https://www.amazon.com/gp/product/B01DBXNYCS/ref=as_li_tl?ie=UTF8&camp=1789&creative=9325&creativeASIN=B01DBXNYCS&linkCode=as2&tag=ntalekt0c-20&linkId=934f0720129cf096876ab8b14a26bbbb).


<details>
  <summary>Ability to ask Alexa to repeat the last Voice notification - 'Alexa, Turn on Last message'.</summary><p align="center">
  <a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/packages/triggers/last_message.yaml>
  Last Message Package - /config/packages/triggers/last_message.yaml</a><br>
<p></details>

[NMAP](https://github.com/CCOSTAN/Home-AssistantConfig/tree/master/config/device_tracker) for presence detection.
<details>
<summary>IOS Notifications for Offline Devices, BadLogins, HA Startups, new HA versions and IP Changes for DNS.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/System/ip_change.yaml>
External IP changes - /config/automation/System/ip_change.yaml</a><br>
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/packages/network.yaml>
Network Monitor package - /config/packages/network.yaml</a><br>
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/away.yaml>
Away triggers -/config/automation/away.yaml</a><br>
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/script/interior_off.yaml>
Shut interior script -/config/script/interior_off.yaml</a><br>
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/late_night_helper.yaml>
Late night Helper Automation -/config/automation/late_night_helper.yaml</a><br>
</details>
<details>
<summary>Reminders to take my medicine sent as IOS notifications ONLY when I arrive back home for the night.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/packages/ios.yaml>
IOS Package - /config/packages/ios.yaml</a><br>
</details>
<p><br>
The Tablets are for the awesome FloorPlan that you see in the images.  We have 2 in the house mounted for quick consumption of all the HA data in a glance.  We also leverage them as TTS endpoints.  During certain times of the day, TTS is only played on the tablets rather than over the whole house.  Other times, Notifications are sent only to the Mobile Devices rather than using speech.</p>
<details>
<summary>Custom Component Fire Tablet Media Player</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/tree/master/config/custom_components/media_player>
Kiosk TTS Custom component - /config/custom_components/media_player</a><br>
</details>

<details>
<summary>Using [Etekcity Outlets](http://amzn.to/2efNoBP) to control accent lighting above kitchen cabinets and room cutouts.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/kitchen_lights_and_accents.yaml>
Kitchen Accents Automation - /config/automation/kitchen_lights_and_accents.yaml</a><br>
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/master_bath_accents.yaml>
Master Bath Accents Automation - /config/automation/master_bath_accents.yaml</a><br>
</details><details>
<summary>Turn on Hallway light for no more than 20 minutes when Pantry door is opened.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/zwave_hallway_door_sensor.yaml>
Hallway Automation - /config/automation/zwave_hallway_door_sensor.yaml</a><br>
</details><details>
<summary>Detects when lights are turned on and adjusts them to correct brightness based on time of day.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/System/detect_and_adjust_lights.yaml>
Auto Light adjustment Automation - /config/automation/System/detect_and_adjust_lights.yaml</a><br>
</details>
<br>

Still buying, looking for inexpensive white A19s.  Even Ikea has great lights now.  Colored lights are in the front sconces and also used in the living room.  The Go lights are specifically for the kids since they are both wireless and also have a button on them making them very tactile for kids.  I use the Lightstrips for TV backlighting and also couch accent lighting.
<details>
<summary>Turn on TV Time Lights (dim and color) at Sunset (if home and TV is on)</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/tv_time_on_and_off.yaml>
TV Time Automations - /config/automation/tv_time_on_and_off.yaml</a><br>
</details><details>
<summary>Sets up the front lights in the house with preset colors depending on the ~~month~~ day!.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/packages/holiday.yaml>
Holiday Lights package - /config/packages/holiday.yaml</a><br>
</details><details>
<summary>Turns living room lights `red` when a Window or Door is opened past sunset.  Resets to `yellow/gold` when all doors/windows are closed.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/packages/alarm.yaml#L289-L299>
DIY Alarm package - /config/packages/alarm.yaml</a><br>
</details>

<details>
<summary>Shut down HVAC system if a Window or Door is left open for more than 5 minutes.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/packages/alarm.yaml#L209>
HVAC Watchdog Automation - /config/packages/alarm.yaml#L209</a><br>
</details><details>
<summary>Play chime on all window and door open/closes.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/System/door_chime.yaml>
Door Chime Automation - /config/automation/System/door_chime.yaml</a><br>
</details>
<details>
<summary>Change Aura scenes based on presence and sleep.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/packages/aurahome.yaml>
Aura Package - /config/packages/aurahome.yaml</a><br>
</details>

<details>
<summary>On motion from Doorbell turns front lights to Bright White lights for 10 minutes and then back to original colors.  Fake Dog barking when there is motion by the house.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/script/skybell_pressed.yaml>
Skybell HD script - /config/script/skybell_pressed.yaml</a><br>
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/guard_dog.yaml>
Dog Bark script - /config/automation/guard_dog.yaml</a><br>
</details>
<details>
<summary>When someone rings the Doorbell, the backyard and Bathroom lights Flash - Since we might not hear the doorbell. Fake Dog barks as well (which can be snoozed for 30 minutes via Alexa).</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/script/skybell_pressed.yaml>
Skybell HD script - /config/script/skybell_pressed.yaml</a><br>
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/guard_dog.yaml>
Dog Bark script - /config/automation/guard_dog.yaml</a><br>
</details>

The great outdoors can be automated too!  Mainly lights but also the sprinkler system and water supply.  The Phyn leak detector was announced in CES.  It looks for abnormal flows and if senses them, alerts me and shuts water main.  The GE Outlets are hooked up to my 12v transformers allowing me to turn the landscaping lights on and off.  The LED strips are DIY and the recipe is in the next section.
<details>
<summary>(IFTTT) Add a 1 day rain delay to Rachio Sprinkler system if it is going to rain tomorrow also logged to MQTT.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/System/rachio_rain_delay.yaml>
Rain Delay Package - /config/automation/System/rachio_rain_delay.yaml</a><br>
</details>
<details>
<summary>(IFTTT) Blink ALL lights if Winds get to 70MPH - Hurricane warning.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/flash_all.yaml>
Flash Light automation - /config/automation/flash_all.yaml</a><br>
</details>
<details>
<summary>Turn on some outdoor Lights at Sunset, Turn off 4 hours before sunrise.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/Timed_Triggers/sunset_turn_on.yaml>
Sunset automation - /config/automation/Timed_Triggers/sunset_turn_on.yaml</a><br>
</details>
<details>
<summary>Turn off interior and backyardlights when we go to sleep.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/good_night.yaml>
Good Night automation - /config/automation/good_night.yaml</a><br>
</details>

<details>
<summary>Change the front colors of the LED lights based on holidays.  The best part is the LED controller works with HA right out of the box.  No fiddling around with it at all.  HUGE Plus in my book.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/packages/holiday.yaml>
Holiday Package - /config/packages/holiday.yaml</a><br>
</details>
<details>
<summary>When the garage doors open, change all lights in the front of the house to bright white.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/garadget.yaml>
Garadget automations - /master/config/automation/garadget.yaml</a><br>
</details>
<details>
<summary>On motion, turn all the lights to a bright white outside for a random amount of time before resuming the daily color choice.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/script/front_house_motion.yaml>
Motion automations - /config/script/front_house_motion.yaml</a><br>
</details>

<details>
<summary>If any Doors or Windows are open, the TV backlights turn Red.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/packages/alarm.yaml>
Alarm package - /config/packages/alarm.yaml</a><br>
</details>
<details>
<summary>When the Roku reports we are watching Plex or TabloTV, TV Time scene is triggered dimming 2 of 4 living room lights.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/tv_time_on_and_off.yaml>
TV Time Automations - /config/automation/tv_time_on_and_off.yaml</a><br>
</details>
<details>
<summary>Rainy days trigger extra subtle light (TV back lights and other accent lighting) inside the house.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/dark_rainy_day.yaml>
Rainy Day Automations - /config/automation/dark_rainy_day.yaml</a><br>
</details>

Sensors add data to Home Assistant.  Most of my Doors and windows are hardwired but for some interior doors, I also have the wireless sensors.  They connect to my Wink Hub.  [PiHole](https://pi-hole.net/) is running on my PiZero.  It's super easy to install and runs DNS, DHCP and ad blocking for the whole house on a great little 5v form factor.

<details>
<summary>Tweet out daily Pi Hole stats. (Ads Blocked and % of bandwidth saved.)</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/packages/pihole.yaml>
Pi-Hole Package - /config/packages/pihole.yaml</a><br>
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/script/tweet.yaml>
Tweet script - /config/script/tweet.yaml</a><br>
</details>
<details>
<summary>Leverage Alexa and Elekcity outlet to control Printer On/Off via Voice. Turns off automatically after 20 minutes.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/System/watchdog_light.yaml>
Light watchdog Automations - /config/automation/System/watchdog_light.yaml</a><br>
</details>
<details>
<summary>Sound door chimes whenever doors open or close.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/automation/System/door_chime.yaml>
Door Chimes Automations - /config/automation/System/door_chime.yaml</a><br>
</details>
<details>
<summary>Watch and alert on Home Assistant's Disk usage and Pi Zero.</summary><p align="center">
<a href=https://github.com/CCOSTAN/Home-AssistantConfig/blob/master/config/packages/processmonitor.yaml>
Process Monitor Package - /config/packages/processmonitor.yaml</a><br>
</details>
