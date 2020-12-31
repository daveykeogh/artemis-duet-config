I purchased a SeeMeCNC Artemis 300 back in December of 2018.

Since then I haven't seen any firmware upgrades come out to support the latest additions to RepRapFirmware.

There are some coming changes (like meta commands) that I'd like to adopt so I decided to port the RRF-2.x gcode configuration to RRF-3.x. Also it's nice to have the latest and greatest firmware to ensure that the printer can keep up with any changes in temperature control or extruder control algorithms.

There are some slight configuration changes which you can see in the diff for config.g and homedelta.g. 

I used the RepRapTool (https://configtool.reprapfirmware.org/Start) to start with, and then diffed the old config and new config to address any issues or missing configuration.

This is an early port and whilst I have tested the changes I haven't done exhaustive testing so your mileage may vary. 