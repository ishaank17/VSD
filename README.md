
<details>
	<summary>Task 1 and 2  </summary>
	
# Day 0 - Tools Installation
We start by modeling the entire RISC-V processor using C code. This C model acts as a high-level specification of how the processor should behave. We compile and run applications on this model using tools like RISC-V GCC to make sure it works correctly.
Once we're confident the C model is accurate, we move on to writing the actual hardware description in Verilog. The Verilog code for the processor only contains what is part of the processor’s instruction set and core logic. Peripherals and other modules (called IP blocks) are kept separate and reused as needed.
These IP blocks can include analog components, macros, or gate-level netlists that are proven and ready to use. By integrating the processor core with these peripherals and IP blocks, we create the full System on Chip (SoC).
Finally, to ensure everything works as expected, we run the same applications on the Verilog hardware model and check that the output matches the behavior of the C specification model.
Key Differences Between Microcontroller and Microprocessor
Microcontroller: A complete system on one chip, including CPU, memory, and peripherals. Used for embedded, specific tasks. Low cost and power-efficient.
Microprocessor: Only the CPU core; needs external memory and peripherals to work. More powerful and flexible, used in PCs and complex systems.

All concept explained using green block.Work only on the blue block .
RTL are converted into gates which are properly placed and routed using and an or gate ff etc. No more if statement - basically only metal layers - it has only transitors.
it makes a gds2 file . It has the information for the fabricator to to make the design. This gos thru various checks(DRC LVS). Then sent to factory (tape out).
Factory gives back made chips (tape in). Then we connect all the pheripherals and transfer data onto the chip to program it. It gives output O4 and we make sure O1=O2=O3=O4.
This all takes 14 Months due to tests and production. Our processors 100Mhz to 130Mhz. 
OG Arduino used risc 5 chip


## Yosys

<img width="575" alt="yosys" src="Photos/Screenshot from 2025-09-20 21-01-08.png">
<img width="575" alt="yosys" src="Photos/Screenshot from 2025-09-20 21-02-48.png">

## Iverilog

<img width="702" alt="iverilog" src="Photos/Screenshot from 2025-09-20 21-03-36.png">
<img width="702" alt="iverilog" src="Photos/Screenshot from 2025-09-20 21-04-25.png">

## NGSpice

<img width="702" alt="iverilog" src="Photos/Screenshot from 2025-09-20 21-22-51.png">

## GTKWave

<img width="604" alt="gtkwave2" src="Photos/Screenshot from 2025-09-20 23-31-01.png">


## Magic

<img width="604" alt="gtkwave2" src="Photos/Screenshot from 2025-09-20 21-29-20.png">

<img width="1008" alt="gtkwave1" src="Photos/Screenshot from 2025-09-20 21-29-53.png">
<img width="1008" alt="gtkwave1" src="Photos/Screenshot from 2025-09-20 21-29-56.png">


# Open Lane

## Dependencies 

<img width="604" alt="gtkwave2" src="Photos/Screenshot from 2025-09-20 21-35-18.png">
<img width="1008" alt="gtkwave1" src="Photos/Screenshot from 2025-09-20 21-36-25.png">
<img width="1008" alt="gtkwave1" src="Photos/Screenshot from 2025-09-20 21-36-34.png">

## PDK Tools

<img width="604" alt="gtkwave2" src="Photos/Screenshot from 2025-09-20 22-49-43.png">

<img width="1008" alt="gtkwave1" src="Photos/Screenshot from 2025-09-20 22-49-52.png">
</details>
