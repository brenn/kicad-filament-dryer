# Filament dryer

Using an AtMega and old Ender 5 heat plate to make a filament drying box

## Status

# Design 

* Using a Buck converter for 24V-5V conversion
* Using temperature stable LM336, for fun
* Fan inside box runs continously to sirculate air
* Exhaust fan runs briefly every 10th minute to get rid of humidity
* Thermistor in heater is 100k
  * Thermistor value drops pretty fast above 25 degrees
  * I want accuracy when bed temp > 80 degrees
  * To improve accuracy in temperature range of interest a 47k resistor is used in the divider
* Thermistor is a simple glass rod type of 10k@25 degrees
    * I want accuracy when box temp is 50-80 degrees
    * Using a 4.7k resistor in divider (instead of 10k)
* Using small Pololu LCD in 4-bit mode, scrapped from old bots
* 



