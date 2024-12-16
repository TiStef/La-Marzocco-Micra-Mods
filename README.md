# **La Marzocco Micra Add-Ons**

This repository contains scripts and configuration files designed to enhance the La Marzocco Micra experience. These add-ons allow you to integrate the espresso machine into a smart home environment with **Home Assistant** and **ESPHome**, enabling monitoring and automation capabilities.

This project integrates the La Marzocco Micra with Home Assistant and an ESP32-based LilyGO TTGO T-Display to enhance its functionality. Key features include:

- **Shot Timer Display**: 
  - Text sensor data from the La Marzocco Micra is captured and displayed on the TTGO T-Display screen, allowing real-time monitoring of brewing activity.
  
- **Machine Control**:
  - **GPIO35 Button**: Toggles the machine ON/OFF directly from the board.
  - **GPIO0 Button**: Enables or disables the steam boiler.

The video below demonstrates the board's functionality and its integration with the La Marzocco Micra:

## **Demonstration Video**

[![Watch the video](https://via.placeholder.com/800x400.png?text=Click+to+watch+the+video)](https://raw.githubusercontent.com/TiStef/La-Marzocco-Micra-Mods/main/micra_ESP32.mp4)

[Watch the demonstration video](https://raw.githubusercontent.com/TiStef/La-Marzocco-Micra-Mods/main/micra_ESP32.mp4)


---

Setting up the system requires some familiarity with network configurations and basic coding, but this guide will walk you through the necessary steps.

## **Home Assistant Hub**

To get started, you’ll need to set up a **Home Assistant (HA)** hub. Home Assistant is an open-source home automation platform that acts as the central control system for all smart devices.

1. Create an account at [Home Assistant](https://www.home-assistant.io).
2. Set up a dedicated server for the HA hub. A **Raspberry Pi** is a popular choice, offering simplicity and affordability.
3. Follow the official installation guide for Raspberry Pi: [Home Assistant Raspberry Pi Installation](https://www.home-assistant.io/installation/raspberrypi).

---

## **ESPHome**

To integrate an **ESP32 board** with Home Assistant, this project uses **ESPHome**—a simple yet powerful platform for managing ESP-based devices. ESPHome is fully integrated into Home Assistant and requires only a YAML configuration file to get started.

### **Why ESPHome?**
ESPHome simplifies communication between the ESP32 and Home Assistant by abstracting low-level details, making it accessible for beginners and robust enough for advanced users.

### **How to Set Up ESPHome**
1. Install ESPHome: [ESPHome Getting Started Guide](https://esphome.io/guides/getting_started_command_line).
2. Flash the ESP32 board with your configuration file using ESPHome CLI or another flashing method.

Once configured, the ESP32 board will communicate seamlessly with your Home Assistant hub.

---

## **Parts List**

This project requires just a few components:
1. **ESP32 Board**  
   - I recommend the [LilyGO T-Display ESP32](https://lilygo.cc/products/lilygo®-ttgo-t-display-1-14-inch-lcd-esp32-control-board) for its affordability, compact size, and compatibility with USB-C and battery power. The built-in 1.14-inch LCD is an added bonus for displaying real-time data.
   
2. **Power Source**  
   - If you plan to use the ESP32 board with a **LiPO rechargeable battery**, ensure the battery is compatible with the board’s voltage and current requirements.
   - ⚠️ *Each board has different power requirements. Seek expert advice or refer to the board’s specifications to select a suitable battery.*

---

## **Disclaimer**

Disclaimer and Warning

Recreating this project involves working with potentially hazardous components, such as batteries and electrical circuits. It is strongly advised that only individuals with sufficient expertise in handling such components attempt to replicate this project.

Important Notes:
	•	The author is not responsible for any damage to you, your devices, or your surroundings caused by recreating this project or any part of it.
	•	If you choose to replicate this project, you do so entirely at your own risk.
	•	This project involves working with electronic components and batteries, which may pose safety risks if not handled properly.
  • Ensure you follow all safety guidelines and consult the board’s documentation before proceeding

This project is shared for educational purposes only, and the author does not assume any liability for its use or misuse.

---

## Special thanks
This little add-on was only possibile thanks to the amazing work Josef Zweck (https://github.com/zweckj) did for the La Marzocco integration into Home Assistant: https://github.com/zweckj/lamarzocco
Thanks to him, Home Assistant and ESPHome!

Feel free to suggest improvements or report issues via GitHub. Happy brewing! ☕
