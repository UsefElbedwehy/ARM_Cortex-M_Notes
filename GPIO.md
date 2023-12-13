# GPIO 

General Purpose Input Output 

STM32 have 16 pins per port

The output is circuit **CMOS** but the input is **TTL**.

CMOS uses PMOS and NMOS but TTL schmitt trigger uses pnp(active low) and npn.

Defualt pin state is **Input floating** (Hi-Z). 

It's better to keep unused GPIO pins *pulled up* or *pulled down*.

- ***when pin is programmed as I/P:***

    - output buffer is disabled.

    - schmitt trigger is activated.

    - pull ap and pull down are comfigured, and set depending on PUPDR.

    - Data present on the pin is sampled into IDR every AHB1 clock cycle.


- ***Input mode:***

    - Analog mode. 
    - Floating mode (reset state).
    - Input with pull-up/pull-down.

- ***Output mode:*** 

    - General purpose output push-pull. 
    - General purpose output Open-drain.
    - Alternate function output Push-pull.
    - Alternate function output Open-drain.

