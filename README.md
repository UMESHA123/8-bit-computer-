# 8-bit-computer-

TABLE OF CONTENTS

Acknowledgement03

Abstract04
Table of Contents05
List of Figures07
List of Tables08
1. INTRODUCTION
2.  General Introduction
3.  Problem Statement
4.  Methodology
5. Scope of the project
6.  Limitations
7. Organization of the Report
8.  THEORITICAL BACKGROUND
9.  Literature Survey
10.  DESIGN AND IMPLEMENTATION
11. Introduction
12. System Design
13. Circuit Description
14. Implementation
15.  RESULTS AND DISCUSSION
16.  Expected Outcome
17.  CONCLUSION AND FUTURE SCOPE
18.  Conclusion
19.  Future Scope
20.  REFERENCES



            22.  LIST OF FIGURES
            23.  Figure 3.1 Block diagram of 8-bit computer
            24.  Figure 3.2 Circuit diagram of clock
            25.  Figure 3.3 Circuit diagram of Registers
            26.  Figure 3.4 Circuit diagram of ALU
            27.  Figure 3.5 Circuit diagram of RAM
            28.  Figure 3.6 Circuit diagram of PC
            29.  Figure 3.7 Project Setup
            30.  Figure 4.1 Block diagram of ADDITION
            31.  Figure 4.2 Block diagram of SUBTRACTION
            32.  Figure 4.3 Flow chart of FIBONACCI series
            33.  Figure 4.4 Image of Seven segment display and Buzzer
            34.  Figure 4.5 Interfacing Seven segment display




Introduction

1.1 General Introduction:

                Introduction Computer Architecture consists of some basic design
      based on Computer Organization and Architecture (COA) such as logic design.
      The Design based on Von Neumann Architecture that generally includes
      Registers, Bus Interface, ALU, Memory and their structures. In computer
      architecture, 8- bit integers, memory addresses, or other data units are those that
      are 8 bits wide. Also, 8-bit CPU and ALU architectures are those that are based
      on registers, address buses, or data buses of that size. 8-bit is also a generation of
      microcomputers in which 8-bit microprocessors were the normal form and they
      performed basic arithmetic problems. The control logic is the heart of the CPU.
      It’s what defines the opcodes the processor recognizes and what happens when it
      executes each instruction. Before building the control logic, we want to connect
      all of the modules to a shared bus and test things out. The output register is similar
      to any other register (like the A and B registers) except rather than displaying its
      contents in binary on 8 LEDs, it displays its contents in decimal on a 7-segment
      display. The program counter (PC) counts in binary to keep track of which
      instruction the computer is currently executing.



Problem Statement:

                Leading students to improve knowledge about COA needs a
        comprehensive learning with a working simulation of a simple 8-bit
        Central Processing Unit (CPU).
        
1.3 Methodology:

      ➢ The job of Program Counter is to send to the memory the address of
        the next instruction to be fetched and executed.
      ➢ The job of address register is to give the address for fetching the
        particular instruction.
      ➢ The lower 4 bit of instruction register is now used to point the address
        of the data which is stored in the RAM.
      ➢ Now this data is sent to the register A and stored.
      ➢ The above process repeats again for the storing data in register B.
      ➢ Now the ALU performs the tasks by taking input from register A and B.
      ➢ After getting the output from ALU, now that result is stored in register A.
      ➢ Now from the A register we can take the result and transfer it to output
        port and show the result.

Scope of the project:

                        One of the most important elements in a computer system is the
            bus structure that supplies the interface for all the hardware components.
            This bus structure contains the necessary signals to allow the various
            system components to interact with each other. The bus supports two
            independent address spaces: memory and I/O. During memory cycles, the
            bus allows direct addressability of up to 16 megabytes using 24-bit
            addressing. During I/O bus cycles, the bus allows addressing of up to 64
            kilobyte I/O ports using l6.bit addressing. Memory and I/O cycles can
            support 8-bit or 16-bit data transfers.

Limitations:

            ➢ Instruction set is limited to only 16 bytes.
            ➢ Maximum result is 255(8-bit only).
            ➢ Program needs to be written every time the power goes off.
            ➢ Input is through dip switches, which is not very user-friendly.
            ➢ Power supply is limited to 5 volts.
            
            
DESIGN AND IMPLEMENTATION

3.1 Introduction:

                        Figure 3.1 shows the architecture (structure) of 8-bit computer, a
            bus-organized computer. All register outputs to the W bus are three-state; this
            allows orderly transfer of data. All other register outputs are two-state; these
            outputs continuously drive the boxes they are connected to.
            The layout of Fig. 3.1 emphasizes the registers used in 8-bit computer. For this
            reason, no attempt has been made to keep all control circuits in one block called
            the control unit, all input-output circuits in another block
            called the i/o unit, etc.

