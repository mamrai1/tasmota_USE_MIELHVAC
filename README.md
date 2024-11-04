tasmota 4M binary (development 14.3.04) with miel hvac driver and sample configuration for home assistant...

https://github.com/arendst/Tasmota/commit/56243ef720275790a85478d72b05c4b50f32520b
New features for MiElHVAC (#22423)
* Add prohibit function for MiElHVAC

Add Prohibit functions:
* Power
* Temperature
* Mode
 and all combinations of this functions
Updated VaneV names for better identify

* Fixed Compressor and Operation for MiElHVAC

Changed Widevane position name from ISEE to AUTO sam as in MELCLoud

* Revert "Fixed Compressor and Operation for MiElHVAC"

This reverts commit f0973c8.

* New feature for MiElHVAC

* Added Compressor map
* Added Operation Power in Watts
* Added Operation Energy in kWh
* Changed Widevane position name from ISEE to AUTO, displays sam as in
* Changed all map value to lover case MELCloud

* New feature for MiElHVAC

* Add device operation time in minutes

* New feature Outdoor Temperature for MiElHVAC

* Add Outdoor Temperature

* New feature Compressor Frequency for MiElHVAC

* Added Outdoor Temperature
* Renamed internal properties due typo operating and oprating to operation

* New feature Auto Clear Remote Temp for MiElHVAC

* This PR add auto clear remote temperature function
* This funcion is call on first run and after 10 sec the remote temperature stop refresh its value
* Send manually Clear command is also available

* change function name, small corrections

* added auto clear time configurable using cmnd

* Improvements to remote temp, auto clear time for MiElHVAC

* Added min = 1000ms and max 600000ms limit to remotetemp auto clear time function
* Changed function name to use sam format as other
* Added RemoteTemperatureSensor to the sensor

* more improvements to auto clear time

* Changed RemoteTemperatureSensor to RemoteTemperatureSensorState
* Added RemoteTemperatureSensorAutoClearTime to the sensor output

* New feature Timers for MiElHVAC

* Added Timers to the sensor output:
  * TimerMode - none, on, off, on_and_off
  * TimerOn - display time to ON
  * TimerOnRemaining - display remaining time to ON
  * TimerOff - display time to OFF
    * TimerOffRemaining - display remaining time to OFF

* New feature for Stage and more for MiElHVAC

* Added to sensor output:
  * Added PrerunStage - on/off, report compressor prepare stage before start working
  * FanStage - off, quiet, 1, 2, 3 ,4 ,5, report current fan stage
  * ModeStage - manual(heat, dry, cool, fan_only, heat_isee, dry_isee, cool_isee), auto_fan, auto_heat, auto_cool, report current mode
  * Renamed Bytes to Settings for raw data

* Renamed const UPDATE to SETTINGS
* Moved SETTINGS const from miel_hvac_msg_settings to miel_hvac_data_settings
* Renamed some functions name to get better code readable

* Removed some empty lines
* Refactor some structure of code to make more clean and better readable

* remove duplicate settings request

* New features for MiElHVAC

* Changed PrerunStage to OperationStage
* Updated map for OperationStage
* Updated map for ModeStage
* Changed map fan_only to fan
* Cleanup
