# ESP32 Camera Project

This project leverages the capabilities of the ESP32 camera module to demonstrate four key functionalities: local camera access, flashlight control, video streaming over a global network, and image retrieval using a Telegram bot. Each feature showcases the versatility of the ESP32 in real-world applications, from home automation to IoT-based surveillance.

## Features

1. **Local Camera Access**  
   Access the camera feed on your local network using the IP address assigned to the ESP32. This allows you to monitor the feed within your home network without needing an external internet connection. The camera feed is accessible through a web browser, making it easy to view on multiple devices.

2. **Flashlight Control**  
   The ESP32's built-in LED can be controlled remotely, functioning as a flashlight. You can turn the flashlight on and off using a simple web interface, making it useful for low-light situations or as an additional signaling feature.

3. **Global Video Streaming**  
   The project includes a feature that streams live video from the ESP32 camera, accessible from anywhere in the world. By setting up port forwarding on your router or using a cloud-based service, you can access the stream via the internet, making it ideal for remote monitoring.

4. **Telegram Bot Integration**  
   A custom Telegram bot is used to retrieve images from the ESP32 camera. By sending specific commands to the bot, you can request snapshots from the camera, which will be delivered directly to your Telegram chat. This feature is useful for quickly checking in on your camera feed from anywhere using a familiar interface.

## How It Works

The ESP32 module is programmed using the Arduino IDE. The project involves setting up a web server on the ESP32, configuring a local network, and integrating the various functionalities:

- The web server handles both the local camera access and flashlight control.
- For global video streaming, network configurations like port forwarding or dynamic DNS are set up.
- The Telegram bot is created using the BotFather and communicates with the ESP32 through HTTP requests to fetch images.

## Setup Instructions

1. **Hardware Required**:
   - ESP32-CAM module
   - FTDI programmer (for uploading code)
   - Jumper wires

2. **Software Requirements**:
   - Arduino IDE with ESP32 board support
   - Telegram Bot API
   - Libraries: `ESP32WebServer`, `WiFi`, `UniversalTelegramBot`

3. **Steps to Upload Code**:
   - Connect the ESP32-CAM to your computer using an FTDI programmer.
   - Load the provided code in the Arduino IDE and configure your Wi-Fi credentials.
   - Upload the code and monitor the serial output for the IP address.

4. **Configure Global Access** (Optional):
   - Set up port forwarding on your router to make the camera stream accessible via the internet.
   - Alternatively, use a dynamic DNS service to map your changing IP address to a static URL.

5. **Telegram Bot Setup**:
   - Create a bot using BotFather on Telegram.
   - Get the API token and insert it into the code.
   - Run the bot to start receiving images on request.

## Applications

- **Home Surveillance**: Monitor your home remotely with the global streaming feature.
- **DIY Projects**: Experiment with IoT and embedded systems.
- **Automation**: Integrate with other smart devices using the Telegram bot or custom web-based controls.

## Future Improvements

- Adding motion detection and automated alerts.
- Integration with cloud storage for saving images and videos.
- Implementing face recognition for enhanced security.

