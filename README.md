# DISCLAIMER
> ⚠️ This project is not being actively maintained. It is just a PoC to show that the new authentication method of Hisense TVs can be implemented in Home Assistant. Use at your own risk. ⚠️

# Hisense TV Integration for Home Assistant

Integration of a Hisense TV as media player into Home Assistant. The communication is handled via the integrated MQTT broker and wake-on-LAN.
Requires Home Assistant >= `2021.12.x`.

## Current features:
* Turn on / off

## Setup in Home Assistant

[![Add this repository to HACS.](https://my.home-assistant.io/badges/hacs_repository.svg)](https://my.home-assistant.io/redirect/hacs_repository/?owner=PeterBurner&repository=ha_hisense_tv&category=integration)
1. Download and install the integration via [HACS](https://www.hacs.xyz/).
2. Restart Home Assistant.
3. Add the [client certificate](https://github.com/nikagl/hisense/issues/4#issuecomment-2441630703) to your Home Assistant config folder.
4. Go to `Settings` -> `Devices & Services` -> `Add Integration`. Search for `Hisense TV` and add the integration.

> [!NOTE]
> During the first setup your TV should be turned on. The integration requires a PIN code from you TV. The PIN will be triggered automatically during setup. This is a onetime step where the client `HomeAssistant` is requesting access to remote control the TV.

# Compatibility

Tested on a `Hisense 65U8KQ` with firmware version `V0000.09.09O.P0930`.
Calling `http://ip:18400/MediaServer/rendererdevicedesc.xml` shows `transport_protocol=3290`.

# Acknowledgment
This repository is a fork of @nikagl's [ha_hisense_tv](https://github.com/nikagl/ha_hisense_tv) which in turn is also a fork of the original @sehaas [ha_hisense_tv](https://github.com/sehaas/ha_hisense_tv). My own contribution boils down to replacing a password salt. So all props to them!

## Related Projects

* [Original ha_hisense_tv](https://github.com/sehaas/ha_hisense_tv) by @sehaas
* [Hisense TV MQTT guide](https://github.com/Krazy998/mqtt-hisensetv) by @Krazy998
* [ha_hisense_tv with new authentication method](https://github.com/nikagl/ha_hisense_tv) by @nikagl
* [Python script with new authentication method](https://github.com/nikagl/hisense) by @nikagl
* [ha_hisense_tv with latest features](https://github.com/sven-probst/ha_hisense_tv) by @sven-probst
* [ha_hisense_tv predecessor](https://github.com/newAM/hisensetv_hass) by @newAM

## Related Discussions

* https://github.com/Krazy998/mqtt-hisensetv/issues/14
* https://github.com/nikagl/hisense/issues/4
* https://github.com/nikagl/hisense/issues/14
* [HA Community](https://community.home-assistant.io/t/hisense-tv-control/97638/1)

## Other

* [Client certificate for newer Hisense TVs / firmwares](https://github.com/nikagl/hisense/issues/4#issuecomment-2441630703) by @nikagl
* [Client certificate for older Hisense TVs / firmwares](https://github.com/d3nd3/Hisense-mqtt-keyfiles) by @d3nd3
* [VIDAA Smart TV app](https://play.google.com/store/apps/details?id=com.universal.remote.multi) by Hisense
