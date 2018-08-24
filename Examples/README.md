All these examples are bare-metal examples generated using the STM32CubeMX application and compiled using System Workbench for STM32. The STM32CubeMX tool can also generate projects for other compilers, etc.

Examples so far...

Blinky
------------
Toggles an LED at 10Hz

CDC
------------
Toasty enumerates as a CDC device and sends "Hello!" at 10Hz


** Info **

For all the above projects, the compiled output is a HEX file which needs to be converted into a DFU file by the STM "DFU File Manager" utility. Once a DFU file is generated, it can be uploaded to Toasty using "DfuSe Demo" application which makes use of the built-in STM USB bootloader.

The above process is currently being automated so that post-build actions automatically convert the HEX file and program the board.

** NOTES **
When attempting to load the CDC example, it is vital that in this File Manager utility, the correct VID and PID is entered (0483 and 5740) to match the USB settings from the STM32CubeMX project.