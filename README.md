# MQTT-SERVER

First, install Telegram on PI

- for OS update - sudo app update
- To install Telegram, I install snap first by - sudo apt install snapd
- Then install telegram by - sudo snap install telegram-desktop
- Then I changed wifi to have a static IP of 192.168.1.130 by referring from https://www.tomshardware.com/how-to/static-ip-raspberry-pi
- Note: I put 'request 192.168.1.130' instead of assinging with static IP address.
- The name server IP was 172.26.1.1

- Then I installed node red and mqtt on my raspberry pi by referring to https://www.makeuseof.com/install-mqtt-server-node-red-raspberry-pi-home-automation/
- To ssh into my raspberry pi, I had to give SSH permission in the Raspberry PI's Perferrence

To auto start Node-Red (https://nodered.org/docs/getting-started/raspberrypi)

- sudo systemctl enable nodered.service
- sudo systemctl disable nodered.service

![image](https://user-images.githubusercontent.com/16104631/201664807-cf14e56d-4e08-4aef-8d28-63dc83d4e1cb.png)

Setting for MQTT Broker; I has to copy MQTT ID from Tasmota Info.

![image](https://user-images.githubusercontent.com/16104631/202504108-1c066da7-9491-4b56-a9c5-46282d4e6646.png)


- to reboot Raspberry Pi 'sudo reboot'

To connect Tasmota to NodeRed : https://flows.nodered.org/node/node-red-contrib-tasmota
To connect to Telegram : https://flows.nodered.org/node/node-red-contrib-telegrambot

For NodeRed flow, I refer to: https://discourse.nodered.org/t/turn-flow-on-off-via-iphone/8395/16
