# 🍽️ Microwave Oven using PIC16F877A

A complete **Embedded Systems project** that simulates the working of a modern **Microwave Oven** using the **PIC16F877A microcontroller**, developed in **Embedded C**, and tested using the **PICSimLab Simulator**.

This project demonstrates real-world appliance automation using:

- Timer Interrupts
- Matrix Keypad Interfacing
- CLCD Display
- Door Safety Detection
- Buzzer Alerts
- Fan Control
- State Machine Logic
- Real-Time Countdown Operations

---

# 📌 Project Overview

A microwave oven is one of the most common real-time embedded systems used in modern homes. It combines multiple hardware peripherals and embedded firmware to provide efficient and safe cooking operations.

This project simulates the core functionalities of a microwave oven including:

- Micro Cooking Mode
- Grill Mode
- Convection Mode
- Temperature Setting
- Pre-heating Process
- Cooking Timer
- Pause/Resume Control
- Door Safety Monitoring
- Fan & Buzzer Control

The firmware is written completely in **Embedded C** with a modular design approach.

---

# 🎯 Objective

The objective of this project is to understand and implement:

- Embedded firmware development
- Real-time timer management
- Interrupt-driven programming
- User input handling
- LCD interfacing
- Appliance automation logic
- State machine implementation
- Safety feature integration

---

# ⚙️ Technologies Used

| Technology | Purpose |
|---|---|
| Embedded C | Firmware Development |
| MPLAB X IDE | Code Development |
| XC8 Compiler | PIC Compilation |
| PIC16F877A | Microcontroller |
| PICSimLab | Hardware Simulation |
| CLCD | Display Interface |
| Matrix Keypad | User Input |
| Timer2 Interrupt | Real-Time Countdown |

---

# 🧠 Features

## ✅ Cooking Modes

### 🔹 Micro Mode
- Standard microwave heating mode
- Displays fixed power level (900W)
- User-configurable cooking time

### 🔹 Grill Mode
- Simulates grilling operation
- Timer-controlled cooking

### 🔹 Convection Mode
- Temperature selection support
- Temperature validation
- Pre-heating simulation
- Cooking time configuration after heating

---

# ⌨️ Keypad Controls

| Key | Function |
|---|---|
| `1` | Micro Mode |
| `2` | Grill Mode |
| `3` | Convection Mode |
| `4` | Start / Resume / Add 30 sec |
| `5` | Pause |
| `6` | Stop |
| `*` | Clear Input |
| `#` | Confirm / Enter |

---

# 🖥️ Hardware Components

| Component | Description |
|---|---|
| PIC16F877A | Main Controller |
| 16x4 CLCD | Display Unit |
| Matrix Keypad | User Input |
| Buzzer | Audio Alert |
| Fan | Cooling Simulation |
| Door Switch | Safety Monitoring |

---

# 🔄 Working Principle

## 1️⃣ Power ON
- System initializes peripherals
- LCD displays startup screen
- Timer and keypad modules become active

---

## 2️⃣ Mode Selection
User selects one of the available cooking modes:

- Micro
- Grill
- Convection

using the matrix keypad.

---

## 3️⃣ Time / Temperature Setup

### Micro & Grill Modes
- User enters cooking time

### Convection Mode
- User sets temperature
- System validates entered temperature
- Pre-heating process starts
- User sets cooking time after pre-heating

---

## 4️⃣ Cooking Process
- Timer interrupt updates countdown every second
- Fan turns ON during operation
- LCD continuously displays remaining time

---

## 5️⃣ Door Safety Detection
If the door opens during cooking:

- Cooking pauses immediately
- Fan turns OFF
- Buzzer activates
- Warning message displayed on LCD

Cooking resumes only after the door is closed.

---

## 6️⃣ Cooking Completion
Once timer reaches zero:

- Cooking stops
- Fan turns OFF
- Buzzer alerts the user
- System returns to idle mode

---

# 🧩 Software Architecture

## 📂 Project Structure

```text
Microwave_Oven/
│
├── main.c                 # Main application logic
├── isr.c                  # Timer interrupt service routine
├── timers.c               # Timer2 initialization
├── clcd.c                 # CLCD driver functions
├── matrix_keypad.c        # Matrix keypad scanning
│
├── main.h                 # Main macros and declarations
├── clcd.h                 # LCD configurations
├── matrix_keypad.h        # Keypad definitions
├── timers.h               # Timer declarations
│
└── README.md
```

---

# ⏱️ Timer Interrupt Logic

The project uses **Timer2 Interrupt** for real-time countdown management.

### Responsibilities of ISR
- 1-second delay generation
- Minute and second decrement
- Cooking completion handling

This demonstrates:
- Interrupt-driven programming
- Real-time embedded system design

---

# 🛡️ Safety Features

## ✅ Door Detection
Cooking automatically pauses when the door opens.

## ✅ Temperature Validation
Convection temperature limited to 250°C maximum.

## ✅ Controlled Resume
Cooking resumes safely after user interaction.

---

# 📺 LCD Display Screens

The CLCD displays:

- Startup animation
- Mode selection menu
- Cooking timer
- Temperature settings
- Pre-heating status
- Door warning alerts
- Cooking completed message

---

# 🔍 Embedded Concepts Used

- Embedded C Programming
- Timer Interrupts
- GPIO Interfacing
- Matrix Keypad Scanning
- LCD Interfacing
- State Machine Design
- Appliance Automation
- Human Machine Interface (HMI)
- Real-Time Countdown Logic

---

# 🚀 How to Run the Project

## 🔧 Requirements

- MPLAB X IDE
- XC8 Compiler
- PICSimLab Simulator

---

## ▶️ Steps to Execute

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/Smart-Microwave-Oven-PIC16F877A.git
```

### 2️⃣ Open Project
Open the project in **MPLAB X IDE**

### 3️⃣ Build the Project
Compile the project using **XC8 Compiler**

### 4️⃣ Load HEX File
Load the generated `.hex` file into **PICSimLab**

### 5️⃣ Run Simulation
Start simulation and test all microwave functionalities

---

# 📸 Recommended GitHub Screenshots

Add screenshots for:

- Startup Screen
- Mode Selection Menu
- Cooking Timer Running
- Convection Temperature Setup
- Door Open Warning
- Cooking Completion Screen
- PICSimLab Hardware Setup

---

# 📈 Learning Outcomes

This project helped in understanding:

- Real-time embedded application design
- PIC microcontroller programming
- Timer interrupt handling
- Peripheral interfacing
- Modular firmware architecture
- Embedded simulation and debugging
- User interface implementation

---

# 🌟 Future Enhancements

- EEPROM-based memory storage
- RTC integration
- Adjustable power levels
- PWM-based heating simulation
- Temperature sensor integration
- IoT monitoring support
- Touch keypad interface

---

# 👨‍💻 Author

Developed using:

- Embedded C
- PIC16F877A
- MPLAB X IDE
- XC8 Compiler
- PICSimLab Simulator

---

# ⭐ Support

If you found this project useful:

- ⭐ Star the repository
- 🍴 Fork the project
- 🛠️ Contribute improvements
- 📢 Share feedback

---
