# Mekamate Controlling App

## Overview
Mekamate is a robot designed to help industries manage their inventories and more fluidly exchange different packages on production lines. This repository contains the code for the robot's management and control application, designed to provide customers with an easy-to-use interface for controlling and monitoring the robot. This document outlines the app's features and provides a detailed explanation of its implementation, including architecture, key components, and technologies used.

## Features

 ![The App Interface](/assets/images/interface.png)

### Manual Control
- **Buttons**: Connect to, specify start point, end point and send the robot with dedicated buttons.

 ![Buttons](/assets/images/buttons.png)

### Automated Tasks
- **Path Seeking**: By choosing a starting point and a arrival point, an optimal path is determined and sent to the robot for him to follow.
- **Routine Management**: Save and manage routine tasks for quick execution.

### Real-Time Monitoring
- **Robot Status**: Allows you to know at all times whether the robot is at a standstill, in motion or encountering an obstacle..
 ![Robot Status](/assets/images/status.png)

- **Alerts**: Receive alerts for obstacles, connections and other important events.

### Configuration
- **Settings**: Customize the app's settings to suit your preferences.

## Implementation Details

### Architecture
The app follows a client-server architecture:
- **Client**: The mobile application, developed using MIT Inventor App (iOS and Android).
 ![MIT Inventor App Designer Interface](/assets/images/mit_des_intface.png)

- **Server**: A backend server implemented using MIT Inventor App blocks, handling communication between the app and the robot.

 ![MIT Inventor App Block Interface](/assets/images/mit_block_intface.png)

- **Robot**: Equipped with a microcontroller (e.g., Arduino, Raspberry Pi) and sensors, connected via Wi-Fi.

### Technologies Used
- **MIT Inventor App**: For building the cross-platform mobile application and its backend using the blocks.
- **MQTT Protocol**: For real-time communication between the app and the robot via messages.
- **Wi-Fi**: For connectivity between the app and the robot.

### Key Components

#### 1. User Interface
- **MIT Inventor App Designer Interface**: Utilized for building a responsive and intuitive user interface.

#### 2. Communication
- **MQTT**: Established between the app and the server to facilitate real-time data exchange.
 ![MQTT Package](/assets/images/mqtt_package.png)

- **Wi-Fi**: Used to connect the mobile app to the robot, allowing for control and data transmission.
 ![Wifi Package(Web)](/assets/images/wifi_package.png)


#### 3. Control Logic
- **Manual Control**: Processes user input from the buttons, sending control commands to the robot.
 ![Blocks for pathfinding](/assets/images/blocks_pathfinding.png)

- **Automated Tasks**: Manages path planning, sending appropriate commands to the robot based on the tasks finded.

#### 4. Real-Time Monitoring
- **Robot Status**: Utilizes MQTT to receive and send messages to the robot, thus always knowing its current status.
 ![Blocks for robot status](/assets/images/blocks_robots_status.png)

- **Alerts**: Configured to trigger notifications for specific events (e.g., connections, obstacles).

### Implementation Steps

#### 1. Setting Up the Development Environment
- Create an MIT Inventor App Account.
- Download an MQTT server Client Extension for communication (UrsAI2PahoMqtt preferred).
- Configure the microcontroller with the necessary firmware to interface with the app.

#### 2. Developing the Mobile App
- Create the app structure using MIT Inventor App Designer Interface.
- Implement the user interface for manual control, automated tasks, and real-time monitoring.

#### 3. Implementing the Backend
- Set up the interactions and the logic behind your user interface in the MIT Inventor App Blocks Interface.
- Implement MQTT client interactions for real-time control and monitoring.

#### 4. Robot Integration
- Program the microcontroller to handle commands from the app.
- Set up Wi-Fi connectivity for communication with the app.
- Integrate sensors, and configure them to send data to the app.

#### 5. Testing and Calibration
- Test the app's functionality in various scenarios.
- Calibrate the robot's sensors and controls for accurate operation.
- Perform usability testing to ensure a smooth user experience.

 ![All the blocks for the app](/assets/images/blocks.png)


## Getting Started

### Installation
1. **Download the App**: Download the Mekamate Controlling App Apk from this repository.
2. **Install**: Follow the installation instructions for your device.

### Connecting Your Robot
1. **Power On**: Turn on your robot and ensure it is in pairing mode.
2. **Wi-Fi**: Open the app and connect to your robot via Wi-Fi.

## User Guide

### Manual Control
- **Buttons**: Tap the **Connect** button to connect with the robot, the **Location A** button to choose the starting point, **Location B** to choose the destination, and **Go** to find the shortest path to be sent to the robot.

### Automated Tasks
- **Path Seeking**: Use the map interface to draw a path for your robot to follow.
- **Routine Management**: Save last travels tasks for easy access.

### Real-Time Monitoring
- **Sensor Data**: View real-time sensor data in the sensor dashboard.
- **Alerts**: Configure alert notifications in the settings menu.

## Troubleshooting

### Common Issues
- **Connection Problems**: Ensure your robot is powered on and connected to the internet. Restart the app and try reconnecting.
- **Firmware Updates**: Ensure your robot has the latest firmware installed. Check for updates in the firmware update section.

## License
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgements
We would like to thank all contributors and the open-source community for their support and contributions.

---

**Developed by [Tekbot](#)**
