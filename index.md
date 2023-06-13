---
title: Home
nav_order: 1
---

# Clackotron 2000

[COVER IMAGE]

The Clackotron 2000 project aims to bring the [split flap modules](https://en.wikipedia.org/wiki/Split-flap_display) used by the [Swiss Federal Railways (SBB)](https://en.wikipedia.org/wiki/Swiss_Federal_Railways) back to life for makers an enthusiasts. Unlike other projects, we intend to provide a complete hardware and software solution that can be used out-of-the-box.

In short, the project consists of the following parts:
* [Hardware](https://github.com/clackotron/clackotron_hardware) - A custom PCB designed in KiCAD that can be ordered (almost fully) assembled.
* [Firmware](https://github.com/clackotron/clackotron_firmware) - A firmware for the ESP32 on the hardware based on PlatformIO and ESP32/Arduino.
* [Webinterface](https://github.com/clackotron/clackotron_webinterface) - A Svelte.js based webinterface that can be built and uploaded with the firmware to have a graphical user interface for the device.

---

This repository serves as the documentation for all parts of the project.

### Contents
* [User manual](docs/user-manual.md)
* [Configuration files](docs/config.md)
  * [`modules.json`](docs/config-modules.md)
  * [`timezone.json`](docs/config-timezone.md)
  * [`webinterface.json`](docs/config-webinterface.md)
* [Additional documentation](docs/misc.md)
  * [Template Format](docs/misc-templates.md)
  * [Webinterface & API](docs/misc-api-docs.md)
* [Specific use cases](docs/uc.md)
  * [Rewriting module address](docs/uc-rewrite-address.md)

---

### Special Thanks
A lot of the Clackotron2000 project is based on information compiled by Adfinis in their awesome [sbb-fallblatt](https://github.com/adfinis/sbb-fallblatt) repository. If you are looking for a more in-depth technical documentation of the split-flap modules themselves, or even documentation for the old (first generation) modules, definitely check out their work! 

