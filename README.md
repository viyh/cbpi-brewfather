# Brewfather (brewfather.app) stream plugin for CraftBeerPi3

Use this plugin to send your fermenation temperatures and gravities to Brewfather.

## Installation

Download and Install this Plugin via the CraftBeerPi user interface
or pull into the [craftbeerpi]/modules/plugins/ directory.
Make sure to install the python requests library: `sudo pip install requests`

Set the following parameters in CraftBeerPi3:
* `brewfather_api_key`: The api key from https://web.brewfather.app/tabs/settings
* `brewfather_temp_sensor`: The name of the Temperature sensor for all fermenters being submitted to Brewfather. This is one of "sensor", "sensor2", or "sensor3", and must be consistent on all fermenters. Leave empty if no temperature sensor.
* `brewfather_gravity_sensor`: The name of the Gravity sensor for all fermenters being submitted to Brewfather. This is one of "sensor", "sensor2", or "sensor3", and must be consistent on all fermenters. Leave empty if no gravity sensor.

Additional parameters (default values are fine most of the time):
* `brewfather_api_url`: API URL, default: https://log.brewfather.net/stream
* `brewfather_temp_unit`: Temperature unit of sensor (C or F for Celsius or Fahrenheit) default: C
* `brewfather_gravity_unit`: Gravity unit of sensor (G or P for Gravity or Plato), default: G

## Updates

Temperatures will update every 15 minutes to Brewfather for all fermenters that are set to automatic.

You can view the logs and attach to a brew session under the Fermentation tab in your brew session within Brewfather.
