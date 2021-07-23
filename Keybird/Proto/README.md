# Prototype v. 1.0 Description
Prior to the handover of the developement of electronics for Keybird, two student from DTU had made an attempt to develop a prototype. This prototype did not function as desired and the further development was therefore handed over to the authors of this GitHub repository.

The prototype is based on the [CNY70 Infrared sensor](https://www.vishay.com/optical-sensors/list/product-83751/), the [CD74HC4067M analog MUX](https://www.digikey.dk/product-detail/da/texas-instruments/CD74HC4067M/296-9225-5-ND/376870) and the [Arduino MKR WiFi 1010](https://store.arduino.cc/arduino-mkr-wifi-1010).

The reasoning for the faulty functionalities of the v. 1.0 prototype is as follows:
* Noise in sensor signals.
  * Traces for logic level anolog signal are not properly designed and are prone to noise because of their length and placement.
* Inproper choice of components.
  * All interpretation of sensor signal is done by ADC on the microcontroller.
  * Analog MUXs is used inorder to increase to number of ADC channels, which can introduce both latency and noise.
  * The chosen microcontroller does not have a capable clocks speed in order to do ADC for 69 individual keys. 

A complete redesign was therefore necessary as the prior design did have a sufficient groundwork. All files from the prior project can be found in this subfolder.
