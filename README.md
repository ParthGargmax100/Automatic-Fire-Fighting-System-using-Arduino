# Automatic-Fire-Fighting-System-using-Arduino
An autonomous Arduino-based fire-fighting system. It uses a servo-mounted IR flame sensor to continuously sweep the area. Upon detecting a fire, it locks onto the exact angle and triggers a targeted water pump to extinguish it, automatically resetting once clear.
Overview
This project aims to design and implement an automatic fire fighting system that detects fire using a flame sensor and extinguishes it automatically without human intervention. Built around an Arduino UNO, the system utilizes a servo-mounted infrared flame sensor to continuously sweep and monitor its surroundings, expanding its detection range. When a fire is detected, a secondary servo aims a water nozzle at the specific angle, and a relay triggers a water pump to neutralize the flame. This automated setup is highly suitable for preventing fire hazards in small-scale environments like homes, labs, and industries.

Key Features
Active Area Scanning: The flame sensor is mounted on a servo motor, which increases its detection angle range by continuously monitoring its surroundings.  
Precision Targeting: The output water pipe is mounted on a second servo motor, allowing the system to point water directly at the exact angle where the fire is detected.  
Autonomous Operation: Upon detecting a sudden rise in infrared radiation, the Arduino immediately activates the relay to spray water. Once the flame is extinguished, the system automatically turns off the pump and resets for the next detection cycle.  
Fast Detection: The infrared receiver diode is sensitive to 760 nm to 1100 nm wavelengths and features a fast response time of less than 15 ms

Hardware Required
Arduino UNO   
Flame Sensor (3-Pin)   
2x Servo Motors   
Relay Module   
Water Pump   
12V DC Power Supply   
Breadboard  
Connecting Wires

Working Principle
The system operates on the principle of infrared light detection, identifying the presence of fire by sensing the infrared (IR) radiation emitted from the flame.  
When no fire is present, the sensor output remains LOW.  
As soon as a flame appears within the detection range (up to 100 cm, depending on flame size), the sensor sends a HIGH signal to the Arduino input pin.  
The Arduino executes its programmed response by locking the aiming servo to the detected angle and activating the relay module to switch ON the water pump.  
As long as the flame is detected, the pump remains ON. Once extinguished, the sensor output returns to LOW, the pump shuts off, and the sweeping cycle resumes. 
