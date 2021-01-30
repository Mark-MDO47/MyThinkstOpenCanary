# Install Ubuntu

## Back to Readme.md
- https://github.com/Mark-MDO47/MyThinkstOpenCanary/blob/main/README.md

## To get the Ubuntu image to load, I went here
- https://ubuntu.com/download/raspberry-pi

The OtherMaker Youtube video about OpenCanary recommends Ubuntu 18.04.5 even though Ubuntu 20.04.1 LTS was available at the time
- https://www.youtube.com/watch?v=RanpEQBvAY0
- At this time Ubuntu Server 20.04.1 LTS is still visible on the Ubuntu download but Ubuntu 18.04.5 is no longer visible
- I downloaded Ubuntu Server 20.04.1 LTS 32-bit since I plan to run it on a Raspberry Pi 2 or 3
- At the time I did the download, the "verify your download" link just went back to the same download page and downloaded the image again

## Then I  went to the link "How to install Ubuntu Server on your Raspberry Pi" and got directions
- https://ubuntu.com/tutorials/how-to-install-ubuntu-on-your-raspberry-pi#1-overview

## First you should choose the SD card and format it. As for size of SD card, it looks like anything under 256GB is OK for Ubuntu on Raspberry Pi 2 or 3; there are limitations for NOOBS. I had a 32Gbyte SD card so I used that; Ubuntu apparently requires 16Gbyte
- https://www.raspberrypi.org/documentation/installation/sd-cards.md
- https://www.raspberrypi.org/documentation/installation/sdxc_formatting.md
## As for size of SD card, it looks like anything under 256GB is OK for Ubuntu on Raspberry Pi 2 or 3; there are limitations for NOOBS
- https://www.raspberrypi.org/documentation/installation/sd-cards.md
- https://www.raspberrypi.org/documentation/installation/sdxc_formatting.md

## To format the card I use the SD Association free formatter on Windows
- https://www.sdcard.org/downloads/formatter/

## To install the image, www.raspberrypi.org talks about a "Raspberry Pi Imager"
- https://www.raspberrypi.org/software/

## ... but I have Windows 10 and Balena Etcher so I chose to use that
- https://www.raspberrypi.org/documentation/installation/installing-images/windows.md

- ... here from https://www.raspberrypi.org/forums/viewtopic.php?t=279692
- - 1 Download image (do not unzip)
- - 2 Insert sd card to be flashed into computer
- - 3 Start Balena Etcher
- - 4 Click 'Flash from file'
- - 5 Select your image
- - 6 Click 'Select target'
- - 7 Select your sd card
- - 8 Click 'Flash'

## First boot and updates
When trying to upgrade I kept getting "waiting for unattended-upgr..." - theoretically it would eventually finish but I like to do this myself
- I did "**sudo systemctl disable unattended-upgrades**"
- Need to wait a couple of minutes for this to completely take effect and release all resources
- Then "**sudo apt-get update**" to update the list of upgrades
- "**sudo apt-get upgrade**" to upgrade Ubuntu
- "**sudo apt-get dist-upgrade**" to install kernel updates on Ubuntu LTS server
- "**sudo reboot**" as needed
