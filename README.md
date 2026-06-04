# Real-Time-Electric-Vehicle-Dashboard
Developed a real-time Electric Vehicle monitoring dashboard using STM32 Blue Pill, PICSimLab, and Python. ADAS (Advanced Driver Assistance System) features include collision and blind-spot detection. The system monitors speed, battery SOC, range, and motor temperature, providing live UART-based visualization, alerts, and drive mode control

# 🚗 EV ADAS Dashboard System

Real-time Electric Vehicle (EV) Monitoring and Advanced Driver Assistance System (ADAS) using STM32F103C8T6 Blue Pill, PICSimLab, HC-SR04 Ultrasonic Sensors, and a Python Dashboard. The system provides live EV telemetry, collision detection, blind-spot monitoring, parking assist, fault management, and UART-based dashboard visualization.

## ✨ Features

### EV Monitoring
- Real-time speed monitoring
- Battery State of Charge (SOC) estimation
- Remaining range prediction
- Motor torque and power monitoring
- Motor temperature monitoring
- ECO, NORMAL, and SPORT drive modes

### ADAS Features
- Forward collision warning
- Time-To-Collision (TTC) calculation
- Left and right blind-spot detection
- Parking assist mode
- Multi-level alarm system

### Safety & Fault Management
- Motor over-temperature protection
- Low SOC protection
- Collision-critical fault handling
- Watchdog monitoring
- Safe-state transition
- PWM motor shutdown during faults

### Dashboard
- Live UART telemetry streaming
- Speedometer gauge
- SOC and range display
- ADAS bird-eye visualization
- Blind-spot indicators
- Warning and fault alerts



## 🛠 Hardware Used

- STM32F103C8T6 Blue Pill
- 3 × HC-SR04 Ultrasonic Sensors
- Passive Buzzer
- Status LEDs
- Potentiometers (Simulation Inputs)
- ST-Link V2


## 💻 Software & Tools

- STM32CubeIDE
- STM32 HAL Drivers
- PICSimLab
- Python
- PySerial
- Matplotlib



## 🏗 System Architecture

HC-SR04 Sensors → STM32 Blue Pill → ADAS & EV Control Logic → UART → Python Dashboard



## 🚘 Vehicle States

- PARKED
- READY
- DRIVING
- REGEN
- FAULT


## ⚠ Alarm Levels

| Level | Description |
|---------|-------------|
| P0 | Normal |
| P1 | Critical Collision |
| P2 | Collision Warning |
| P3 | Blind Spot / Advisory |



## 📊 Telemetry Parameters

### EV Metrics
- Speed (km/h)
- SOC (%)
- Torque (Nm)
- Power (kW)
- Range (km)
- Motor Temperature (°C)
- Drive Mode
- Uptime

### ADAS Metrics
- Front Distance
- Left Distance
- Right Distance
- Collision Level
- Blind Spot Status
- TTC (Time-To-Collision)



## 📡 UART Communication

- Baud Rate: 115200
- Protocol: UART
- EV Metrics Packet (0x01)
- ADAS Alerts Packet (0x02)
- Vehicle State Packet (0x03)
- Status/ACK Packet (0x04)




## 📈 Performance

- Control Loop < 5 ms
- Sensor Polling = 100 ms
- Dashboard Refresh = 10 Hz
- UART Latency < 10 ms
- Fault Response ≤ 10 ms



## 📂 Project Structure


EV_ADAS_Dashboard/
│
├── Core/
│   ├── ev_control.c
│   ├── adas.c
│   ├── ultrasonic.c
│   ├── fault.c
│   ├── uart_shell.c
│   └── buzzer.c
│
├── Dashboard/
│   ├── dashboard.py
│   └── telemetry_parser.py
│
├── Docs/
│   └── Requirements_Design_Document.pdf
│
└── README.md



## 🎯 Applications

- Electric Vehicle Monitoring
- ADAS Development
- Automotive Embedded Systems
- Real-Time Telemetry Systems
- Embedded Firmware Training
- Automotive Safety Research
