---
title: "Task1: Servo Default Movements"
layout: default
nav_order: 11
parent: Lab2 - Signals to Speed
---

# Task1 – Servo Default Movements

---

## Brief

In this task, you’ll move a servo motor in **TinkerCAD** through a simple pattern:  
0°, 90°, 180°, then back to 0°, repeating endlessly.  

This introduces the **Servo library** and how PWM signals translate to angle control.

---

## Objectives
- Learn how to include and use the Arduino **`<Servo.h>`** library  
- Understand how servo signals correspond to movement  
- Create a repeatable motion pattern  

---

## Equipment
- TinkerCAD account  
- x1 Arduino Uno (virtual)  
- x1 Servo (9g or similar) 

---

## Step 1 – Set Up the Circuit
1. In TinkerCAD → Circuits, create a new project.  
2. Add an **Arduino Uno R3** and a **servo motor**.  
3. Wire the servo:  
   - **Signal** (yellow/orange) → pin 9  
   - **VCC** (red) → 5 V  
   - **GND** (black/brown) → GND  
4. Open *Code → Text* to switch to text mode.  

---

## Step 2 – Write the Program

```cpp
#include <Servo.h>  

Servo myServo;  

void setup() {  
    myServo.attach(9);  // connect servo to pin 9  
}  

void loop() {  
    myServo.write(0);  
    delay(1000);  
    myServo.write(90);  
    delay(1000);  
    myServo.write(180);  
    delay(1000);  
    myServo.write(0);  
    delay(1000);  
}  
```

---

## Step 3 – Simulate
Click **Start Simulation**.  
The servo horn should sweep to 0°, pause, then 90°, 180°, and back to 0°.  

{: .troubleshooting }
> If it doesn’t move:  
> - Check the servo’s signal wire is on `pin 9`.  
> - Ensure you used `.attach(9)` in the code.  
> - Give it a moment - TinkerCAD’s simulation can lag slightly.  

---

## Step 4 – Modify and Explore
Try some quick changes such as altering the delay or angles to see how the servo responds.

{: .challenge}
Try set an angle beyond 180º. What happens? Why?

<!-- {: .challenge-title}
> 💪 Challenge 1  
> - Change the delay times to speed up or slow down the motion.  
> - Reverse the order (180 → 90 → 0) to test direction.  
> - Add intermediate angles like 45° and 135°.  
> - Use `Serial.println(angle);` to print each angle to the Serial Monitor.   -->

You’ve just created a programmed motion loop - the foundation for every robot that follows orders without complaining.  
{: .think }
