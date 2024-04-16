<!----

This file is used to generate your project datasheet. Please fill in the information below and delete any unused
sections.

You can also include images in this folder and reference them in the markdown. Each image must be less than
512 kb in size, and the combined size of all images must be less than 1 MB.
-->

## How it works

El proyecto es un circuito que implementa compuertas logicas para el control de giro de dos motores dc, el cual tiene como entradas a- Entrada 1, Entrada 2, Entrada 3,- y como salidas a SALIDA1, SALIDA 2, SALIDA 3, SALIDA 4.


A schematic of the circuit may be found at:

https://wokwi.com/projects/354858054593504257

The circuit has 10 inputs:

| Input    | Setting                     |
| -------- | -------                     |
| CLK      | Clock                       |
| RST_N    | Not Used                    |
| 01       | ENTRADA 1                    |
| 02       | ENTRADA 2      |
| 03       | ENTRADA 3               |
| 04       | Not Used                    |
| 05       | Not Used                    |
| 06       | Not Used                    |
| 07       | Not Used                    |
| 08       | Not Used                    |

The CLK sets the clocking for the flip-flop registers for latching the LFSR values. In the schematic shown in the Wokwi project, a switch is used to select either the system clock or an externally provided or manual clock that allows the user to manually step through each latching event.

An 8-input DIP switch provides some flexibility to initalizing the LFSR. DIP03 (IN2) allows the user to toggle the Input Select function, which is a multiplexer that select whether the left-most register (R1) takes in as the input the LFSR feedback output (i.e., (R1 = R32 ^ R30 & R26 ^ R25) or a value that is manually selected by the user.

DIP02 (IN1) allows a the user to manually enter a 0 or a 1 value into the leftmost register.

The cicuit has 8 outputs. They output the values of the 8 right-most registers (R25, R26, R27, R28, R29, R30, R31, R32).

| Output   | Value in    |
| -------- | -------     |
| 01       | SALIDA 1 |
| 02       | SALIDA 2 |
| 03       | SALIDA 3 |
| 04       | SALIDA 4 |
| 05       | R29 |
| 06       | R30 |
| 07       | R31 |
| 08       | R32 |

## How to test

LA ENTRADA NUMERO 1 ES LA QUE HACE QUE CAMBIE DE DIRECCION EN AMBOS MOTORES, CUANDO SE PULSA LA ENTRADA 2 NO EXISTE NINGUN CAMBIO, AL PRESIONAR LA ENTRADA 3 SE DETIENEN POR COMPLETO MANTENIENDO EL CLICK EN LA PRIMER ENTRADA



A python implementation of the 32-bit Fibonacci LFSR can be found at the link below. It may be used for testing the hardware for sequences longer than the initial 100 values.



## External hardware

No external hardware is required.
