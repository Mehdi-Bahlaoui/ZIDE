# ZIDE: ZIG-Integrated Development Environement
An IDE built with the language ZIG, also, specifically designed for embedded software design with ZIG.

Initial support will be for the Arduino Microcontrollers Family (Q not Included)

More on ZIG: [www.wikipedia/zig (programming language) ](https://en.wikipedia.org/wiki/Zig_(programming_language))



# Currently

This repo is a fork of an already existing project that can build code that can be run on an Arduino Uno, using only Zig as its **only** dependency. 

Currently only `avrdude` is an external dependency that is needed to program the chip.

## Build instructions

* `zig build` creates the executable.
* `zig build upload -Dtty=/dev/ttyACM0` uploads the code to an Arduino connected to `/dev/ttyACM0`.
* `zig build monitor -Dtty=/dev/ttyACM0` shows the serial monitor using `screen`.  
* `zig build objdump` shows the disassembly (`avr-objdump` has to be installed).