UART Polling Based Communication on LPC2129

UART (Universal Asynchronous Receiver/Transmitter) communication implemented on the LPC2129 ARM7 microcontroller using the polling method in Embedded C.


---

Overview

This project demonstrates UART serial communication on the LPC2129 microcontroller using a polling-based approach without interrupts.

The implementation includes UART initialization, data transmission, and data reception functionalities for serial communication between the LPC2129 and external devices such as PCs, terminals, or other microcontrollers.

The project is developed using Embedded C and direct register-level programming.


---

Features

UART initialization on LPC2129

Polling-based UART communication

Serial data transmission

Serial data reception

Register-level peripheral access

Lightweight embedded implementation

ARM7 LPC2129 microcontroller support



---

Technologies Used

Embedded C

LPC2129 ARM7 MCU

UART Protocol

Keil µVision

Flash Magic



---

Repository Structure

.
├── Driver_code/
│   ├── lpc2129_REGACC.h
│   ├── lpc2129_main.c
│   ├── lpc2129_uart.c
│   └── lpc2129_uart.h
│
├── README.md


---

File Description

lpc2129_REGACC.h

Contains register access macros and memory-mapped register definitions for LPC2129 peripheral configuration.

lpc2129_uart.h

Header file containing UART function declarations and configuration definitions.

lpc2129_uart.c

Implements UART driver functions including:

UART initialization

Transmit character

Receive character

String transmission


lpc2129_main.c

Main application file demonstrating UART communication using polling.


---

UART Polling Concept

In polling-based UART communication, the processor continuously checks UART status flags to determine whether:

data has been received

transmission buffer is ready


Unlike interrupt-based communication, polling does not rely on ISR execution.


---

Working Principle

1. Initialize UART peripheral


2. Configure baud rate and frame format


3. Poll UART status registers


4. Transmit and receive serial data


5. Display/output received information




---

Example Functionalities

Send characters over serial terminal

Receive serial input from PC

Echo received characters back to terminal

Serial debugging support



---

UART Configuration

Parameter	Value

Baud Rate	9600
Data Bits	8
Stop Bits	1
Parity	None



---

Development Environment

Hardware

LPC2129 Development Board

USB to UART Converter


Software

Keil µVision

Flash Magic

Serial Terminal (PuTTY/Tera Term)



---

Build and Flash

Compile Using Keil

1. Open project in Keil µVision


2. Build the project


3. Generate HEX file



Flash to LPC2129

1. Connect LPC2129 board


2. Open Flash Magic


3. Select generated HEX file


4. Flash program to MCU




---

Sample Output

UART Initialized
Sending Data...
Hello from LPC2129 UART


---

Applications

Serial debugging

Embedded communication systems

Sensor interfacing

Bootloader communication

Industrial embedded systems



---

Future Improvements

Interrupt-based UART communication

FIFO support

DMA integration

RS485 communication

Multi-UART support



---

Author

Kavya B Ramasali 


---

License

This project is licensed under the MIT License.
