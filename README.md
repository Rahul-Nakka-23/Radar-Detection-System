# Radar-Detection-System

This project demonstrates the implementation of an ultrasonic radar system using an Arduino microcontroller, a servo motor, and an ultrasonic sensor. The radar's data is visualized in real-time using Processing.

---

## Project Features
1. **Arduino Code:**
   - Controls a servo motor to rotate the ultrasonic sensor.
   - Measures distance using an ultrasonic sensor.
   - Sends angle and distance data to the serial port.

2. **Processing Code:**
   - Visualizes radar sweeps and detected objects in a graphical interface.
   - Displays real-time angle and distance readings.
   - Indicates whether objects are "In Range" or "Out of Range."

---

## Hardware Requirements
- Arduino Uno (or compatible)
- Ultrasonic Sensor (HC-SR04)
- Servo Motor (e.g., SG90)
- Connecting Wires
- Breadboard
- USB Cable for Arduino
- Computer with Arduino IDE and Processing installed

---

## Arduino Setup
1. **Connections:**
   - Ultrasonic Sensor:
     - VCC → Arduino 5V
     - GND → Arduino GND
     - Trig → Pin 10
     - Echo → Pin 11
   - Servo Motor:
     - Signal → Pin 12
     - Power and GND → Appropriate sources (ensure adequate power supply)

2. **Arduino Code:**
   - Upload the provided Arduino code using the Arduino IDE.
   - Ensure the correct COM port and board type are selected in the IDE.

---

## Processing Setup
1. **Environment:**
   - Install the Processing IDE.
   - Add the `serial` library if not pre-installed (usually included by default).

2. **Code Configuration:**
   - Update the serial port in the line:
     ```java
     myPort = new Serial(this, "COM5", 9600);
     ```
     Replace `"COM5"` with the appropriate port for your Arduino.

3. **Screen Resolution:**
   - Adjust the `size()` function in the `setup()` method for your screen resolution.

4. **Run the Code:**
   - Start the Processing sketch. The radar visualization will begin.

---

## Functionality
### Arduino Code:
- **Servo Sweep:** 
  - The servo sweeps from 15° to 165° and back.
- **Distance Measurement:**
  - Measures distance to objects using the ultrasonic sensor.
  - Sends angle and distance data over the serial port.

### Processing Code:
- **Radar Visualization:**
  - Simulates a radar screen with arcs and angle lines.
  - Displays detected objects as red points.
- **Real-Time Data:**
  - Updates angle and distance readings dynamically.
  - Displays whether objects are "In Range" (distance ≤ 40 cm).

---

## Notes
1. **Range Limitation:**
   - The radar system is configured to detect objects up to 40 cm away.
   - Adjust the `if` condition in the Processing code for a different range.

2. **Dependencies:**
   - Ensure a stable serial connection between Arduino and the computer.
   - Use proper power supply for the servo motor.

3. **Troubleshooting:**
   - Verify hardware connections and upload the Arduino code correctly.
   - Check the serial port configuration in the Processing code.

---

