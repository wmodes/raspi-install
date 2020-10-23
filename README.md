# Raspberry Pi Standard Install for Development or Projects

* **Pi Version:** Raspberry Pi 3 B+
* **PiOS Version:** Raspberry Pi OS (32-bit) 2020-08-20
* **Date:** 2020/10/23

**A Note:** These are my notes to help me streamline the process of readying a Raspi for development or project work. Your use and therefore your process may vary. My engagement with the Pi is episodic and these notes may fall out of date as new technology and new tools may emerge.

## Use Case

I frequently use Raspberry Pis to serve as a behind-the-scenes controller for projects. In the last several years, the Pi has controller for:

* A retro gaming system
* A "chicken robot" to open and close the doors of our chicken coop, and serve IR camera images so we could confirm the door was closed and everyone accounted for
* An audio and visual piece at Burning Man
* Controller for a musical instrument and LED controller for another piece at Burning Man
* A smart video sequencer/player for art exhibitions
* A primary controller and video/audio player with various arduino secondaries to control peripherals in an art installation
* A "time machine" radio that allowed you to tune in to various radio stations that represented different eras and styles

In all these cases, the Pi was the obvious choice because of its incredible adaptibility and modularity, including:

* standard Unix OS/Debian
* ability to run python and its many useful modules
* Chromium browser with leading edge JavaScript support
* GPIO access to control hardware
* selection of various inexpensive hats/peripheral boards

## Imaging Card

In the past, I'd imaged my Pi SD card from the command line because there was not a mature card imager (let alone one specifically for Raspberry OS) for MacOS.

1. Go to https://www.raspberrypi.org/documentation/installation/installing-images/
2. Go to section "Using Raspberry Pi Imager"
3. Download the latest version of Raspberry Pi Imager
4. Install and run
5. Install the latest version of Raspberry Pi OS (formerly Raspbian) to your SD card

Voila! Simple as Pi.

## Basic Configuration

We'll be doing the basic configuration through the GUI. So install the SD card, plug in a monitor, keyboard, and mouse, and power it up.

1. Go through the startup menus, choosing your language, password, wireless network, etc
1. Allow the Pi to update to the latest software and packages
1. Go to Pi Menu > Preference > Raspberry Pi Configuration
1. Under the Systems tab, rename your system
1. Under the Interface tab, Enable SSH and any other interfaces you need to enable
1. Reboot as necessary

## Git Configuration

We'll use git and github to manage our development. This allows us to code on our favorite development machine/IDE/editor, push changes, and pull them down to the pi. 

1. First we create an ssh key so we can clone from github.
  1. Open up the pi terminal and run:
    `cd ~/.ssh && ssh-keygen`
  1. Show your public key with
    `cat id_rsa.pub`
  1. Select and copy
  1. On the github.com website, go to Profile (upper right) > Settings > SSH and GPG keys > New SSH Key, paste in your SSH public key
  
  

