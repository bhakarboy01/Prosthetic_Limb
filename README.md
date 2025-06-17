# Prosthetic Limb Using Flex Sensors and 3D Printed Hand

##  Project Overview

This project showcases a functional, low-cost **prosthetic limb** system that mimics the motion of a human hand using **flex sensors** and **servo motors**. The system is controlled by a glove equipped with flex sensors worn by a user, and actuates a 3D printed robotic hand in real-time.

Flexing a finger on the glove causes the corresponding finger on the prosthetic hand to move with a similar bend. This is achieved using an Arduino microcontroller, servo motors, and nylon thread-based tendon mechanisms.

---

## How It Works

1. **User wears a glove** embedded with 5 flex sensors — one on each finger.
2. **Flex sensors** detect bending motion and send analog signals to the **Arduino**.
3. The Arduino (programmed with `main.ino`) interprets sensor values and maps them to servo angles.
4. **Servo motors** inside the 3D printed arm pull strings connected to each robotic finger.
5. This enables **real-time finger movement replication** on the prosthetic hand.

---

## 3D Printed Parts

The hand is composed of multiple articulated components, all of which are 3D printable:

| File Name        | Part Description                   |
|------------------|------------------------------------|
| `arm.stl`        | Main arm housing (servo container) |
| `arm_cover.stl`  | Protective cover for the arm       |
| `hand_left.stl`  | Left hand base                     |
| `hand_right.stl` | Right hand base (optional variant) |
| `f_thumb.stl`    | Thumb finger                       |
| `f_index.stl`    | Index finger                       |
| `f_middle.stl`   | Middle finger                      |
| `f_ring.stl`     | Ring finger                        |
| `f_baby.stl`     | Little (pinky) finger              |

Images of the assembled model can be found in the [`Images/`](./Images) directory.

---

## Hardware Required

- **Arduino Uno / Nano**
- **5x Flex Sensors**
- **5x Servo Motors** (e.g., SG90 or MG90S)
- Nylon thread (for finger actuation)
- 3D Printed parts (STL files listed above)
- Glove (to mount flex sensors)
- Jumper wires, resistors (for voltage dividers)
- Breadboard and power supply

---

## Setup Instructions

1. **Print and Assemble** all STL parts.
2. Mount **servo motors** inside the `arm.stl` housing and secure using `arm_cover.stl`.
3. Use **nylon thread** to connect servos to each finger joint (via eyelets or holes in finger STL models).
4. Attach **flex sensors** to the glove over finger joints and connect them to analog pins on the Arduino.
5. Connect servos to PWM digital pins.
6. Upload the provided code file `main.ino` to the Arduino via the Arduino IDE.
7. Power on the setup and observe the robotic hand replicate human finger motions.

---


