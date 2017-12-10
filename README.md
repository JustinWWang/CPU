# CPU
10-bit, 7 register CPU that can do register transfers and ALU operations.

Load a testing file onto my RAM (on the right) by right clicking it and selecting "load image." You can also create your own set of instructions by using the assembler. 

Instructions:
AND Bitwise AND of registers A and B
OR Bitwise OR of registers A and B
NOT Negate register A
ADD Add registers A and B. You must use carry look-ahead unit(s)
MOV Copy register A
SLL Shift Left Logical. Shift all bits to the left by 1; discard leftmost bit and make
the least significant bit 0. Example: 1011 -> 0110 (operate on mux A input)
SRL Shift Right Logical. Shift all bits to the right by 1; discard rightmost bit and make the most significant bit 0. Example: 1011 ->0101 (operate on mux A input)
SUB Subtract the register B from register A. You must carry look-ahead unit(s)
ADDI Add the instruction data to register A
SUBI Subtract the instruction data from register A
MOVI Copy the instruction data.
BNEZCompare the Dest register with 0. If not zero, then add the lower 5 bits of the immediate data (which may be negative) to the PC, and place the result in the
PC. Note that unlike normal CPUs, the PC will not have been incremented!
The addition will have to be done by a 5-bit adder separate from the ALU.
NOP No registers, other than the PC, should change during this instruction cycle.
HALT Stop the CPU from executing any further instructions.

Example instructions for the assembler (not case sensitive, r's optional):
Movi R1, 1 # load 1 into R(register) 1
Movi r2, 2 # load 2 into R2
Add r3, 2, R1 # add R2 and R1, store result in R3
HALT
