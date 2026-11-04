# DRAKO GAUGE web installer

Installs DRAKO GAUGE (an OBD2 gauge that reads a Bluetooth ELM327) on an ESP32-2432S028 (CYD) from a
browser over USB: computers with Chrome or Edge (Web Serial), Android phones with Chrome and an OTG
cable (WebUSB, small CH340 driver).

firmware/boot.bin goes to 0x0 and firmware/game.bin to 0xe000, so the settings (NVS 0x9000-0xDFFF)
are kept; "erase" wipes the whole chip first. Installs go through this page only (no one-file image),
so each one is counted.

Uses esptool-js 0.6.1 (Apache-2.0), vendored in mobile/esptool-js/ with its licence.
Made by tee & claude.
