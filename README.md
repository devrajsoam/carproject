Obstacle Avoiding Robot with Bluetooth and Voice Control
Overview
This project is for an autonomous obstacle-avoiding robot that can be controlled via Bluetooth and voice commands. The robot uses ultrasonic sensors to detect obstacles and avoid collisions. It also has the capability to respond to voice commands for manual control.

Features
Obstacle Avoidance: Uses ultrasonic sensors to detect obstacles and avoid them by steering left or right.
Bluetooth Control: Allows you to control the robot via Bluetooth using commands.
Voice Control: The robot can be controlled using voice commands via serial communication.
Servo for Scanning: The servo moves the ultrasonic sensor to scan left and right for better obstacle detection.
Components Used
Arduino Board (e.g., Arduino Uno)
Ultrasonic Sensor (HC-SR04): Measures the distance between the robot and obstacles.
Servo Motor: Used to rotate the ultrasonic sensor for scanning the left and right sides.
DC Motors with Motor Driver: Used for controlling the movement of the robot.
Bluetooth Module (HC-05 or HC-06): For Bluetooth control via a mobile device.
Power Supply: Provides power to the robot.
Circuit Diagram
You can connect the components as follows:

Ultrasonic Sensor:
Echo Pin → A0
Trigger Pin → A1
Motor Driver (AFMotor):
M1, M2, M3, M4 pins to motor driver channels
Servo Motor: Connect to motor pin (e.g., pin 10).
Bluetooth Module:
Connect the TX and RX pins to the corresponding pins on the Arduino.
Refer to a wiring diagram for complete connections.

Installation
Install the Arduino IDE: Download and install the Arduino IDE.

Install Required Libraries:

AFMotor library (for motor control)
Servo library (for controlling the servo motor)
You can install these libraries via the Arduino IDE:

Go to Sketch > Include Library > Manage Libraries.
Search for AFMotor and Servo and click on Install for both.
Upload the Code:

Open the Arduino IDE and create a new sketch.
Copy and paste the code from the provided .ino file.
Select the correct Board and Port in the Tools menu.
Click Upload to upload the code to your Arduino board.
Bluetooth Setup:

Pair your Bluetooth module (HC-05/HC-06) with your mobile device.
Use a Bluetooth terminal app to send commands (e.g., "F" for forward, "B" for backward, etc.) to control the robot.
Usage
Bluetooth Control:
The robot can be controlled via Bluetooth using a terminal app. The following commands can be used:

'F': Move forward
'B': Move backward
'L': Turn left
'R': Turn right
'S': Stop
Voice Control:
The robot can also be controlled via voice commands through serial input. Use the following commands:

'^': Move forward
'-': Move backward
'<': Turn left if space is available
'>': Turn right if space is available
'*': Stop
Obstacle Avoidance:
The robot will automatically detect obstacles using the ultrasonic sensor. If an obstacle is detected within 12 cm, the robot will:

Stop and move backward.
Scan the left and right sides.
Choose the direction with more space to continue moving.
Manual and Automatic Control:
The robot will follow obstacle-avoidance logic by default.
You can override automatic control and manually control the robot via Bluetooth or voice.
Code Structure
Functions:
Bluetoothcontrol(): Processes Bluetooth commands from the serial input to control the robot's movements.
voicecontrol(): Processes voice commands from serial input to control the robot.
Obstacle(): Handles obstacle detection and avoidance behavior.
ultrasonic(): Measures the distance using the ultrasonic sensor.
forward(), backward(), left(), right(), Stop(): Functions to control the robot’s movement.
leftsee() and rightsee(): Used for obstacle scanning on the left and right side.
License
This project is licensed under the MIT License.

Acknowledgements
The code is developed by Devraj Soam.
The components and libraries used in this project are available from various open-source communities