![8 bir architecture Diagram](https://user-images.githubusercontent.com/73009807/189870670-e3030582-d6a7-4d8a-a518-aebc5d88680a.png)

1.Clock:

                          The computer’s clock is used to synchronize all operations. The clock
            we’re building is based on the popular 555 timer IC. Our clock is adjustable-speed
            (from less than 1Hz to a few hundred Hz). The clock can also be put into a manual
            mode where you push a button to advance each clock cycle. This will be a really
            useful feature for debugging the computer later on.

![IMG_20220717_162902](https://user-images.githubusercontent.com/73009807/189871822-376c5903-8938-4f04-981c-c991c1366ff5.jpg)


Registers

                        Most CPUs have a number of registers which store small amounts
            of data that the CPU is processing. In our simple breadboard CPU, we’ll build
            three 8-bit registers: A, B, and IR. The A and B registers are general-purpose
            registers. IR (the instruction register) works similarly, but we’ll only use it for
            storing the current instruction that’s being executed. The instruction register is
            part of the control unit. To fetch an instruction from the memory the computer
            does a memory read operation. This places the contents of the addressed
            memory location on the W bus.
            At the same time, the instruction register is set up for loading on
            the next positive clock edge. The contents of the instruction register are split
            into two nibbles. The upper nibble is a two-state output that goes directly to the
            block labeled Controller-sequencer." The lower nibble is a three-state output
            that is read onto the W bus when needed.







Arithmetic and logic unit:

            The arithmetic logic unit (ALU) part of a CPU is usually capable of
            performing various arithmetic, bitwise, and comparison operations on binary
            numbers. In our simple breadboard CPU, the ALU is just able to add and
            subtract. It’s connected to the A and B registers and outputs either the sum of
            A+B or the difference of A-B.

![Uploading IMG_20220717_162937.jpg…]()

Random access memory (RAM) module

                        The random access memory (RAM) stores the program the computer
            is executing as well as any data the program needs. Our breadboard computer
            uses 4-bit addresses which means it will only have 16 bytes of RAM, limiting the
            size and complexity of programs it can run. above the program counter is the
            input and MAR block.
            It includes the address and data switch registers show in fig 3.1. These
            switch registers, which are part of the input unit, allow you to send 4 address bits
            and 8 data bits to the RAM. As you recall, instruction and data words are written
            into the RAM before a computer run. The memory address register (MAR) is part
            of the SAP1 memory. During a computer run, the address in the program counter
            is latched into the MAR. A bit later, the MAR applies this 4-bit address to the
            RAM, where a read operation is performed.
            The RAM is a 16 X 8 static TTL RAM. As discussed in Sec. 9-4, you can
            program the RAM by means of the address and data switch registers. This allows
            you to store a program and data in the memory before a computer run. During a
            computer run, the RAM receives 4-bit addresses from the MAR and a read
            operation is performed. In this way, the instruction or data word stored in the
            RAM is placed on the W bus for use in some other part of the computer.

![IMG_20220717_162910](https://user-images.githubusercontent.com/73009807/189876291-0f5b912f-0143-4ad2-b0f8-21b8c744e694.jpg)


Address genereter

![IMG_20220717_162906](https://user-images.githubusercontent.com/73009807/189876322-f88944cd-d01e-4a55-92e4-6f252236374b.jpg)


Data genereter
![Uploading IMG_20220717_162912.jpg…]()



Program counter

                         The program is stored at the beginning of the memory with the first
            instruction at binary address 0000, the second instruction at address 0001, the
            third at address 0010, and so on. The program counter, which is part of the control
            unit, counts from 0000 to 1111. Its job is to send to the memory the address of
            the next instruction to be fetched and executed. It does this as follows. The
            program counter is reset to 0000 before each computer run. When the computer
            run begins, the program counter sends address 0000 to the memory.
            The program counter is then incremented to get 0001. After the first
            instruction is fetched and executed, the program counter sends address 0001 to
            the memory. Again the program counter is incremented. After the second
            instruction is fetched and executed, the program counter sends address 0010 to
            the memory. In this way, the program counter is keeping track of the next
            instruction to be fetched and executed.
            The program counter is like someone pointing a finger at a list of
            instructions, saying do this first, do this second, do this third, etc. This is why the
            program counter is sometimes called a pointer; it points to an address in memory
            where something important is being stored.



![Screenshot from 2022-09-13 15-30-55](https://user-images.githubusercontent.com/73009807/189873053-013f1bfe-3186-484c-a070-f88d639cd671.png)


Project Setup


![Screenshot from 2022-09-13 15-34-13](https://user-images.githubusercontent.com/73009807/189873738-9974997d-efc6-4830-9c4d-ab83a8763f47.png)


The 8 bit computer does basic arithmetic functions like addition,
subtraction.


![ADD_BB](https://user-images.githubusercontent.com/73009807/189874193-211f94e2-f6fe-486b-838b-e1a177bcfd20.PNG)

Addition:

            MOV R0,@14
            ADD R0,@15
            OUT

![ADDTION BLOCK](https://user-images.githubusercontent.com/73009807/189874352-471df819-1e98-4987-a12a-c0185f1c6913.png)

Subtraction:

            MOV R0,@14
            SUB R0,@15
            OUT

Finding the Fibonacci Sequence

            a series of numbers in which each number (Fibonacci number) is
            the sum of the two preceding numbers. The simplest is the series
            0,1,1,2,3,5,8,11…….

            
            MOV R0,@13 // X INPUT
            MOV R1,@14 // Y INPUT
     LOOP   OUT
            ADD R0,R1 // X = X +Y
            MOV @15,R0 // Z = X
            MOV @13,R1 // X = Y
            MOV R1,@15 // Y = Z
            JC LOOP
            END
            
![Screenshot from 2022-09-13 15-40-50](https://user-images.githubusercontent.com/73009807/189875082-01d9ddb4-55da-4b85-afc6-090c8e044d25.png)


Interface Seven segment display and buzzer.

![IMG_20220717_162918](https://user-images.githubusercontent.com/73009807/189875194-036f8af2-65c2-4110-8908-225fb8c5cef6.jpg)

            The number 8 is displayed when the power is given to all the
            segments and if you disconnect the power for ‘g’, then it displays
            number 0. In seven segment display, power (or voltage) at different pins
            can be applied at the same time, so we can form combinations of display
            numerical from 0 to 9. Since seven segment display can not form
            alphabet like X and Z, so it can not be used for alphabet and it can be
            used only for displaying decimal numerical magnitudes. However, seven
            segment displays can form alphabets A, B, C, D, E, and F, so it can also
            used for representing hexadecimal digits.
            
![Seven-Segment-Display-Truth-Table](https://user-images.githubusercontent.com/73009807/189875339-bb3b33b2-9bcb-4158-8cc7-dbed36a354f9.png)

            MOV @0000 , 0111111B
            MOV @0001 , 0000110B
            MOV @0010 , 1011011B
            MOV @0011 , 1001111B
            MOV @0100 , 1100110B
            MOV @0101 , 1101101B
            MOV @0110 , 1111101B
            MOV @0111 , 0000111B
            MOV @1000 , 1111111B
            MOV @1001 , 1100111B
            MOV R0 , 0000B
       LOOP
            OUT @R0
            INC R0,#1
            JC LOOP


CONCLUSION

            An student has suffered to study COA with the theory that
            explained in several lessons, the lesson explained a structure and an
            architecture computer only. There are not providing a simulation that
            explained step by step computer architecture
            The 8 bit computer does all basic arithmetic functions like addition,
            subtraction, etc., but doesn’t do all the arithmetic functions. This computer
            can be made Turing complete. If the computer supports and runs all the
            Turing functions we can say that the 8 bit computer is Turing complete.
            This can be done by simple enhancements in the computer. This
            will make the computer do a whole lot of new functions and the
            possibilities will be greater than the previous generation. This makes it
            easy to use for creating temporary prototypes and experimenting with
            circuit design. For this reason, solderless breadboards and other
            components can be diminished into a suitable and user friendly
            environment.

FUTURE SCOPE

            The microprocessors are considered to be one of the most
            enhanced product of this product and thus made to be used in an user
            friendly and accessible environment. The modularity of the design makes
            it easier to test each module by itself so we won’t ever get to a point where
            we put it all together and nothing works.
            The output register is similar to any other register (like the A and B
            registers) except rather than displaying its contents in binary on 8 LEDs, it
            displays its contents in decimal The modularity of the design makes it
            easier to test each module by itself so we won’t ever get to a point where
            we put it all together and nothing works. The output register is similar to
            any other register (like the A and B registers) except rather than displaying
            its contents in binary on 8 LEDs, it displays its contents in decimal.


REFERENCES

https://eater.net/8bit/

http://www.instructables.com/id/How-to-Build-an-8-Bit-Computer/

https://electronicsforu.com/electronics-projects/simple-8-bit-computer-
learning

https://www.extremetech.com/computing/128035-how-to-build-an-8-
bit-computerfrom-scratch

digital-computer-electronics-3rd-edition-malvino

http://www.instructables.com/id/How-to-Build-an-8-Bit-Computer
