DAMI 3000: An Advanced Arduino Robot
This repository contains the full code for DAMI 3000, a versatile Arduino-based robot designed to demonstrate several key robotics and embedded systems concepts. The robot features multiple operational modes, including Bluetooth control and autonomous maze navigation, all managed through a comprehensive user interface.

🚀 Features
Multi-Mode Operation: Select from four distinct operational modes using a 4x4 keypad:
Bluetooth Mode (1): Remotely control the robot's movement (forward, backward, left, right) and other functions (servo, buzzer) via a Bluetooth connection. An ultrasonic sensor displays real-time distance on the LCD and streams it to the Bluetooth module.



Maze Mode (2): The robot autonomously navigates a maze using a left-hand rule algorithm. It utilizes a servo-mounted ultrasonic sensor to scan its surroundings and avoid obstacles.


Testing Mode (3): A built-in diagnostic mode that sequentially tests the motors and servo to ensure all components are functioning correctly.
VC Mode (A): A dedicated mode for custom or future functionality.
Intuitive User Interface: The robot's status and menu are displayed on a 16x2 I2C LCD. A 7-segment display provides clear visual feedback for mode selection and status.




Safety Features: A global emergency stop function is available via a dedicated keypad button (D) and a Bluetooth command (X). This feature immediately halts all motors and provides an audible and visual alert.


Dynamic Visual Feedback: A series of LEDs (Green, Red, Blue) provide a welcoming sequence and dynamic light patterns that respond to the robot's current mode and state.



🛠️ Hardware Requirements
To replicate this project, you will need the following components:
Arduino Mega 2560 or similar board
L298N Motor Driver
2x DC Motors
1x Micro Servo Motor (SG90)
1x HC-SR04 Ultrasonic Sensor
1x 4x4 Keypad
1x 16x2 LCD with I2C Module
1x 7-Segment Display
1x Buzzer
LEDs (Red, Green, Blue, White) and resistors
1x Potentiometer
Bluetooth Module (e.g., HC-05)
⚙️ Installation & Setup
Libraries: Install the following Arduino libraries through the Arduino IDE's Library Manager:
LiquidCrystal_I2C
Servo
Keypad
Wiring: Follow the pin definitions in the code to connect all components to your Arduino board.
Motors: ENA (pin 3), ENB (pin 4).
Servo: Pin 2.
Ultrasonic Sensor: TRIG (pin 43), ECHO (pin 44).
Keypad: Rows (pins 35-38), Columns (pins 34-30).
LCD: I2C (address 0x27).
Code Upload: Open Final Working Code.txt in the Arduino IDE and upload it to your board.
🏃 Usage
Upon startup, the robot will perform a brief welcome sequence. The LCD will then display a menu. Use the keypad to select a mode:

Press '1' for Bluetooth Mode.
Press '2' for Maze Mode.
Press '3' for Testing Mode.
Press 'A' for VC Mode.
Emergency Stop: Press 'D' on the keypad at any time to activate the emergency stop.

🤝 Contribution
Feel free to fork this repository, add new features, and open a pull request. Your contributions are welcome!
