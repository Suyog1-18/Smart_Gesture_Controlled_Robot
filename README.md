# 🤖 Smart Gesture Controlled Robot Car

This project demonstrates a **gesture-controlled robotic car** built using Arduino, self-coded embedded logic, and wireless communication. By integrating an **accelerometer**, **RF modules**, **motor driver**, and **ultrasonic sensor**, the robot responds to natural hand gestures for movement and features real-time obstacle detection and speed monitoring.

---

## 🔧 Hardware Components

### 🖐 Transmitter Module (Glove)
- Arduino Uno  
- Accelerometer (MPU6050)  
- RF Transceiver (nRF24L01)  
- Glove (for mounting the sensor)

### 🚗 Receiver Module (Car)
- Arduino Uno  
- RF Transceiver (nRF24L01)  
- Motor Driver (L298N)  
- DC Motors (x4)  
- Ultrasonic Sensor  
- LCD Display (16x2)  
- Buzzer  
- 9V Battery

---

## ⚙️ Working Principle

1. **Gesture Detection:**  
   MPU6050 detects X and Y tilt values based on hand movements.

2. **Wireless Communication:**  
   The glove sends directional commands via nRF24L01 to the car.

3. **Movement & Control:**  
   The car receives the command, controls motors via L298N, and displays speed on the LCD.

4. **Obstacle Avoidance:**  
   Ultrasonic sensor detects objects ahead and halts movement, triggering a buzzer alert.

---

## 🧠 Key Features
- Gesture-based control using accelerometer
- Wireless transmission via nRF24L01
- Real-time obstacle detection with buzzer warning
- Speed display using 16x2 LCD
- Modular architecture with clean separation between control and actuation units

---

## 🛠 Challenges & Solutions
- **Sensor Fluctuation:** Applied moving average filter and gesture thresholds  
- **Signal Delay:** Reduced transmission rate and used unique RF addresses  
- **Obstacle Response Lag:** Implemented non-blocking sensor reads using timers  
- **Faulty Components:** Diagnosed and replaced to maintain system stability

