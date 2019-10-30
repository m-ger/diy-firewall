# diy-firewall
This Project describes how to set up an own firewall within your home network and also add dns and dhcp and free yourself from your mostly remote controlled ISP hardware.

## Concept

## Target audience
Basic Pi and Linux knowledge.

## Requirements
These are soft requirements. You will need these parts but you could also use other hardware or software but the instructions may change.  
Every point will also have a short explaination why i would recommend this resource over another.

### Hardware Requirements:

* 1 "Orange Pi R1" http://www.orangepi.org/OrangePiR1/
* 1 Power Supply for the Orange Pi
* 1 SD Card for the Orange Pi
* 1 Additional Ethernet Cable

### Software Requirements:

* Armbian ISO Image https://www.armbian.com/orange-pi-r1/
* A way to flash the image to the sdcard
* Firewall Builder (in latest Version)
* SSH Client
* (optional) bind9
* (optional) isc-hdcp-server
* (optional) openvpn


### Rationale / Consideration of alternatives
There is a whole universe of Pis, OSs and software. Therefore I'd like to point out why i think this is the best solution and what you should keep in mind for your own project.  

#### Orange Pi
The Orange Pi fits perfectly the casual home use. It is small so you can place it easily near your ISP hardware. It is cheap to get and supports two 100mbit ethernet ports. So if you have a 100mbit ISP contract like it works fine.
And here comes the big drawback, if you have more than 100mbit, you might want to get another device.

#### Armbian ISO Image
Debian based with good support and really well working OS.
Clear drawback but a risk you take with any Pi. If the OS is not supported anylonger, you might have an update problem.


## Basic Setup

### Install Armbian on the SDCard

### Configure the Pi

### Install the Pi

### Install the Firewall Builder

### 


## Firewall Setup

## DNS

## DHCP

## VPN
