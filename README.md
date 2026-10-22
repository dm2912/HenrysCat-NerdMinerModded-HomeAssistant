# HenrysCat-NerdMinerModded-HomeAssistant
Home assistant rest scraping and panels for Henry'sCat modified Nerdminer API https://github.com/HenrysCat/NerdMiner-Modded/

<img width="1552" height="708" alt="Screenshot_20261020_162129" src="https://github.com/user-attachments/assets/4e31c30e-8c3e-47b3-a261-f3e5441f2f62" />

Preparation
------------

+ enable a subdirectory for yaml if not already enabled by adding the contents of configuration-example.yaml to your configuration.yaml in the existing homeassistant section

+ Create a subdirectory /packages, if not already created in your home assistant configuration directory

Fetching from the API
----------------------

+ Using packages/miner_51.yaml as your template create one yaml file for each miner you wish to monitor. In the example file I have used Miner_51 as that miner is on IP 192.168.1.51, ensure you name your files according to your preference, and replace every single instance of miner_51 with your chosen identity for that miner. 

+ repeat the process for each miner you wish to monitor

+ then place all miner files in the /packages directory

Checking for firmware updates
-----------------------------

+ Edit /packages/update-check.yaml with your own miner details. Again, this is set to scrape for my "miner_51" so change that, and add any further entries for other miners both in the "rest" section and the "template" section

+ Add this file to your /packages directory in home assistant

Code verification
------------------

+ In home assistant go to settings > tools and check configuration to look for any yaml errors

+ If all passes, restart home assistant

Dashboard Panel
---------------

+ dashboard_card.yaml contains a basic setup for a panel monitoring online status, hashrate and checking for available firmware updates

Home Assistant notification
---------------------------

+ Use firmware_notification.yaml to create a custom automation to notify you in HA of firmware updates
