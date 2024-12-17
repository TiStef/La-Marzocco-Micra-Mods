# **La Marzocco Micra Add-Ons**

![Project Image](image.png)

This repository contains a sample configuration file designed to integrate the **La Marzocco Micra** espresso machine into a smart home environment using **Home Assistant** and **ESPHome**. These add-ons enhance functionality by enabling real-time monitoring and machine control without the need a phone.

### Demo Video


[![Watch the Demo Video](https://img.youtube.com/vi/x1dEXdpyUi8/0.jpg)](https://www.youtube.com/shorts/x1dEXdpyUi8)
---

## **Project Overview**

This project connects the La Marzocco Micra to an **ESP32-based LilyGO TTGO T-Display** board, unlocking features for monitoring and control.

### **Key Features**  

- **Shot Timer Display**  
  - Real-time shot timer is displayed on the LilyGO TTGO T-Display.  
  - Text sensor data is captured from the La Marzocco Micra and updated dynamically.  

- **Machine Control**  
  - **GPIO35 Button (ON CLICK)**: Toggles the machine power **ON/OFF**.  
  - **GPIO0 Button (ON CLICK)**: Enables or disables the **steam boiler**.  

- **Deep Sleep Mode**  
  - **Long Press GPIO0 (3 seconds)**: Puts the ESP32 board into Deep Sleep mode to save battery.  
  - **GPIO35 (ON CLICK)**: Exits Deep Sleep and wakes up the controller.  

- **Battery Monitoring and Icons**  
  - Displays battery percentage on the TTGO T-Display screen.  
  - Visual icons indicate:  
    - **Power ON**  : the Micra is powered
    - **Steam Boiler ON**  : the steam boiler is activated

---

## **Setup Instructions**

### **1. Home Assistant Hub**  

To get started, you need a working **Home Assistant** setup, which will serve as the central hub.  

- Install Home Assistant on a dedicated server, such as a **Raspberry Pi**.  
- Follow the official installation guide here: [Home Assistant Raspberry Pi Installation](https://www.home-assistant.io/installation/raspberrypi).  
- Ensure that the La Marzocco Micra is integrated with Home Assistant using the excellent work by Josef Zweck:  
  [La Marzocco Integration](https://github.com/zweckj/lamarzocco).  

---

### **2. ESPHome Configuration**  

The **ESP32 board** is configured using **ESPHome**, a tool that allows seamless integration with Home Assistant.  

- Install ESPHome: Follow the [ESPHome Getting Started Guide](https://esphome.io/guides/getting_started_command_line).  
- Flash the ESP32 board with the provided YAML configuration file and the other basic info needed (Wifi password, OTA etc).  
- Modify the configuration to match your environment:  
   - Update entity IDs for switches and text sensors.  
   - Verify GPIO pin mappings.  

Once the board is configured, it will communicate with Home Assistant allowing you to control some basic functionality and display the shot timer on the TTGO screen.

---

## **Parts List**

### **Required Components**  

1. **LilyGO T-Display ESP32 Board**  
   - Compact and affordable ESP32-based controller with a built-in 1.14" LCD.  
   

2. **LiPO Rechargeable Battery** *(Optional)*  
   - Allows portable operation of the ESP32 board.  
   - ⚠️ Ensure compatibility with the board’s voltage and current requirements.  

3. **USB-C Cable**  
   - Powers the ESP32 board if a battery is not used.  

---

## **Disclaimer**  

⚠️ **Important Notes**:  

- The author is **not responsible** for any damage to you, your devices, or your surroundings caused by recreating this project or any part of it.  
- Reproducing this project involves working with **electrical circuits** and **batteries**, which may pose safety risks if mishandled.  
- Follow all safety guidelines, consult hardware documentation, and take appropriate precautions.  
- Use this project entirely **at your own risk**.  

This project is shared for educational purposes only. The author assumes no liability for misuse.

---

## **Special Thanks**  

This project builds upon the exceptional work of **Josef Zweck**, who created the La Marzocco integration for Home Assistant.  
- GitHub: [Josef Zweck](https://github.com/zweckj)  
- Project: [La Marzocco Integration](https://github.com/zweckj/lamarzocco)  

---

**Happy brewing!** ☕  

