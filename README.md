Here is a comprehensive README.md file for your Arduino project, based on the provided code.

---

# DAMI 3000: An Advanced Arduino Robot

This repository contains the full code for DAMI 3000, a versatile Arduino-based robot designed to demonstrate several key robotics and embedded systems concepts. The robot features multiple operational modes, including Bluetooth control and autonomous maze navigation, all managed through a comprehensive user interface.

## 🚀 Features

* [cite_start]**Multi-Mode Operation**: Select from four distinct operational modes using a 4x4 keypad[cite: 401, 402, 403]:
    * [cite_start]**Bluetooth Mode (1)**: Remotely control the robot's movement (forward, backward, left, right) and other functions (servo, buzzer) via a Bluetooth connection[cite: 455, 468, 565, 566, 567, 568, 569, 570, 571, 572, 573, 574, 575, 576, 577, 578, 579, 580, 581, 582, 583, 584, 585, 586]. [cite_start]An ultrasonic sensor displays real-time distance on the LCD and streams it to the Bluetooth module[cite: 478, 479].
    * [cite_start]**Maze Mode (2)**: The robot autonomously navigates a maze using a left-hand rule algorithm[cite: 432]. [cite_start]It utilizes a servo-mounted ultrasonic sensor to scan its surroundings and avoid obstacles[cite: 410, 434, 435].
    * [cite_start]**Testing Mode (3)**: A built-in diagnostic mode that sequentially tests the motors and servo to ensure all components are functioning correctly[cite: 436, 437].
    * [cite_start]**VC Mode (A)**: A dedicated mode for custom or future functionality[cite: 465, 466].
* [cite_start]**Intuitive User Interface**: The robot's status and menu are displayed on a 16x2 I2C LCD[cite: 413, 499, 500, 507, 508]. [cite_start]A 7-segment display provides clear visual feedback for mode selection and status[cite: 411, 471, 472, 473].
* [cite_start]**Safety Features**: A global emergency stop function is available via a dedicated keypad button (`D`) and a Bluetooth command (`X`)[cite: 450, 451, 452, 453, 585, 586]. [cite_start]This feature immediately halts all motors and provides an audible and visual alert[cite: 538, 539, 540, 541, 542, 543, 544].
* [cite_start]**Dynamic Visual Feedback**: A series of LEDs (Green, Red, Blue) provide a welcoming sequence and dynamic light patterns that respond to the robot's current mode and state[cite: 399, 446, 485, 486, 487, 488, 489, 527, 528, 529].

---

## 🛠️ Hardware Requirements

To replicate this project, you will need the following components:
* Arduino Mega 2560 or similar board
* L298N Motor Driver
* 2x DC Motors
* 1x Micro Servo Motor (SG90)
* 1x HC-SR04 Ultrasonic Sensor
* 1x 4x4 Keypad
* 1x 16x2 LCD with I2C Module
* 1x 7-Segment Display
* 1x Buzzer
* LEDs (Red, Green, Blue, White) and resistors
* 1x Potentiometer
* Bluetooth Module (e.g., HC-05)

---

## ⚙️ Installation & Setup

1.  **Libraries**: Install the following Arduino libraries through the Arduino IDE's Library Manager:
    * `LiquidCrystal_I2C`
    * `Servo`
    * `Keypad`
2.  **Wiring**: Follow the pin definitions in the code to connect all components to your Arduino board.
    * [cite_start]**Motors**: ENA (pin 3), ENB (pin 4)[cite: 408].
    * [cite_start]**Servo**: Pin 2[cite: 409].
    * [cite_start]**Ultrasonic Sensor**: TRIG (pin 43), ECHO (pin 44)[cite: 410].
    * [cite_start]**Keypad**: Rows (pins 35-38), Columns (pins 34-30)[cite: 404, 405].
    * [cite_start]**LCD**: I2C (address 0x27)[cite: 413].
3.  **Code Upload**: Open `Final Working Code.txt` in the Arduino IDE and upload it to your board.

---

## 🏃 Usage

[cite_start]Upon startup, the robot will perform a brief welcome sequence[cite: 482]. [cite_start]The LCD will then display a menu[cite: 499]. Use the keypad to select a mode:
* Press **'1'** for **Bluetooth Mode**.
* Press **'2'** for **Maze Mode**.
* Press **'3'** for **Testing Mode**.
* Press **'A'** for **VC Mode**.

[cite_start]**Emergency Stop**: Press **'D'** on the keypad at any time to activate the emergency stop[cite: 450].

---

## 🤝 Contribution

Feel free to fork this repository, add new features, and open a pull request. Your contributions are welcome!
