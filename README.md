# Interactive Attendance Management System

This project is an **Arduino-based attendance management interface** that allows users to record attendance securely using a **keypad passcode system**. The system provides real-time feedback through an **LCD screen and LED indicator**, making the attendance marking process simple, efficient, and error-free.

## 📌 Features

- 🔢 **Passcode Entry using 4×4 Keypad**
- 👤 **User Identity Verification**
- 💡 **LED Feedback**
  - Solid ON = Valid Passcode  
  - Blinking = Invalid Passcode
- 🖥 **Real-time LCD Display**
- ⏱ **Input Timeout (5 seconds)**
- 📊 **Attendance Tracking**
  - Counts Present & Absent users dynamically
- 🔐 **Incorrect Passcode Warning**
- ✨ **Scalable User Database Support**


## 🧰 Components Used

| Component | Quantity |
|----------|----------|
| Arduino (UNO/Nano/Mega) | 1 |
| 4×4 Matrix Keypad | 1 |
| 16×2 LCD Display | 1 |
| LED + 220Ω Resistor | 1 |
| Jumper Wires | Required |
| Breadboard | Optional |



## ⚙️ Circuit Wiring Summary

- **Keypad** → Arduino Pins **2–9**
- **LCD (4-bit mode)** → Pins **10–15**
- **LED Indicator** → Pin **16**
- Potentiometer used for LCD contrast control
- All GND and VCC(5V) connections shared via breadboard


## 🧠 System Workflow

1. System prompts user: **"Enter Passcode"**
2. User enters a 4-digit code.
3. Press `#` to submit or `*` to clear.
4. System checks:
   - If match found → Mark **Present**
   - Else → Show **Invalid ID**
5. Attendance counters update on screen.
6. After 5 seconds of inactivity, the input resets.



## 🧪 Code Structure

| Section | Description |
|---------|-------------|
| `User struct` | Stores username and passcode |
| `Keypad input handling` | Captures and builds entry |
| `Validation logic` | Compares to stored data |
| `LCD display updates` | Shows real-time feedback |
| `Timeout mechanism` | Clears stale input |



## 📁 Repository Contents

