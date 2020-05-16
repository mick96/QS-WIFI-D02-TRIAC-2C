# QS-WIFI-D02-TRIAC-2C
Conversion of QS-WIFI-D02-TRIA-2C Tuya based dimmer to Tasmota fw.
The device is MOSFET based not TRIAC as stated by device name.

## Install TASMOTA
Flashing of ESP8266 (LM1) can be done through [Tuya-Convert](https://tasmota.github.io/docs/Tuya-OTA), but future update could fix it. It is always possible to flash it via serial.

**REMEMBER** to flash a Tasmota build with script enabled.

If for some reason the device bricks you need to solder serial interface directly on the board. In doing it remember to disable the two STM mcu chip connecting to GND the EN pins.
## Set-Up Tasmota
### TEMPLATE:
`{"NAME":"QS-WIFI-D02","GPIO":[255,148,255,149,38,43,255,255,37,42,255,255,255],"FLAG":0,"BASE":1}`

### Console:
- Enable Multi-channel PWM (to make the color channel a second brightness channel)
`SetOption68 1`
- Update of Dimmer/Color/CT without turning power on (decouple Channel<x> and Power<x>):
`SetOption20 1`
 
 ### Script:
 Copy and paste the [Dimmer-QS-WiFi-D02-Script.txt](https://github.com/mick96/QS-WIFI-D02-TRIAC-2C/blob/master/Dimmer-QS-WiFi-D02-Script.txt)
 
