# 4-Bit Binary to Decimal Display (0–15)

An electronics project that converts a 4-bit binary input into a decimal number from 0 to 15 and displays it using two seven-segment displays.

## Project Motivation

I built this project to understand digital logic, binary-to-BCD conversion, transistor switching and seven-segment display interfacing.

During development, I faced several problems with logic gate polarity, IC pin connections, BCD conversion and display interfacing.

I am sharing the complete project so other students and electronics enthusiasts can learn from it without spending the same amount of time troubleshooting.

## Features

- Four DIP switches for binary input.
- Displays decimal numbers from 0 to 15.
- Separate tens and ones digit display.
- BCD conversion for the ones digit.
- Logic IC-based implementation.
- BC547 transistor-based circuitry.
- Two seven-segment displays.

## Components

- BC547 NPN transistors
- SN74LS48 BCD-to-seven-segment decoder
- 74HC04 hex inverter
- 74HC11 triple 3-input AND gate
- CD4081 quad 2-input AND gate
- 74HC32 quad OR gate
- CD4011 NAND gate (if used in the final circuit)
- Four-position DIP switch
- Two seven-segment displays
- Resistors
- 5V DC power supply

*Update this list to match the exact components in your final working schematic.*

## Binary-to-Decimal Conversion

The input is represented by four bits:

| Input | Decimal |
|---|---:|
| 0000 | 0 |
| 0001 | 1 |
| 0010 | 2 |
| 0011 | 3 |
| 0100 | 4 |
| 0101 | 5 |
| 0110 | 6 |
| 0111 | 7 |
| 1000 | 8 |
| 1001 | 9 |
| 1010 | 10 |
| 1011 | 11 |
| 1100 | 12 |
| 1101 | 13 |
| 1110 | 14 |
| 1111 | 15 |

## Ones Digit Logic

Let A, B, C and D represent the binary inputs with weights 8, 4, 2 and 1.

The BCD output equations are:

- Y3 = A·B'·C'
- Y2 = B·(A' + C)
- Y1 = A'·C + A·B·C'
- Y0 = D

These equations produce the ones digit for inputs 0–15.

## Power Supply

Use a regulated 5V supply.

All logic ICs must share a common ground. Check the supply pins of every IC before starting the simulation or physical testing.

## Troubleshooting Lessons

1. Check IC power connections. An SN74LS48 supply voltage of 0.90V prevented the decoder from operating.
2. Verify the pinout of every IC.
3. Check whether an LED is connected to indicate active-HIGH or active-LOW logic.
4. Do not connect two logic outputs directly together.
5. Check DIP switch polarity and pull-down resistors.
6. Verify BCD inputs before troubleshooting the seven-segment display.
7. Check display type and decoder compatibility.

## Project Files

See the `Circuit`, `Images` and `Documentation` folders for the complete schematic, connection details, simulation results and troubleshooting guide.

## Contribution

Students and electronics enthusiasts are welcome to suggest improvements, report mistakes and contribute better circuit implementations.

## License

MIT License (see LICENSE file).

---

**Built to learn, documented to help others.**
