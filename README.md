# UART Transmitter on VSDSquadron FPGA Mini Board

This project demonstrates the implementation of a Verilog-based UART transmitter on the VSDSquadron FPGA Mini board. The design uses the internal high-frequency oscillator (SB_HFOSC), a frequency counter, and a baud rate generator to transmit a fixed ASCII character (“D”) serially to a PC or any UART-compatible device. The UART follows the **8N1 format (8 data bits, no parity, 1 stop bit) at a baud rate of 9600 bps.

The project also includes RGB LEDs for visual feedback, which indicate internal activity and clock operation. The design is synthesized and programmed using the open-source iCE40 FPGA toolchain and stored in SPI flash memory.

# Objectives

- Understand the provided Verilog code for UART transmission.
- Implement and verify baud rate generation and UART finite state machine (FSM).
- Integrate the UART transmitter with the VSDSquadron FPGA Mini board.
- Observe transmitted data on a PC using a serial terminal such as PuTTY or Tera Term.
- Document the complete workflow, testing process, and observations for reproducibility.

# Hardware Used

- VSDSquadron FPGA Mini board
- USB-to-UART adapter (FTDI, CP2102, or CH340)
- PC with serial terminal software (PuTTY, Tera Term, etc.)
- USB Type-C cable for board connection

## What This Project Does

- Generates a 9600 Hz baud-rate clock from the internal oscillator.
- Implements a UART transmitter FSM that sends start bit, 8 data bits, and stop bit sequentially.
- Transmits the ASCII character “D” continuously to a PC via the UART TX pin.
- Provides visual feedback via RGB LEDs, showing activity and verifying internal counters and clock.
- Demonstrates reliable FPGA-based serial communication with minimal external hardware.
