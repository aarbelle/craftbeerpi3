# CraftBeerPi V3.0

This is CraftBeerPi version 3.0. It's the same version as the original but this install actually does work. The installation will install all missing dependencies. I have also altered the menu a bit - and provided an option for installing a working running demo, bye providing to sample databases. There is a single kettle demo database inclued (Menu 9 selection) -and also a three kettle HEMRS demo database (Menu 10 selection)

ATT: You must stop the current running craftbeerpi service (Menu 6 selection) - before you attempt to move the empty database and install a "demo" system. After either menu (9) or (10) is run, make sure you restart the craftbeerpi service (Menu 5 selection)

So - What Raspbian image should you download and use? well, I have used the Raspbian Buster STD (https://downloads.raspberrypi.org/raspbian_latest) - missing dependencies included is only tested on this release. I would guess the "lite" release have even more missing, so -to avoid faulty installations, use the one from the link above. This will ensure a successfull and problemfree installation, as of 14.05.2020 at least :)


## Introduction Video

https://www.youtube.com/watch?v=YGARUJgFWh4&t=1s

## Installation

Open a terminal window on Raspberry Pi and type:

<code> git clone https://github.com/BrewChef/craftbeerpi3</code>

This will download (clone) the software to your local Raspberry Pi.

Type <code>cd craftbeerpi3</code> to navigate into the craftbeerpi folder.

Type <code>sudo ./install.sh</code>

Open browser - goto http://xxx.xxx.xxx.xxx:5000 (xxx is your RaspberryPi`s IP address.
It all should work now. If something does not start - run sudo ./run.py - look for missing components, if any -add with 
sudo pip install xx - where xx is the missing components name - as displayed in upper or lower - or combined letters.

## Hardware Wiring

Here you will find a guide how to wire everything up.

http://web.craftbeerpi.com/hardware/

## ATTENTION

CraftBeerPi 3.0 is a complete rewrite. Server as well as user interface. I recommend to use a second SD card for testing.

## Docker-based development

For developing this application or its plugins on a PC/Mac you can use the docker-compose file:

``` shell
$ docker-compose up
...
Starting craftbeerpi3_app_1 ... done
Attaching to craftbeerpi3_app_1
app_1  | [2018-08-13 12:54:44,264] ERROR in __init__: BUZZER not working
app_1  | (1) wsgi starting up on http://0.0.0.0:5000
```

The contents of this folder will be mounted to `/usr/src/craftbeerpi3` and the server will be accesible on `localhost:5000`.

## Donation

CraftBeerPi is a free & open source project. If you like to support the project I happy about a donation:

[![Donate](https://www.paypal.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=2X9KR98KJ8YZQ)
