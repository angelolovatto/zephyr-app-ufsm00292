# Temperature Monitoring with Zephyr RTOS

Academic project developed during the **Embedded Systems Design** course at the **Federal University of Santa Maria (UFSM)**.

The goal of this project is to structure firmware for temperature monitoring on the **SAM R21 Xplained Pro**, using the **AT30TSE752A** temperature sensor available on the I/O1 Xplained Pro expansion board.

A central aspect of the work is the use of **Test-Driven Development (TDD)** to validate the temperature-conversion logic independently from the physical hardware.

## Technologies and concepts

- **Microcontroller:** ATSAMR21G18A
- **Development board:** SAM R21 Xplained Pro
- **Sensor:** AT30TSE752A
- **Bus:** I²C
- **RTOS:** Zephyr
- **Language:** C
- **Testing:** Ztest
- **Methodology:** Test-Driven Development (TDD)
- **Build/tooling:** CMake and west

## What was implemented

The first development phase focused on building and validating the software architecture before hardware integration.

Completed work includes:

- project structure and Zephyr configuration files;
- sensor-driver interface definition;
- temperature conversion logic;
- host-side tests for the conversion logic;
- validation of the software logic using Zephyr's testing tools.

## Project status

### Phase 1 — Software foundation and testing

- [x] Define project architecture and folder structure
- [x] Create Zephyr configuration files
- [x] Define the temperature-driver interface
- [x] Implement temperature conversion logic using TDD
- [x] Validate the logic on a host/native target

### Phase 2 — Hardware integration

- [ ] Validate the board/toolchain with a basic firmware test
- [ ] Adjust the Device Tree overlay for the I²C bus
- [ ] Implement the low-level Zephyr I²C access
- [ ] Read raw data from the physical sensor
- [ ] Validate complete temperature acquisition on hardware

### Phase 3 — Application features

- [ ] Add periodic temperature acquisition
- [ ] Add Zephyr logging for temperature values
- [ ] Optional shell command for on-demand measurements
- [ ] Optional UART output

## Why the project is structured this way

The project intentionally separates the **business logic** from the **hardware-access layer**. This makes it possible to test the conversion logic independently and reduces the amount of code that depends directly on the physical board.

This repository reflects the actual development status: the software foundation and tests were completed, while full hardware integration remained as future work.

## Academic context

Developed as coursework for **Embedded Systems Design — UFSM**.

## Author

**Angelo Luigi Bocchi Lovatto**  
Computer Engineering — Federal University of Santa Maria (UFSM)
