# Dual-Mode Autonomous Vehicle Prototype

An embedded robotics system supporting intelligent autonomous obstacle avoidance and dynamic manual override via serial commands (NodeMCU/ESP8266 interface).

### Key Features
- **Dual Operational Modes:** Smooth toggle between Auto Navigation and Manual Override via Serial commands (`AUTO`, `MANUAL`, `F`, `B`, `L`, `R`, `S`).
- **Look-Ahead Ultrasonic Scanning:** Servo-mounted HC-SR04 executes 180° sweeps (150° Left vs. 30° Right) to determine optimal path clearance upon threshold breach.
- **Sensor Noise Filtering:** Implemented a software 5-sample averaging filter to eliminate ultrasonic jitter and false obstacle detection.
- **Fail-Safe Mechanism:** Automatically defaults to autonomous collision avoidance if serial command link is interrupted.

### Hardware Stack
- **Microcontroller:** Arduino / Microchip ATmega328P
- **Wireless/Interface:** NodeMCU (ESP8266) via Hardware Serial (9600 baud)
- **Actuators:** L298N Dual H-Bridge Motor Driver, Micro Servo Motor (SG90)
- **Sensors:** Ultrasonic Sensor (HC-SR04)
- **Language/Framework:** Embedded C / C++ (Arduino Core)
