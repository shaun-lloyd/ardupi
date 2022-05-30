# ArduPi, Ardupilot + Raspberry Pi

ArduPi is an open hardware/software Raspberry Pi shield with all the components to run ardupilot.

## Thanks

This project stands on the ardupilot & raspberry pi platforms, ardupilot in particular is an outstanding example of open source communities flourishing.

OPAL, Muhammad Hefny. ArduPi has been created using OPAL as a reference and design inspiration.

ArduPi-v0.1 == OPAL


## Development

Kicad-v6.0

Linux is the focus however Kicad is available on windows so there is no reason developement couldn't be done on windows.

As long as anything done on windows is "do-able" on linux then that's cool.


## Problem i'm trying to solve

General "user" complexity of the rc/ardupilot ecosystem.

While the complexity is good from many perspectives especially ardupilot showing support for an ever growning number 
of technologies.

Traditional RC vehicles have been controlled via RF thru opentx "an outstanding contribution to the community".

For FPV also another RF thru some propritary video Tx Rx solution.

Each of these elements have there own firmware, configuration and intergration considerations. While thankfully the RC world is
full of open source technology it is still litered like most domains with non-free proprietary tech.

This leaves the user, in particular the linux user with a world of pain and non-ending issues to deal with. In many cases with
no hope in sight.


## Elements required for Solution
Interestingly all these features exists in the community in various implementations using various technologies.

ArduPi is a distribution of many open source projects much like ubuntu is a linux distribution.

1. Support for "standard" PC/BT/USB controllers.
2. IP-streaming HD-video.
	- For <25ms latency use S-video out on raspberry pi, simple use existing solutions to transmit and recieve this real-real-time
		signal on gear the user all-ready has.
	- Currently webrtc considers real-time to be <200ms, this isn't quite good enough. Open.HD is getting <150ms latency.
	- I believe with the continued work of the community it wouldn't be unresonable to see <100ms in the near future.
	- ArduPi plans to allow for both configurations eg: analog & HD. Best of both worlds.
3. Simple ground station.
	- linux host(s)


## Solution: ArduPi
The Raspberry pi platform requires some additional hardware to be able to control a vehicle.
The RPI handles ardupilot-cpu / comms:control-telemetry-video, and ardupi handles everything else.

This hardware is designed as OPAL reference.


### Hardware Specification

RpiZero2W footprint.
	- PCA9685:pwm
	- ULN2803:led,buzzer
	- ADS1115:current voltage sensor
	- IMU9650:IMU
	- BMP280:Barometer

### Connections
	- +5V@3A input
	- ESC
	- UART
	- I2C
	- SPI
	- Serial
	- PWM:servo/esc
	- RC:Rx
	- Buzzer & Safety Circuit

### Software
TODO

## Future
Please see roadmap.

## How you can help :)

Any and all feedback is encouraged.

Anyone with electronics experience can look over our shematics and crtique or even better suggest better circuits or components.

1. Proof the schematics we have for 0.1.

2. I plan to add ExpressLRS,ADSB,GPS,optical flow,lidar & airspeed sensor. So anyone with expertise and some spare time willing to
share would be really appreciated.

Help documenting and organise schematics such that new users in particular can easily understand and fork.

Suggest better IC's, sensors and features.

One potential future i would love to see is a reference implementation of all supported sensors/cpu/mcu. Allowing
anyone to rapidly develop ardupilot hardware, essentially ArduPi hopes to be that platform.




