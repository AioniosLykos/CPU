# CPU
Pipeline CPU with one instuction per CPU execution cycle

A school project that was graded 100% 

Instructions

•
The Instruction RAM has 8 nibbles. These nibbles will be used to store your assembler instructions. Algorithms must fit within this space and terminate with HALT.

•
The Data RAM has 2 nibbles and will store the program’s data.

•
To run a program, you will need to first input the instruction into the Instruction RAM, the data in the Data RAM, and set the PC pointing to the first instruction in the Instruction RAM. All other registers are assumed to be zero or overwritable. Then the auto-clock is turned on and the programs runs. Make sure to set the mode input pin to 1 for the incrementation to start.

o
LOAD REGISTER, RAM_ADDRESS

▪
1st 2 bits : LOAD = 00

▪
3rd bit : REGISTER = 0 for R0, 1 for R1

▪
4th bit : RAM_ADDRESS = 0 for address 0 in RAM, 1 for address 1 in RAM

▪
Example: LOAD R1, 0 → 0010

▪
Example: LOAD R0, 1 → 0001


o
SAVE REGISTER, RAM_ADDRESS

▪
1st 2 bits : SAVE = 01

▪
3rd bit : REGISTER = as in LOAD

▪
4th bit : RAM_ADDRESS = as in LOAD

▪
Example: SAVE R0, 1 → 0101


o
ADD REGISTER1 REGISER2

▪
1st 2 bits : ADD = 10

▪
3rd bit : REGISTER = as in LOAD
▪
4th bit : REGISTER = as in LOAD

▪
The solution to the addition is saved in REGISTER1.

▪
Example: ADD R1 R0 → R1 = R1 + R0 → 1010

▪
Example: ADD R0 R0 → R0 = R0 + R0 → 1000


o
SUB REGISTER1 REGISTER2

▪
1st 2 bits : SUB = 11

▪
3rd bit : REGISTER = as in LOAD
McGill Project COMP 273
Vybihal School of Computer Science Page 6 of 7

▪
4th bit : REGISTER = as in LOAD

▪
The solution to the subtraction is saved in REGISTER1.

▪
Example: SUB R1 R0 → R1 = R1 – R0 → 1110

▪
Example: SUB R0 R0 → R0 = R0 – R0 → 1100


o
HALT

▪
All four bits are 1.

▪
Example: HALT → 1111

▪
This marks the end of the algorithm. The clock’s ticking does not affect the circuit anymore. The PC no longer increments.
