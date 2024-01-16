# vmagent for Home Assistant

Home Assistant addon that uses `vmagent` to scrape Home Assistant Prometheus metrics and writes them to remote storage systems via Prometheus `remote_write` protocol or via VictoriaMetrics `remote_write` protocol.

## Installation and Configuration

### Install the add-on

If you are reading this in the documentation tab of the add-on - you have already completed this step. 

Otherwise:

* Add the reposity. (Quick link: [![Open your Home Assistant instance and show the Supervisor add-on store.](https://my.home-assistant.io/badges/supervisor_store.svg)](https://my.home-assistant.io/redirect/supervisor_store/) )
    * Add the reposity (click 3 dots on the top right of the screen). Repository URL: *https://github.com/jbub/hass-addons*
    * Refresh/reload your browser tab/window
* Install the add-on:
    * Find, and **install** the vmagent Add-on

### Steps to get everything running

Once the add-on is installed:

* Read the add-on documentation
* Enable the Home Assistant Prometheus integration https://www.home-assistant.io/integrations/prometheus/
* Generate a Long-Lived Access Tokens in your Home Assistant profile and set it up as `longelivedToken`
* Configure your remote write target using `remoteWriteUrl`, `remoteWriteUsername` and `remoteWritePassword`
* Configure your `homeassistantUrl` to your local Home Assistant url (http://homeassistant.local:8123)
* Start the addon

## Data Storage

vmagent temp data (`tmpDataPath`) is stored in folder `/share/vmagent-data` of Home Assistant OS.
