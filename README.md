# diy-firewall
This Project describes how to set up an own firewall within your home network and also add dns and dhcp and free yourself from your mostly remote controlled ISP hardware.

## Concept

!(https://github.com/m-ger/diy-firewall/blob/master/Concept.png)

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
* Firewall Builder http://fwbuilder.sourceforge.net/
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

### Download Armbian
Armbian is typically available for two diffrent linux distributions. Debiand and Ubuntu.  
Use the Debian image. For the actual Release Buster here is the link:
#### Downloadlink: https://dl.armbian.com/orangepi-r1/Debian_buster_next.7z

### Install Armbian on the SDCard
I'd highly recommend EtcherIO because this software worked so great in the past and is available for many operation systems.
But in fact you can use any way or software which flashes you an iso to a bootable sdcard.

#### Downloadlink: https://www.balena.io/etcher/

Flash the Image to your sdcard and then put it into the Pi.

### Configure the Pi

#### Connect to Network
* Connect the Pi with an ethernet cable to your ISP router or a local switch.
* Boot the Pi.
* Now the Pi will try to allocate an IP adress given by the DHCP service on your ISP router.
* Since you can't connect a monitor to your Pi because there is no HDMI port, you have to find out which IP was given to the Pi. This can be really easy or really tricky depending on the ISP router. Normally the ISP router of any kind should have a webinterface where you can see connected devices. TODO: other ways.

#### Connect to Pi via SSH client
* Now open up a SSH connection to the IP of your Pi.
* Linux and Mac have already pre installed ssh clients, for window you will need to use putty.
* Check below for OS specific connections. 
* After you have succeffully connected to your Pi, login with the predefined user "root" and password "1234"
* First of all change these credentials with "passwd". Now you will be asked to enter a new password.

##### Windows
* Download Putty https://www.chiark.greenend.org.uk/~sgtatham/putty/
* Install Putty
* Enter the IP of the Pi in the edit field for "Host Name (or IP address)" and click "Open"

##### Linux
* Open a terminal
* Enter: ssh {IP of the Pi} 

#### Configure Network
At the moment your Pi has an IP from the ISP router. This IP is also variable.



### Install the Pi in your network
Now you need to setup the Pi between your internal network and the router/modem of your ISP.
Therefore you unplug the ethernet cable from your ISP router and connect it to you Pi and then take a new ethernet cable and connect this with the spare ethernet port on the Pi and the ISP router where the ethernet cable where plugged before.







### 


## Firewall Setup

### Install Firewall Builder


## DNS

### Install bind9 as dns service

### Configure

## DHCP

### Install isc-hdcp-server

### Configure


## VPN

### Install OpenVPN

### Configure Client
