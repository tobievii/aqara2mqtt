# aqara2mqtt

[![mqtt-smarthome](https://img.shields.io/badge/mqtt-smarthome-blue.svg)](https://github.com/mqtt-smarthome/mqtt-smarthome)
[![NPM version](https://badge.fury.io/js/aqara2mqtt.svg)](http://badge.fury.io/js/aqara2mqtt)
[![Dependency Status](https://img.shields.io/gemnasium/hobbyquaker/aqara2mqtt.svg?maxAge=2592000)](https://gemnasium.com/github.com/hobbyquaker/aqara2mqtt)
[![Build Status](https://travis-ci.org/hobbyquaker/aqara2mqtt.svg?branch=master)](https://travis-ci.org/hobbyquaker/aqara2mqtt)
[![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg)](https://github.com/sindresorhus/xo)
[![License][mit-badge]][mit-url]

> Attach an [Aqara](https://www.aqara.com/en/products.html) Smart Hub to MQTT

### Install

`$ sudo npm install -g aqara2mqtt`


### Usage 

```
Usage: aqara2mqtt [options]

Options:
  -v, --verbosity  possible values: "error", "warn", "info", "debug"
                                                               [default: "info"]
  -n, --name       instance name. used as topic prefix        [default: "aqara"]
  -k, --insecure   allow ssl connections without valid certificate     [boolean]
  -u, --url        mqtt broker url (may contain user/password)
                                                   [default: "mqtt://127.0.0.1"]
  -p, --password   gateway password
  -d, --devices    json file with sid to name mappings
  -h, --help       Show help                                           [boolean]
  --version        Show version number                                 [boolean]
```

See [Domoticz Wiki](https://www.domoticz.com/wiki/Xiaomi_Gateway_(Aqara)#Adding_the_Xiaomi_Gateway_to_Domoticz) on how 
to enable local network access to the Gateway.


### Supported Devices

All Switches, all Sensors (Cube, Weather, Vibration, Motion, Leak, Door/Window) and the Gateway itself. As of today you 
_can't_ control plugs, the air condition controller and the curtain actuator.


### Topics subscribed by aqara2mqtt

* aqara/set/gateway/bri `0` - `100`
* aqara/set/gateway/rgb `#rrggbb` e.g. `#0099FF`
* aqara/set/gateway/volume `0` - `100`
* aqara/set/gateway/sound 
  * `0` - Police car 1
  * `1` - Police car 2
  * `2` - Accident
  * `3` - Countdown
  * `4` - Ghost
  * `5` - Sniper rifle
  * `6` - Battle
  * `7` - Air raid
  * `8` - Bark
  * `10` - Doorbell
  * `11` - Knock at a door
  * `12` - Amuse
  * `13` - Alarm clock
  * `20` - MiMix
  * `21` - Enthusiastic
  * `22` - GuitarClassic
  * `23` - IceWorldPiano
  * `24` - LeisureTime
  * `25` - ChildHood
  * `26` - MorningStreamLiet
  * `27` - MusicBox
  * `28` - Orange
  * `29` - Thinker


## License

MIT © [Sebastian Raff](https://github.com/hobbyquaker)

[mit-badge]: https://img.shields.io/badge/License-MIT-blue.svg?style=flat
[mit-url]: LICENSE
