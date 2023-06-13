---
title: User Manual
permalink: /docs/user-manual
nav_order: 2
---

{: .cover}
![../assets/cover-manual.png](../assets/cover-manual.png)

# Clackotron 2000 User Manual
This user manual covers the whole process of building and programming a device. If you have bought a completed, pre-programmed PCB or Clackotron assembly, you may skip to the [Setup](#setup) step below.

# Hardware
## Obtaining the hardware
...

## Hardware overview
The following sketch describes the most important features of the hardware:

![../assets/hardware-sketch.png](../assets/hardware-sketch.png)

ID | Description
--- | ---
(1) | 30V DC input from power supply.
(2) | 30V DC +/- and RS485 A/B line output to modules.
(3) | Mode button - Hold >5s to activate configuration mode.
(4) | Reset button - Hold >10s to reset all settings on the device.
(5) | Power LED - Lights up as soon as device is powered with 30V DC.
(6) | Mode LED - Lights up when in configuration mode.
(7) | Reset LED - Lights up shortly when reset was accepted.
(8) | Battery holder for real time clock (RTC) to keep time.

## Wiring the hardware

{: .warning }
**Always** disconnect your power supply before working on the hardware and/or wiring components!

There are two things that don't come with the Clackotron 2000 hardware. The 30V DC power supply (PSU) and the SBB split flap modules. As such, the harware has connectors for wiring to these components.

The following diagram shows the wiring of a Clackotron 2000 assembly with the hardware. Connect the output of a 30V DC PSU to the `+` and `-` terminals of the input of the Clackotron 2000 hardware. The input is reverse polarity protected, so if you accidentally switch the wires, the Clackotron 2000 will simply not work instead of going up in smoke.

Afterwards, connect the `+`, `-`, `A` and `B` terminals of the Clackotron 2000 output to your SBB split flap modules. The terminals are labelled on both the Clackotron 2000 PCB as well as the SBB split flap display PCBs, so it should be easy to figure out which wire goes where.

Once your are done with everything, you can connect the input of your 30V DC PSU to whatever input it takes (most likey 230V AC) and your Clackotron 2000 will be running.

![../assets/hardware-wiring.png](../assets/hardware-wiring.png)

# Software
## Building or downloading webinterface
...

## Building and uploading firmware
...

## Uploading a firmware upate
...

# Setup
## Connecting to your home WiFi network
The Clackotron 2000 uses the [WiFi manager](https://github.com/tzapu/WiFiManager) library to allow the user to easily connect it to an existing WiFi network. When the Clackotron 2000 is first started (or no WiFi network has been configured yet), it will create a WiFi hotspot called `Clackotron2000`.

![../assets/setup-wifi-1.png](../assets/setup-wifi-1.png)

You can connect to this hotspot using any WiFi capable device such as your Android or iOS mobile phone or a laptop. After connecting, you should automatically be redirected to the captive portal that allows you to configure the WiFi settings. If you are not automatically redirected, open `http://192.168.4.1` in your browser to access the WiFi manager.

![../assets/setup-wifi-2.png](../assets/setup-wifi-2.png)

Select the `Configure WiFi` option from the WiFi manager screen.

Select the name of your WiFi access point from the list or enter it in the `SSID` field. Enter the password of your WiFi access point in the `Password` field and click "Save".  

![../assets/setup-wifi-3.png](../assets/setup-wifi-3.png)

After saving the WiFi configuration, the Clackotron 2000 will connect to your home WiFi network.

**KNOWN ISSUE:** The device does not currently automatically connect after storing the credentials. You need to manually reboot (e.g. unplug, wait for a few seconds and plug back in) the device. This is related to the device not automatically re-connecting after losing WiFi connection.


## Finding the device in your network
Once the WiFi setup is complete, the Clackotron 2000 will connect to your home WiFi network. It will receive an IP address from your router via DHCP. This means that for accessing the webinterface of the device, you need to figure out what IP address it has.

The easiest way to do this is to log in to the router webinterface and look for the new device.

## Configuring the device
By default, the Clackotron is configured to use 4 modules in a 2-line configuration with the serial numbers `1,2` and `3,4` respectively. You will most likely need to update the configuration 

