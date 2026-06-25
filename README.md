# Ultrasonic Radar System using AT89S52

## Overview

This project implements an ultrasonic distance measurement and proximity warning system using the AT89S52 (8051-family) microcontroller. The system measures object distances using an HC-SR04 ultrasonic sensor, displays live readings on a 16×2 LCD, and provides visual and audible feedback through LEDs and a buzzer.

The project was developed as part of a Microprocessors course and programmed entirely in Assembly Language.

## Features

* Distance measurement from 2 cm to 200 cm
* Real-time LCD display
* Three-level LED indication system
* Audible warning for critical proximity
* LCD anti-flicker optimization
* Assembly-language implementation
* 4-bit LCD interface

## Hardware Components

* AT89S52 Microcontroller
* HC-SR04 Ultrasonic Sensor
* 16×2 LCD Display
* Green LED
* Yellow LED
* Red LED
* Active Buzzer
* 11.0592 MHz Crystal Oscillator
* Arduino UNO (ISP Programmer)

## System Logic

1. Generate a 10 µs trigger pulse.
2. Measure the ECHO pulse width using Timer 0.
3. Convert the measured time to distance using:

Distance (cm) = Echo Pulse Width (µs) / 58

4. Update the LCD when the value changes.
5. Control LEDs and buzzer according to distance thresholds.

## Feedback Logic

| Distance | Green | Yellow | Red | Buzzer |
| -------- | ----- | ------ | --- | ------ |
| > 30 cm  | ON    | OFF    | OFF | OFF    |
| 20–30 cm | OFF   | ON     | OFF | OFF    |
| 10–20 cm | OFF   | OFF    | ON  | OFF    |
| < 10 cm  | OFF   | OFF    | ON  | ON     |

## Software Tools

* Assembly Language
* ASEM-51 Assembler
* AVRDUDE
* ArduinoISP

## Key Learning Outcomes

* 8051 Microcontroller Programming
* Timer-Based Measurements
* Sensor Interfacing
* LCD Communication in 4-bit Mode
* Embedded System Debugging
* Real-Time Hardware Control

## Results

The system successfully:

* Measured distances from 2 cm to 200 cm
* Displayed live readings on the LCD
* Provided visual status indication
* Activated audible alerts for critical distances
* Achieved reliable operation with low measurement error

## Team

Ahmed Elsayed
Marwan Hossam
Ahmed Gamal

Teaching Assistant: Eng. Zeyad Eldamarawy

## Repository Contents

/code      → Assembly source code
/docs      → Project report


