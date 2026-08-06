# Filament dryer

Using an AtMega and old Ender 5 heat plate to make a filament drying box

## Status / TODO

* Gjør ferdig fan deteksjons-krets, signal fra pnp må ti mosfet driver på et hvis

* Discussed with AI regarding 4-pin FAN control and stall detection using diodes, resistor and PNP transistor
https://chatgpt.com/share/6a73b5c4-4dc8-83eb-8aa8-39055729d19b
  * CONCLUSION: Use a buck converter for 24V->13.2v  instead of biased BD139 arrangement to feed the diodes/resistor current detection circuit
  * Cannot use MIC4680-5BM,  AI suggested MCP16331 which is cheap and looks nice
* Can also use the old MC34063 which i have plenty of
  * https://chatgpt.com/share/6a73c253-b44c-83eb-a0b3-313f6cf0aaa1

* Also, discussed with AI on how to implement ADC driven FAN PWM on atmega8
  * https://chatgpt.com/share/6a73b632-64b8-83eb-b409-dc50dc401a8e

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



