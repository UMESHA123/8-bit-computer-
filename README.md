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
/media/umesha/CCCOMA_X64FRE_EN-GB_DV9/New folder/8 bit computer architecture/final report_final.pdf

