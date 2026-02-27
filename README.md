# OledPanel

I2C OLED control panel featuring an SH1106 display, 5-way navigation switch, and dedicated A/B buttons. Includes an onboard GPIO expander for button handling, with optional side pin headers exposing a GPIO port for external use. Designed for easy integration into embedded systems.

## Hardware

Designed in **Altium Designer 25.8.1**

I2C Devices:
- SH1106 - address: `0x3C`
- TCA9555 - address: `0x20 – 0x27` (configurable via A0-A2 resistors)

## Known issues
- The SH1106 pinout is mirrored.<br>
**Fix:** Jumper the resistor pads to the correct OLED pins using thin wire.
