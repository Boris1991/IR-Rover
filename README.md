IR-Rover 🚗📡
Project Overview

IR-Rover is a firmware for the Rover 5 platform based on the STM32F405 (Iskra JS) microcontroller.
It allows controlling the rover via an infrared remote (IR remote, NEC protocol).
The project uses two DC motors driven through an H-bridge, supporting the following commands:

    Forward 🚀

    Backward ⬅️

    Left ↩️

    Right ↪️

    Stop 🛑

Hardware

    Platform: Rover 5 (without encoders)

    Microcontroller: STM32F405 (Iskra JS)

    Motor driver: Iskra Motor Shield

    IR receiver: based on ADXL335

    Remote control: NEC protocol

Software

    Language: C

    Development environment: STM32CubeIDE

    Libraries: HAL

    Command processing: EXTI interrupts + NEC decode

    The interrupt handler decodes the NEC signal into commands.

    In main(), the commands are interpreted and PWM values are set to control the motors.

Future improvements

    Add encoder support for Rover 5

    Add Mavlink protocol support

    Refactoring throughout Freertos
