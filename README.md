# STARBOY

**My PCB:**   


![My PCB](https://github.com/user-attachments/assets/cbc6b0e9-7dd6-4413-b215-841b4065112d)

**Original Starbie Image:**
![Original Starbie Image](https://github.com/user-attachments/assets/1e089bf2-8aab-477a-9eee-4215cfdacb44)

[![View PCB on KiCanvas](https://hack.club/pcb-badge)](https://kicanvas.org/?repo=https%3A%2F%2Fgithub.com%2FUncle-Noon%2FStarboy-proj%2Ftree%2Fmain%2FStarboy)   < -- (click to open PCB design) 

Starboy is a tiny motion-controlled digital pet: basically a desktop Tamagotchi with minimal gameplay buttons. Instead of pressing controls, you interact with it by physically moving the board.

## What It Is

Starboy is designed to sit on your desk, show its personality on a small display, and react to how you handle it. Tilting, moving, and otherwise checking in on your pet are meant to be part of the experience.

The board includes a microcontroller, display, motion sensor, and environmental sensor in a compact PCB design. It is USB-powered and built around beginner-friendly through-hole soldering for the add-on components.

## Repository Contents

- KiCad source files and fabrication exports
- Front and back PCB renders
- Arduino IDE starter sketch

## Firmware & Flashing

Now that the Starboy board is built, it needs a personality. The project runs on a single Arduino sketch (`Starboy.ino`), requiring no complex VS Code or PlatformIO setups. 

### Step-by-Step Upload Guide

**Note:** Ensure that the `Starboy.ino` file remains inside a folder named `Starboy`, as the Arduino IDE requires the folder and sketch names to match.

1. **Get the IDE:** Download and install the latest [Arduino IDE](https://www.arduino.cc/en/software).
2. **Configure Board Manager:** Open `File` → `Preferences`. In the **Additional Boards Manager URLs** field, paste:
   `https://espressif.github.io/arduino-esp32/package_esp32_index.json`
3. **Install ESP32 Package:** Navigate to `Tools` → `Board` → `Boards Manager`. Search for `esp32` and install the package by **Espressif Systems**.
4. **Select the Board:** Go to `Tools` → `Board` → `esp32` and select **XIAO_ESP32C3**.
5. **Install Libraries:** Go to `Sketch` → `Include Library` → `Manage Libraries`. Search for and install the following libraries (if prompted to install dependencies, choose **Install All**):
   - `Adafruit GFX Library`
   - `Adafruit SSD1306`
   - `Adafruit MPU6050`
   - `DHT sensor library`
6. **Flash to Starboy:** Open the `Starboy.ino` file, connect the board via USB, and click the arrow-shaped **Upload** button in the top left corner of the Arduino IDE.

### How to Interact (Controls)

| Action | What it does |
| :--- | :--- |
| **Button 1 (First Press)** | Opens the radial menu. |
| **Tilt (While menu is open)** | Moves the selector ball to highlight an action sector. |
| **Button 1 (Second Press)** | Confirms the highlighted action. |
| **Button 2** | Shows or hides the stats screen. |
| **Shake** | Gives Starboy a dizzy/shake reaction! |

**Fun Actions:** Selecting `PLAY` makes it sprint quick laps with hearts, while `PET` makes hearts float upward. Other actions trigger a short wiggle and jump.

### Tutorial Link
[Original Starbie Repository Tutorial](https://github.com/SharKingStudios/Starbie/blob/main/README.md)

## BOM (Bill of Materials)

| Part | What it's for | Qty | Unit | Total | Vendor |
| --- | --- | --- | --- | --- | --- |
| [XIAO ESP32 C3](https://www.seeedstudio.com/Seeed-XIAO-ESP32C3-p-5431.html) | microcontroller | 1 | $5.00 | $5.00 | [Seeed Studio](https://www.seeedstudio.com/Seeed-XIAO-ESP32C3-p-5431.html) |
| [0.96 OLED](https://www.amazon.com/dp/B0GBVWBWCR) | screen | 1 | $2.50 | $2.50 | [Amazon](https://www.amazon.com/dp/B0GBVWBWCR) |
| [MPU6050](https://www.amazon.com/dp/B0943SGP34) | gyroscope | 1 | $2.30 | $2.30 | [Amazon](https://www.amazon.com/dp/B0943SGP34) |
| [DHT11](https://www.amazon.com/dp/B0BLG7R99R) | humidity sensor | 1 | $3.33 | $3.33 | [Amazon](https://www.amazon.com/dp/B0BLG7R99R) |
| [MX Switches](https://www.amazon.com//dp/B0FQP8VYX4) | buttons | 4 | $0.18 | $0.72 | [Amazon](https://www.amazon.com//dp/B0FQP8VYX4) |
| [Keycaps](https://www.amazon.com/dp/B0CQ2VLMVY) | Buttons | 4 | $0.60 | $2.40 | [Amazon](https://www.amazon.com/dp/B0CQ2VLMVY) |
| [10k Resistor](https://www.amazon.com/dp/B0B4JFPHTW) | resistance | 1 | $0.05 | $0.05 | [Amazon](https://www.amazon.com/dp/B0B4JFPHTW) |
| [PCB](https://www.jlcpcb.com/) | The main thing | 1 | $10.00 | $10.00 | [JLCPB](https://www.jlcpcb.com/) |
| **Parts subtotal** | — | — | — | **$26.30** | — |
| **Tax & shipping** | — | — | — | **$0.00** | — |
| **Total** | — | — | — | **$26.30** | — |

![Starboy Project Image](https://github.com/user-attachments/assets/3580e60e-09be-440b-8d6b-694dc0c062d0)

*(P.S. I named my project Starboy instead of Starbie)*
