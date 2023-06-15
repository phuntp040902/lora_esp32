# LoRa SX1278 Communication with HDT11 Sensor using ESP32

This project demonstrates the communication between two ESP32 microcontroller boards using LoRa SX1278 modules. 


## Description

The LoRa SX1278 Communication with HDT Sensor project utilizes two ESP32 boards equipped with LoRa SX1278 modules to establish a wireless communication link. One board acts as a transmitter, while the other acts as a receiver. The transmitter reads data from an HDT11 sensor and sends it wirelessly to the receiver. The receiver receives the data and can process or display it as required.

## Features

- Wireless communication using LoRa SX1278 modules
- Transmission of data from the HDT sensor
- Reception and processing of data on the receiving end

## Hardware 

- Two ESP32 microcontroller boards (ESP32-WROOM-32)
- LoRa SX1278 modules (one for each board)
- HDT11 sensor
- Additional hardware components for connecting the sensor (if applicable)

## Software 

- Visual Studio Code (VS Code)
- PlatformIO extension for VS Code
- ESP-IDF framework
- ESP32 toolchain
- Serial monitor tool (e.g., miniterm, PuTTY, etc.)
- LoRa library SDK for ESP32 (https://www.espressif.com/en/support/download/sdks-demos)

## Installation and Setup

1. Clone or download the project repository.
2. If you use ESP-IDF, clone project in SDK folder
3. Open the project in VS Code.
4. Customize the project configuration as needed in the 'sdkconfig' file.
5. Connect the ESP32 board to your computer using a USB cable, one COM gate each ESP32
6. Build and flash the firmware using ESP-IDF
7. In the terminal of ESP-IDF, there is an IP address after building the firmware, use that IP to see the data sent.
8. Using 2 ESP-IDF terminal for 2 boards (send and receive) to see the transmitted data 

## Usage

1. Clone project to your SDk folder
```bash
git clone https://github.com/phuntp040902/lora_esp32.git
```

2. Open 2 ESP-IDF CMD terminals and type:
* data transmission circuit:
```bash
cd send_lora
idf.py build
idf.py -p (COM3) flash monitor
```
* data receiving circuit:
```bash
cd receive_lora
idf.py build
idf.py -p (COM7) flash monitor
```

3. Terminal uses for the transmission circuit, there is an IP after flash project, use that IP to access the platform
   

## License


## Notes

1. Change the SSID and Passwork (line 45,46 in station_example_main.c\main\send_lora) as your WiFi


## Acknowledgments

https://www.espressif.com/en


