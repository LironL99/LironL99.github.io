# Ultrasonic Sensor Servo Control Project 🚀

## Table of Contents
1. [Project Overview](#project-overview)
2. [Components Used](#components-used)
3. [Wiring Diagram](#wiring-diagram)
4. [Code Explanation](#code-explanation)
5. [Integration of Components](#integration-of-components)
6. [Project Functionality](#project-functionality)
7. [Future Improvements](#future-improvements)
8. [Conclusion](#conclusion)

## Project Overview
This project aims to create a distance measurement system using an ultrasonic sensor and a servo motor, providing visual feedback through red LEDs based on the measured distance. Additionally, it features a radar-like display using Processing, which visually represents the distance readings in real time. The system allows users to adjust the scanning speed via a potentiometer. This was my first independent project (besides digital circuits labs), where I enhanced my skills in wiring, using a breadboard, integrating components, debugging, and interfacing with a microcontroller. I also gained experience in programming within the Arduino IDE environment using C++.

## Components Used
- **Arduino UNO R3**: A popular microcontroller board based on the ATmega328P.
  - **Advantages of Arduino**:
    - **User-Friendly**: Easy to program using the Arduino IDE.
    - **Versatile**: Compatible with a wide range of sensors, motors, and other components.
    - **Large Community**: Extensive community support provides resources and tutorials.
    - **Affordable**: Cost-effective for hobbyists and students.

- **Ultrasonic Sensor (HC-SR04)**: Used for measuring distance. It sends ultrasonic pulses and calculates the time it takes for them to return.

- **Servo Motor (SG90)**: A small servo motor that rotates between specified angles to scan the environment.

- **Potentiometer (B10K)**: A variable resistor allowing users to adjust the scanning speed of the servo motor.

- **Red LEDs**: Provide visual feedback about the distance to an object.

- **Processing Environment**: Used to create a radar-like visual display that represents the measured distance in real time.

## Wiring Diagram
![Wiring Diagram](/Arduino-Projects/Sonar_Servo_Project/Wiring-Diagram.png)

## Code Explanation
The provided code utilizes various components to create a distance measurement and feedback system using an ultrasonic sensor, servo motor, potentiometer, LEDs, and a Processing display. Below is a breakdown of how these components work together.

### 1. Component Initialization
- **Servo Motor (SG90)**: Controlled via a PWM-capable digital pin.
- **Ultrasonic Sensor (HC-SR04)**: Connected to pins 7 and 8 (trigPin and echoPin) to measure distance.
- **Potentiometer (B10K)**: Connected to analog pin A0 to control the delay time between servo movements.
- **Red LEDs**: Connected to pins 10, 11, and 12 to provide visual feedback.

### 2. Main Functionality
- The **`setup()`** function initializes the pins for input and output.
- The **`loop()`** function continuously reads the potentiometer value, maps it to a delay time, and moves the servo motor.

### 3. Moving the Servo
The **`moveServo()`** function handles the movement of the servo motor.

### 4. Distance Measurement
The **`calculateDistance()`** function uses the HC-SR04 to measure the distance to an object.

### 5. LED Control Logic
The **`ledControl()`** function controls the state of the red LEDs based on the distance measured.

### 6. Processing Display
The Processing sketch provides a radar-like visualization of the distance readings.

## Integration of Components
This project successfully integrates the components to perform the following tasks:
- Measure distance using the HC-SR04 sensor and adjust the position of the SG90 servo motor.
- Use a potentiometer to adjust the scanning speed of the servo motor.
- Provide visual feedback through red LEDs.

## Project Functionality
![Project Functionality](/Arduino-Projects/Sonar_Servo_Project/Project_Functionality_GIF.gif)
- [**Full Demonstration (HQ)**](/Arduino-Projects/Sonar_Servo_Project/Project_Functionality.mp4)

## Future Improvements
Future iterations could include:
- Integrating an LCD display.
- Adding a buzzer for audio feedback.
- Enhancing the LED control logic.
- Improving the Processing visualization.

## Conclusion
This project demonstrates the integration of an ultrasonic sensor, servo motor, potentiometer, LEDs, and a radar-like Processing display. The experience gained from tackling the challenges and implementing the components will serve as a solid foundation for future projects, particularly in the VLSI field.
