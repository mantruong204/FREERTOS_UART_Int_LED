### STM32 Communication with a Button, an LED, and a Computer via UART

If the button is pressed, the LED toggles its state (if the LED is off, pressing the button turns it on, and vice versa). When the button is released, the LED maintains its current state.

UART sends the following commands:

- `ON\CR\LF` turns the LED on
- `OFF\CR\LF` turns the LED off
- `TOGGLE\CR\LF` toggles the LED's state

The system uses three tasks:

1. A task to control the LED.
2. A task to handle the button interactions.
3. A task to manage UART communication.

The tasks communicate with each other through a queue, and UART interrupts can be used to send data to the UART task.
