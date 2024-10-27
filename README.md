# ESP8266 Web Server Controller for Servo Motor

## Project Overview

This project implements a web server using the **ESP8266** module to remotely control a **servo motor** via a web interface. Users can control the motor's position using a simple, responsive web page built with HTML, CSS, and JavaScript. The ESP8266 serves as both the web server and the communication bridge between the web page and the servo motor.

This project demonstrates how to control hardware over Wi-Fi using the **ESP8266** and how to handle **HTTP requests** to manage real-time motor movement.

# Project Screenshots
## 1. Hardware Setup
![Hardware Setup](https://github.com/Payal-Sinha09/ESP8266-Web-Server-Controller-for-Servo-Motor/blob/main/images/WhatsApp%20Image%202024-10-22%20at%209.26.16%20PM.jpeg)
## 2. Laptop Screen
![Laptop Screen](https://github.com/Payal-Sinha09/ESP8266-Web-Server-Controller-for-Servo-Motor/blob/main/images/Screenshot%20(171).png)
## 3. Phone Screen
![Phone Screen](https://github.com/Payal-Sinha09/ESP8266-Web-Server-Controller-for-Servo-Motor/blob/main/images/WhatsApp%20Image%202024-10-22%20at%209.26.21%20PM.jpeg)

# Video Demonstration
[Watch the demo video](https://github.com/Payal-Sinha09/ESP8266-Web-Server-Controller-for-Servo-Motor/blob/main/images/WhatsApp%20Video%202024-10-27%20at%2010.26.25%20AM.mp4)

## Features

- **ESP8266 Web Server**: Uses the ESP8266 to host a web page for motor control.
- **Remote Motor Control**: Control the servo motor's position through a web interface.
- **Responsive Interface**: Web page built using HTML, CSS, and JavaScript for easy control.
- **Motor Angle Adjustment**: Adjust the servo motor's angle (0° to 180°) in real-time through button clicks.
- **Wi-Fi Connectivity**: ESP8266 communicates over Wi-Fi, allowing control from any device connected to the network.
- **Real-Time Feedback**: The ESP8266 provides feedback on the current position of the servo motor.

## Components Required

- **ESP8266 Module** (e.g., NodeMCU or Wemos D1 Mini)
- **Servo Motor** (e.g., SG90)
- **Power Supply** (e.g., 5V USB or battery)
- **Jumper Wires** and **Breadboard**
- **PC with Arduino IDE** (to program the ESP8266)
- **Wi-Fi Network** (for communication)

## Installation

1. **Hardware Setup**:
   - Connect the servo motor to the ESP8266:
     - **VCC** to 3.3V (or 5V depending on your servo motor).
     - **GND** to GND.
     - **Signal Pin** (usually yellow/white) to GPIO pin (D4 or D5).
   
2. **Software Setup**:
   - Clone this repository to your local machine:
     ```bash
     git clone https://github.com/YourUsername/ESP8266-Servo-Motor-Controller.git
     ```

   - Install the required libraries for ESP8266 in the Arduino IDE:
     - Open Arduino IDE, go to **File > Preferences**, and add the ESP8266 board manager URL:
       ```
       http://arduino.esp8266.com/stable/package_esp8266com_index.json
       ```
     - Go to **Tools > Board > Boards Manager**, search for **ESP8266**, and install it.

   - Open the `servo_controller.ino` file in Arduino IDE.

   - Configure your **Wi-Fi credentials** (SSID and Password) in the code:
     ```cpp
     const char* ssid = "your_SSID";
     const char* password = "your_PASSWORD";
     ```

   - Upload the code to your ESP8266 using the **Arduino IDE**.

3. **Access the Web Interface**:
   - Once the code is uploaded, open the Serial Monitor to get the **IP address** of your ESP8266.
   - Enter the IP address in any web browser connected to the same Wi-Fi network to access the control page.

## Usage

- Use the buttons on the web page to adjust the position of the servo motor.
- The motor will move based on the angle set through the web interface (0° to 180°).
- Refresh the web page to update the motor's position.

## Example

```html
<button onclick="moveServo(0)">Move to 0°</button>
<button onclick="moveServo(90)">Move to 90°</button>
<button onclick="moveServo(180)">Move to 180°</button>
```

## Usage

The web page allows controlling the motor using the following interface:

- **Button 1**: Move to 0°.
- **Button 2**: Move to 90°.
- **Button 3**: Move to 180°.

## Contributing

Feel free to fork the repository, contribute enhancements, and suggest new features. Contributions are welcome via pull requests.
