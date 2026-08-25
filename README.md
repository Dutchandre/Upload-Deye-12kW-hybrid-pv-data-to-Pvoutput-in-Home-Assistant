# Upload-Deye-12kW-hybrid-pv-data-to-Pvoutput
Upload pv data using Solarman, Home Assistant, Solarman stick integration and RESTful command that appears in your integrations list.
The inverter is a Deye SUN-12K-SG04LP3-EU, this method probably will work for other models and brands when Home Assistant logs them.
Aassumed is that Pvoutput is configured to receive the data and that Solarman is working with the Deye inverter in Home Assistant.
For Pvoutput to receive more then 1 string and extended data (dc volt and power) you need a payed subscription (donation).
The Rest command in HA uploads the data, it needs to know your Pvoutput id's and api.
In this case the secrets file in the HA directory is used to store your Pvoutput api key and system id.
The payload items represent the fields in Pvoutput that receive data of each pv string, here 2 strings are provided.
Look for similar sensor naming in your Solarman integration, it may differ a bit from mine.
An automation in HA triggers the rest command each 5 minutes, if you like you can add sun rise and sun down items.

# Pace BMS
To read values of a Pace BMS in Home Assistant I've made an EspHome device using ESP32 with ethernet.
It is based on another desgin with a Lilygo Esp32 that has RS485 on board.
Because it has no usb the intial setup has to be done using an usb-rs232 flash device, after that OTA is available.
I have included some basic code for one-wire devices (DS18B20 temperature) available on IO2.
Use the yaml to flash it with EspHome builder, I assume you know how the secrets file works.

# Pace BMS WT32-TH01 wiring to RS485 module:

<img width="803" height="282" alt="ESP32 WT32-ETH01_RS485_schema" src="https://github.com/user-attachments/assets/6b55af91-17ce-4749-ba48-d72fb1a8917c" />

# Home Assistant CYD for Pace BMS
Another EspHome gadget I've made is a CYD (cheap yellow display) that shows BMS data and other data in Home Assistant.
These modules have usb for the intial flash, there are some cases available or you can print one.

<img width="800" height="1000" alt="IMG_20260628_150631_MP-" src="https://github.com/user-attachments/assets/5ff1bb5c-8b9d-43ca-a91c-6e7e11cee4f4" />
