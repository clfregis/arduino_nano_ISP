# Arduino nano as ISP

I always had problems flashing to AVR microcontrollers in my projects. Instead of exposing the serial pins for programming the chip using a FTDI or similar programmer, I expose the ICSP pins. The reason for that is because I want to burn bootloader in case I buy a microcontroller without it. 

So I needed to buy an AVR programmer, such as AVRISP or AVRISPv2. However, they are very expensive for just programming (maybe it is worth it for debugging purposes), this is why I have always used another Arduino board as ISP programmer. 

But, my projects became very regular and I had a necessity to have a more robust and reliable programmer, without the usage of protoboard and hundreds of faulty cables that made me pluck all my hair of angry.

As you probably know, instead of buying a programmer, as a maker, I just modified an arduino nano to be my programmer. Thus, in this repository I have pushed all files necessary to use an arduino nano as programmer.

In the future, I will create of a board which will contain all the heartbeat LEDs, etc.

_____________

## Flash the ISP code to the programmer
In the future I will create a make file. For now:

- Clone this repo: `git clone ...`
- `cd` to [build](build/) folder.
- Flash it using avrdude: `avrdude -v -patmega328p -Cavrdude.conf -carduino -b115200 -D -P"/dev/cu.*" -Uflash:w:firmware.hex:i`
