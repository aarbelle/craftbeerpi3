# CraftBeerPi V3.0

This is CraftBeerPi version 3.0. It's currently in beta status.

## Introduction Video

https://www.youtube.com/watch?v=YGARUJgFWh4&t=1s

## Installation

Open a terminal window on Raspberry Pi and type:

<code> git clone https://github.com/BrewChef/craftbeerpi3</code>

This will download (clone) the software to your local Raspberry Pi.

Type <code>cd craftbeerpi3</code> to navigate into the craftbeerpi folder.

Type <code>sudo ./install.sh</code>
Say no to do an apt-get update/upgrade, we will run it afterwords, since there are some missing dependencies.

1. Run sudo apt-get update
2. Run sudo apt-get upgrade
3. Run sudo apt-get install python-pip y
4. Run sudo pip install flask
5. Run sudo pip install flask_socketio
6. Run sudo pip install flask_classy
7. Run sudo pip install PyYAML
8. Run sudo pip install GitPython
9. Run sudo pip install requests
10. Run sudo pip install gitdb2==2.0.5
11. Run sudo ./install.sh again. Select menu 3 "Add to autostart" then menu 5 "Start CraftBeerPi"
12. Run sudo reboot - might not be needed, but I always do.

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
