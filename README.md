ECE281_CE4
==========

##PRISM Assembly Language Programming

###So what exactly is "Assembly" anyways?
Well, think of Lego blocks: you only have so many different blocks (in this case 16) to work with, but can build an almost unlimited amount of things. Also, because Santa is on a budget, you have to try and fit everything within 256 addresses because, after all, RAM and ROM - er, Legos - ain't cheap.

 _PRISM_ (That's Programmable Reconfigurable Informational Simple Microcomputer) is a simulation of a typical digital computer which allows for easy assembly programming. The manual – provided by USAFA DFEC – gives more information on how everything works, but basically there is a computer Controller which directs the Datapath, Memory, and Input/Output. Each assembly command takes up one chunk of memory (four bits in PRISM). Certain commands have additional slots for a value or address. It is an extremely simple way of telling the computer precisely what to do. 

###Let's step through a problem.
This is a screenshot of the programming for the Mathematics problem. The actual .psm file is included with the other programs in the repo.

![alt text](https://github.com/byarbrough/ECE281_CE4/blob/master/Mathematics_Shot.PNG?raw=true "Mathematics.psm")

Mathematics.psm doubles the value stored in RAM, subtracts 4, and outputs the result to port 2.

1. Load a -4 into the accumulator. PRISM doesn't accept negative numbers, so instead Address (Addr) loads $C into the accumulator, which is -4 in two's complement.
2. Add the value stored in RAM slot B0. The label is predefined, as is the value within the RAM.
3. Add this number again; this is the same as doubling.
4. Output the final value to port 2
5. Infinite loop to prevent crashing.

##So What?
Why go through all of this trouble in the first place? I mean, there are tons of high level languages out there which could do this with a lot less thinking on the human's part. But what happens once you figure out all of the semicolons in Java? Everything has to run through an assembler which puts it in assembly language. This is then compiled into the lovely 1's and 0's of machine code. As a Computer Engineer, it is important to know about some of the things that run "under the hood." This really ties in everything: registers, the ALU, MUX's, and even logic gates. Plus, I imagine that my friends will think me knowing Assembly is a lot cooler than the cyber guys who get scared to go past the keyboard.

_No Documentation outside of general work in class._
