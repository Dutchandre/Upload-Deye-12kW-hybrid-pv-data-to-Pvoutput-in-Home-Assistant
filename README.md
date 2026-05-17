# Upload-Deye-12kW-hybrid-pv-data-to-Pvoutput-in-Home-Assistant
Upload pv data using Solarman, Home Assistant, Solarman stick integration and RESTful command that appears in your integrations list.

This method assumes that Pvoutput is configured to receive the data and that Solarman is working with the Deye inverter in Home Assistant.
For Pvoutput to receive more then 1 string and extended data (dc volt and power) you need a payed subscription (donation).
The Rest command in HA uploads the data, it needs to know your Pvoutput id's and api.
In this case the secrets file in the HA directory is used to store your Pvoutput api key and system id.
The payload items represent the fields in Pvoutput that receive data of each pv string, here 2 strings are provided.
Look for similar sensor naming in your Solarman integration, it may differ a bit from mine.

An automation in HA triggers the rest command each 5 minutes, if you like you can add sun rise and sun down items.
