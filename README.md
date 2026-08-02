# Bluetooth Controlled Arduino Uno Robot

A simple Bluetooth-controlled robot built using an Arduino Uno, HC-05 Bluetooth module, and L298N Motor Driver.

The robot is controlled through an Android application that sends commands via Bluetooth to the Arduino, allowing forward, backward, left, right, and diagonal movements.

---

## Features

- Bluetooth control using HC-05
- Android App based controller
- Forward, Backward, Left, Right movement
- Diagonal movement support
- Easy to build
- Beginner friendly project

---

## Components Required

| Component | Quantity |
|-----------|----------|
| Arduino Uno | 1 |
| HC-05 Bluetooth Module | 1 |
| L298N Motor Driver | 1 |
| DC Motors | 4 |
| Wheels | 4 |
| Castor Wheel | 1 |
| Chassis | 1 |
| Battery Pack (7V-12V) | 1 |
| Jumper Wires | As required |

> Depending on the application, either BO motors or Metal Gear Motors can be used. Choose the motors based on the required speed and torque.

---

## Folder Structure

```
Arduino_Code/
Android_App/
Circuit_Diagram/
```

---

## Wiring

The complete wiring diagram is available inside the **Circuit_Diagram** folder.

---

## Pin Configuration

| Arduino Pin | Connected To |
|-------------|--------------|
| D9 | IN1 (L298N) |
| D10 | IN2 (L298N) |
| D11 | IN3 (L298N) |
| D12 | IN4 (L298N) |

HC-05 Connections

| HC-05 | Arduino |
|--------|----------|
| TX | RX |
| RX | TX (Recommended through voltage divider) |
| VCC | 5V |
| GND | GND |

---

## Bluetooth Commands

| Command | Movement |
|----------|----------|
| B | Forward |
| F | Backward |
| L | Right |
| R | Left |
| G | Forward Left |
| I | Forward Right |
| H | Backward Left |
| J | Backward Right |
| S | Stop |

---

## Arduino Program

The Arduino continuously listens for serial data from the HC-05 Bluetooth module.

Each received character corresponds to a movement command.

Example:

```
B -> Forward
F -> Backward
L -> Right
R -> Left
S -> Stop
```

The motors are controlled using the L298N Motor Driver by setting the appropriate output pins HIGH or LOW.

---

## Android Application

Install the APK available in the **Android_App** folder.

Steps:

1. Turn ON Bluetooth.
2. Pair with HC-05.
3. Open the application.
4. Connect to HC-05.
5. Control the robot.

---

## Uploading the Code

1. Open Arduino IDE.
2. Open `Bluetooth_Robot.ino`.
3. Select Arduino Uno.
4. Select the correct COM Port.
5. Upload.
6. Disconnect USB.
7. Connect HC-05.
8. Power the robot.

---

## Future Improvements

- PWM speed control
- Obstacle avoidance
- Line follower mode
- Voice control
- WiFi control using ESP8266
- Mobile app improvements

---

## License

This project is released under the MIT License.

---

## Author

Your Name

GitHub:
