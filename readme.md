# ArduPi, Ardupilot + Raspberry Pi

ArduPi is an Raspberry Pi hat with sensors and drivers to run ardupilot.

Based entirely on work and with the guidance and lead of [Muhammad Hefny, OBAL](https://github.com/HefnySco/OBAL "Muhammad Hefny, OBAL").

## Thanks

This project stands on the ardupilot & raspberry pi platforms, ardupilot in particular is an outstanding example of open source communities flourishing.

[OBAL, Mohammad Hefny](https://github.com/HefnySco/OBAL "OBAL, Mohammad Hefny"). ArduPi has been created using [OBAL](https://github.com/HefnySco/OBAL "OBAL") as a reference and design inspiration.

ArduPi-v0.1 == OBAL

## Development

Everything in the entire toolchain must be free software. No dependancy on any non-free software is acceptable. With exception of ardupilot:matlab. "I would really love to hear from anyone that can suggest or give advise on how to or the process involved in porting the current control theory to a free software platform, potential financial support is available to any project that can resonable accomplish this task".

The board itself is developed using Kicad v6.0 on both ubuntu and windows.

Linux is the focus however Kicad is available on mac & windows so there is no reason developement couldn't be done any OS and indeed is. As long as anything done on windows is "do-able" on linux then that's cool.


## Solution: ArduPi
The Raspberry pi platform requires some additional hardware to be able to control a vehicle.
The RPI handles ardupilot-cpu / comms:control-telemetry-video, and ardupi handles everything else.

This hardware is designed using OBAL reference.


### Hardware Specification

Raspberry Pi 4b hat.

### IC
- ULN2803:led,buzzer
- ADS1115:current voltage sensor
- IMU9650:IMU
- BMP280:Barometer

### Module
- GPS:ublox module
- ExpressLRS

### Connections
- ?6S 25V input. Bypass circuit for driving motors and BEC with ?5v@6a
- +5V@3A input
- PWM:pca9685
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

## How you can help :)

Any and all feedback is encouraged.

Anyone with electronics experience can look over our shematics and crtique or even better suggest better circuits or components.

1. QA our schematics/pcb layout.

2. I would like to include ADSB,optical flow,lidar & airspeed sensor. So anyone with expertise and some spare time willing to
share would be really appreciated.

Help documenting and organise schematics such that new users in particular can easily understand and fork.

Suggest better IC's, sensors and features.

Thanks.
