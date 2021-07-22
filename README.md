The Assignment
Recall that an assembler translates code written in mnemonic form in assembly language into machine code.
You will implement an assembler that supports a subset of the MIPS32 assembly language (specified below). The 
assembler will be implemented in C and executed on Linux. Your assembler will take a file written in that subset of the 
MIPS32 assembly language and write an output file containing the corresponding MIPS32 machine code (in text format).
Supported MIPS32 Assembly Language
The subset of the MIPS assembly language that you need to implement is defined below. The following conventions are 
observed in this section:
• The notation (m:n) refers to a range of bits in the value to which it is applied. For example, the expression
(PC+4)(31:28)
refers to the high 4 bits of the address PC+4.
• imm16 refers to a 16-bit immediate value; no assembly instruction will use a longer immediate
• offsetrefers to a literal applied to an address in a register; e.g., offset(rs); offsets will be signed 16-
bit values
• label fields map to addresses, which will always be 16-bit values if you follow the instructions
• sa refers to the shift amount field of an R-format instruction; shift amounts will be nonnegative 5-bit values
• target refers to a 26-bit word address for an instruction; usually a symbolic notation
• Sign-extension of immediates is assumed where necessary and not indicated in the notation.
• C-like notation is used in the comments for arithmetic and logical bit-shifts: >>a , <<l and >>l
• The C ternary operator is used for selection: condition? if-true : if-false
• Concatenation of bit-sequences is denoted by ||.
• A few of the specified instructions are actually pseudo-instructions. That means your assembler must replace each 
of them with a sequence of one or more other instructions; see the comments for details.
You will find the MIPS32 Architecture Volume 2: The MIPS32 Instruction Set (part of the course resources and available 
on Canvas) to be an essential reference for machine instruction formats and opcodes, and even information about the 
execution of the instructions.