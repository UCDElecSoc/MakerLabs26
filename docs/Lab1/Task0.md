---
title: Task0 - Setup
layout: default
parent: Lab1 - RGB Controllers
nav_order: 2
---
# Setting up the circuit
But first, we gotta get basic.

## Ingredients:
  - Arduino Uno
  - RGB LED with common anode configuration
  - 330Ω resistor
  - Breadboard
  - Jumper cables

## Circuit
- 5V of Arduino Uno to the resistor
- Connect the other end of resistor to common anode of LED
- Connect the other pins of the LED to the Arduino digital pins
  - RED -> `pin 3`
  - GREEN -> `pin 5`
  - BLUE -> `pin 6`


## Arduino IDE
You can use:
- Lab computers
- Arduino Cloud
- Install Arduino IDE on your laptop

## Test your Arduino is working
- Go to `File` > `Examples` > `01.Basic` > `Blink`
- Select the correct COM Port
- Upload the file to your arduino

You should see the onboard LED blinking. 
*(If not, please let one of the robotics officers know)*