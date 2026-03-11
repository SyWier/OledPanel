# OledPanel

I2C OLED control panel featuring an SH1106 display, 5-way navigation switch, and dedicated A/B buttons. Includes an onboard GPIO expander for button handling, with optional side pin headers exposing a GPIO port for external use. Designed for easy integration into embedded systems.

<img width="1186" height="1102" alt="image" src="https://github.com/user-attachments/assets/d5b88228-68f4-4668-92cd-22785cf97f2c" />


## Hardware - RevB

Designed in **Altium Designer 25.8.1**

**Connection**

The panel can be simply connected through a **4-pin JST-PH (2 mm)** connector. <br>
Additionally there is space for two **7-pin headers** on the two sides:
- The left side exposes an extra port from the GPIO expander for general use.
- The right side contains VCC, GND, SCL, SDA, and additionally (compared to the JST connector) the INT pin.


**OLED (SH1106)**

I2C Address: `0x3C`

The OLED pins can be configured with resistors. his can be useful if, instead of the SH1106, you want to use an SSD1306 OLED display. However, these modules are generally slightly smaller, so the screw holes will be misaligned.

**GPIO Extender (TCA9555)**

I2C Address: `0x20 – 0x27` (configurable via A0-A2 resistors)

The GPIO Extender has two ports: **P0** and **P1**.

Through P0, the button states can be read or polled. The GPIO extender can generate an interrupt signal when an input changes. This signal is available on the INT pin on the right-side header.

The other port, P1, acts as an extra extension for the board. An onboard LED can be controlled through the **P17**, while the other 7 pins are available for general use.
