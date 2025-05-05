# Bare-Metal Programming on STM32F303RE

## Overview
This is a personal documentation of my journey learning bare-metal programming on the STM32F303RE microcontroller. The goal is understand and document how to program the chip using only its datasheet, reference manual, and basic open-source tools - avoiding the abstractions provided by STM32CubeMX and HAL libraries.

This guide and codebase is updated as I learn. I reference some great community resources to guide my learning and rely on the official board documentation to adapt them specifically for the STM32F303RE.

## Table of Contents
* [Overview](#overview)
* [Setup](#setup)
* [Reference Materials](#reference-materials)

## Setup
This project is developed in an Ubunto host OS using Visual Studio Code. 

### Target Board
**Development Board:** NUCLEO-F303RE  
**Microcontroller (MCU):** STM32F303RE

### Tools
I use the same toolchain used in [cpq's guide](https://github.com/cpq/bare-metal-programming-guide?tab=readme-ov-file). 
- **[ARM GCC (gcc-arm-none-eabi)](https://launchpad.net/gcc-arm-embedded)**  
  Cross-compiler for ARM Cortex-M microcontrollers. Used to compile and link the firmware.
- **[GNU Make](https://www.gnu.org/software/make/)**  
  Automates the build process via `Makefile`.
- **[ST-Link Tools (stlink)](https://github.com/stlink-org/stlink)**  
  Flash and debug the STM32 using the onboard ST-Link programmer/debugger.

Linux(Ubuntu) installation:
```bash
sudo apt update
sudo apt install gcc-arm-none-eabi make stlink-tools
```

## Reference Materials
* [cpq's Bare-Metal Programming Guide](https://github.com/cpq/bare-metal-programming-guide)
* [Mattia Maldini's Bare-Metal Programming Guide](https://maldus512.medium.com/bare-metal-programming-on-an-stm32f103-3a0f4e50ca29)
* [STM32F303RE Datasheet](https://www.st.com/resource/en/datasheet/stm32f303re.pdf)
* [STM32F303RE Reference Manual (RM0316)](https://www.st.com/resource/en/reference_manual/rm0316-stm32f303xbcde-stm32f303x68-stm32f328x8-stm32f358xc-stm32f398xe-advanced-armbased-mcus-stmicroelectronics.pdf)