# Arduino nano as ISP
______________
I always had problems flashing to AVR microcontrollers in my projects. Instead of exposing the serial pins for programming the chip using a FTDI or similar programmer, I expose the ICSP pins. The reason for that is because I want to burn bootloader in case I buy a microcontroller without it. 

So I needed to buy an AVR programmer, such as AVRISP or AVRISPv2. However, they are very expensive for just programming (maybe it is worth it for debugging purposes), this is why I have always used another Arduino board as ISP programmer. 

But, my projects became very regular and I had a necessity to have a more robust and reliable programmer, without the usage of protoboard and hundreds of faulty cables that made me pluck all my hair of angry.

As you probably know, instead of buying a programmer, as a maker, I just modified an arduino nano to be my programmer.Thus, in this repository I have pushed all files necessary to use an arduino nano as programmer using a mixture of platformio and avrdude.

In the future, I will remove the platformio and use pure avr gcc and avrdude commands along with the creation of a make file and a creation of a board which will contain all the heartbeat LEDs, etc.
