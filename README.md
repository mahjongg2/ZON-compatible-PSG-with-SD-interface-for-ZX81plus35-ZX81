# PSG-for-ZX81plus35-ZX81-clone
Programmable sound generator for my ZX81 clone, with hardware for SD-card interface

This is a clone of the ZON soundgenerator for my ZX81 clone ZX81+35 which you can find on github as ZX81plus35.

The .zip file contains gerber and drill files for a PCB.

This should work on a real ZX81, if you build an adapter between the (female) edge header connector, and an edge connector for the ZX81.

This PCB was designed and rev 2.0 was tested, (not by me) and after repairing an error caused by faulty definition of an 74LS02, it worked
In the mean time I went on to design a color homecomputer (RhoCoCo) and abandoned my ZX81+35 efforts, see the ZX81plus35 page.

this A-Y-3-8912 PSG based programmable sound generator is software compatible with ZON based software (dancing demon and others)

I used the GPIO's of the 8912 to interface an SD-Card interface, with a bit-banged sd-card driver you should be able to read SD-cards. The trick here is that I added pullups to ensure the outputs would not float during a read, so if you end a clock signal as high, then swich to read mode, the clock input stays high. 

Errors in schematic (and layout) of older revision 2.0 (now replaced with rev 2.1)

It seems there was an error in the library I used for the 74LS02 quad NOR port, as if the designed of the symbol took a 74LS00 and only changed the NAND symbols into NOR symbols, most of the pin numbers of the gates are actually wrong, with one output pin number switched with one input pin number. On a Ls02 pin 1 is an output, not an input.
This problem was fixed in the revision 2.1 files you will find here.

PCB production files can be found in the the .ZIP file, and I uploaded a component overview drawing to easy the assembly.

The main sound generator function has been confirmed to work, and I just heard that with some small patches a Thomas Freiberg got storing and loading ZX-81 games to work, so my next job will be to create version 2.2 updated with his patches! You can read more about it here: https://forums.raspberrypi.com/viewtopic.php?p=1983650#p1983620

I will also start working on a version for real ZX-81's, and my ZX-81+38 clone, this will be designed using KiCad.



