I purchased a SeeMeCNC Artemis 300 back in December of 2018.

Since then I haven't seen any firmware upgrades come out to support the latest additions to RepRapFirmware.

There are some coming changes (like meta commands) that I'd like to adopt so I decided to port the RRF-2.x gcode configuration to RRF-3.x. Also it's nice to have the latest and greatest firmware to ensure that the printer can keep up with any changes in temperature control or extruder control algorithms.

There are some slight configuration changes which you can see in the diff for config.g and homedelta.g.

I used the RepRapTool (https://configtool.reprapfirmware.org/Start) to start with, and then diffed the old config and new config to address any issues or missing configuration.

This is an early port and whilst I have tested the changes I haven't done exhaustive testing so your mileage may vary.

# January 2021 Update

In order to quieten up the printer some what whilst it's idle I decided to replace the standard case fan with
a Noctua case fan from amazon:

https://www.amazon.com/Noctua-NF-R8-redux-1800-PWM-Performance/dp/B00KF7MVI2

The standard case fan is connected to the duet in an always on configuration.
I used a 4 pin PWM controlled fan, and connected the PWM output of the fan2 header
to the PWM input of the fan.

I set the fan up in thermostatic mode so that when the hotend was heating the fan would heat up. Unless I'm
calibrating the printer, the rest of the time the fan will spin when the hotend is moving and warm.
I do plan on setting up either another thermistor, or tweak the config to use the MCU temp, but this
setup is conservative and will function just fine for now. 
