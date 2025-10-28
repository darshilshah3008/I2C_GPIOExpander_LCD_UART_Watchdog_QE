# I2C GPIO Expander + LCD + UART + Watchdog + Quadrature Encoder

This project demonstrates an embedded system integrating multiple peripheral interfaces, including:
- **MCP23008 I²C GPIO expander**
- **I²C character LCD**
- **UART command interface**
- **Watchdog supervision**
- **Quadrature encoder (QE) reading**

The system provides a flexible platform for monitoring, displaying, and interacting with GPIO and encoder signals, while maintaining functional safety through watchdog operation.

---

## ✅ Features

- Control and expand GPIO using **MCP23008 (I²C)**
- Display messages, values, and status on an **I²C LCD**
- Receive commands via **UART**
- Read position data from a **Quadrature Encoder**
- **Watchdog** implementation for safe operation
- Easily extendable/portable driver structure

---

## 🔌 System Overview

| Module | Description |
|--------|-------------|
| I²C GPIO Expander | Adds 8 extra GPIO pins (configurable as input or output) |
| LCD (I²C) | Displays data such as encoder position or GPIO states |
| UART | Provides user command interface |
| Quadrature Encoder | Provides real-time rotation/position feedback |
| Watchdog Timer | Resets MCU on software hang |
| MCU | Coordinates all modules |

The firmware initializes I²C devices, configures GPIO, captures encoder events, and displays information over the LCD while responding to external user control via UART.

---

## 🧠 Software Highlights

- Modular architecture with separate drivers for:
  - I²C
  - LCD
  - MCP23008 GPIO expander
  - Encoder capture
  - UART parsing
- Debouncing + signal filtering for encoder
- Non-blocking UART command handling
- Periodic watchdog feed

---

## 🛠 Hardware Requirements

- MCU with UART + I²C support
- MCP23008 I²C GPIO Expander
- I²C 16×2 or 20×4 LCD
- Quadrature Encoder
- UART terminal (PC)
- Optional: Pull-ups on encoder signals

---

## 📁 Repository Structure (Example)

/
├── src/
│ ├── lcd/
│ ├── gpio_expander/
│ ├── uart/
│ ├── qe/
│ ├── watchdog/
│ └── main.c
├── docs/
└── README.md

yaml
Copy code

---

## 🚀 Getting Started

1) Connect MCP23008 + LCD to MCU over I²C  
2) Connect encoder signals to MCU capture pins  
3) Flash firmware  
4) Open UART terminal  
5) Interact using text commands  

---

## ✅ Typical Use Cases

- Encoder position display on LCD
- GPIO remote monitoring + control over UART
- Safety-critical demo with watchdog reset
- Modular I²C control demo

---

## 🔮 Future Enhancements

- Store configuration in EEPROM
- Support for additional I²C expanders
- On-screen menus on LCD
- UART CLI enhancements

