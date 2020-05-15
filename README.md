# QS-WIFI-D02-TRIA-2C
Conversion of QS-WIFI-D02-TRIA-2C Tuya based dimmer to Tasmota fw

## Install TASMOTA
Flashing of ESP8266 (LM1) can be done through [Tuya-Convert](https://tasmota.github.io/docs/Tuya-OTA), but future update could fix it. It is always possible to flash it via serial.
WARNING: flash Tasmota with script enabled

## Set-Up Tasmota
The following parameters must be set on Tasmota through console:
- Enable Multi-channel PWM (to make the color channel a second brightness channel)
`SetOption68 1`
- Update of Dimmer/Color/CT without turning power on (decouple Channel<x> and Power<x>):
`SetOption20 1`
 
