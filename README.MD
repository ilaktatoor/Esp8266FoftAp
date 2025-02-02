# ESP8266 Panic Button with Low Power Mode

## Description
This project implements a panic button using an ESP8266. The ESP8266 will:
1. Detect when a button is **pressed for 5 seconds**.
2. **Turn on an LED for 2 seconds** after detecting the button press.
3. **Enter deep sleep mode** to conserve power when idle.

## Components Required
- **ESP8266 (e.g., NodeMCU, Wemos D1 Mini, etc.)**
- **Push Button**
- **LED**
- **Resistor (Optional, 10kΩ for pull-down)**
- **Jumper Wires**

## Circuit Diagram
| ESP8266 Pin | Component |
|------------|-----------|
| GPIO2 (D4) | LED       |
| GPIO0 (D3) | Button    |
| GND        | Button (other leg) |

🔹 **Note:** GPIO0 (D3) is used because it has a pull-up resistor built-in on most ESP8266 boards.

## Installation & Setup
1. Install the **Arduino IDE** and the **ESP8266 Board Package**.
2. Connect the ESP8266 to your computer via USB.
3. Open the provided `panicButton.ino` file in the Arduino IDE.
4. Select the correct **Board (NodeMCU, Wemos, etc.)** and **Port**.
5. Upload the code to the ESP8266.

## Usage Instructions
1. Press and hold the button for **5 seconds**.
2. The **LED will turn on for 2 seconds**.
3. The ESP8266 will then **enter deep sleep mode**.
4. To wake up, **reset the ESP8266** (or use an external wake-up mechanism).

## Power Saving & Wake-Up
- The ESP8266 enters **deep sleep mode** to conserve power.
- **To wake up automatically**, connect **GPIO16 (D0) to RST**.
- Alternatively, use an **external circuit to pull RST low** when needed.

## Notes
- Deep sleep mode disables Wi-Fi and other peripherals.
- If using an **external power source**, ensure it supports waking up from deep sleep.

## License
This project is open-source. Feel free to modify and distribute it.

## Author
Developed by [Rootatkali]


