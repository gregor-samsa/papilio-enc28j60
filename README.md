papilio-enc28j60
================

![Papilio One with Enc28j60](https://raw.github.com/gregor-samsa/papilio-enc28j60/master/img/1.jpg "Papilio One with an Enc28j60") 

SPI Ethernet on the Papilio

This is a quick howto to get started using the enc28j60 SPI based ethernet board with the Papilio One 500k.


## Hardware

* Papilio One 500k 
* Olimex ENC28J60-H dev board

## Set Up
* Install the Papilio [ZAP IDE](http://papilio.cc/index.php?n=Papilio.ZAPIDE)
* Load [hacky fork of jcw's EtherCard](https://github.com/gregor-samsa/ethercard) library for Arduino (this fork contains changes to map pins to SPI)
  * make sure to save this repo as '(Arduino)/libraries/EtherCard'
* Open 'BackSoon' sketch
  * Edit the ip address and gateway address (check your config with IPCONFIG on windows)
* Connect the pins (see enc28j60.h) -

| Enc28j60      | Papilio       |
| ------------- |:-------------:|
| SCK - 1       | WAL0          |
| MOSI - 2      | WAL1          |
| MISO - 3      | WAL2          |
| CS - 7        | WA8           |
| GND - 9       | GND           |
| 3.3v - 10     | 3.3v          |

* Load the sketch and connect the serial monitor
* Plug the ethernet cable in, hopefully dhcp will work and report
* Ping the IP address, hopefully will work, same for http!
