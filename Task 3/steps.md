# TASK 3
## A. List various RISC-V instruction type (R, I, S, B, U, J) after going through RISC-V software documentation.
# What is RISC-V?
(i)  RISC-V is an open-source instruction set architecture (ISA) that allows developers to develop processors for specific applications.
(ii) RISC-V is based on reduced instruction set computer principles and is the fifth generation of processors built on this concept.

# INSTRUCTIONS FORMAT IN RISC-V
The instruction format of a processor refers to how machine language instructions are structured and organized for execution by the processor. These instructions are composed of sequences of 0s and 1s, each encoding information about the data's location and the operations to be performed.

There are 6 instruction formats in RISC-V:
## R, I, S, B, U, J-format
![image](https://github.com/user-attachments/assets/e9b6a795-6e82-4ea6-9feb-129a8dc1bc9b)
1. "opcode" represents a 7-bit instruction operator code, its role is to distinguish between different instructions.
2. "funct3" represents a 3-bit function code.it is an additional opcode.
3. "funct7" represents a 7-bit function code, which can help distinguish different kinds of instructions.
4. "rs1" and "rs2" represent two 5-bit source registers.
5. "rd" is a 5-bit destination register, and the result of the instruction operation is stored in rd.
6. "imm" represents an immediate number of different lengths, which can be used directly as an operand.

### RISC-V Instruction Types

1. **R-Type (Register-Register)**
   - **Use:** Operates on two source registers, stores result in a destination register.
   - **Fields:** `opcode`, `rd` (destination), `func3`, `rs1`, `rs2`, `func7`
   - **Example:** `add x1, x2, x3`

2. **I-Type (Immediate)**
   - **Use:** One source register with an immediate value; includes loads.
   - **Fields:** `opcode`, `rd`, `func3`, `rs1`, `imm[11:0]`
   - **Example:** `addi x1, x2, 10`

3. **S-Type (Store)**
   - **Use:** Stores a register value to memory.
   - **Fields:** `opcode`, `imm[11:5]`, `func3`, `rs1` (base), `rs2` (data), `imm[4:0]`
   - **Example:** `sw x2, 0(x1)`

4. **B-Type (Branch)**
   - **Use:** Conditional branch instructions.
   - **Fields:** `opcode`, `imm[12]`, `imm[10:5]`, `func3`, `rs1`, `rs2`, `imm[4:1]`, `imm[11]`
   - **Example:** `beq x1, x2, label`

5. **U-Type (Upper Immediate)**
   - **Use:** Operates with large immediate values.
   - **Fields:** `opcode`, `rd`, `imm[31:12]`
   - **Example:** `lui x1, 0x10000`

6. **J-Type (Jump)**
   - **Use:** Jump instructions with large immediate values.
   - **Fields:** `opcode`, `rd`, `imm[20]`, `imm[10:1]`, `imm[11]`, `imm[19:12]`
   - **Example:** `jal x1, label`




### 32-bit Instruction Codes in RISC-V Format for 15 Unique Instructions

1. **`addi x1, x2, 10`**
   - **Format:** I-type
   - **Binary Encoding:** `000000000010 00010 000 00001 0010011`
   - **32-bit Code:** `0x00210093`

2. **`li x5, 0x0`**
   - **Format:** I-type (`addi x5, x0, 0x0`)
   - **Binary Encoding:** `000000000000 00000 000 00101 0010011`
   - **32-bit Code:** `0x00000293`

3. **`lui x10, 0x20000`**
   - **Format:** U-type
   - **Binary Encoding:** `00100000000000000000 01010 0110111`
   - **32-bit Code:** `0x20000537`

4. **`mv x1, x2`**
   - **Format:** I-type (`addi x1, x2, 0`)
   - **Binary Encoding:** `000000000000 00010 000 00001 0010011`
   - **32-bit Code:** `0x00010093`

5. **`sw x5, 0(x10)`**
   - **Format:** S-type
   - **Binary Encoding:** `0000000 00101 01010 010 00000 0100011`
   - **32-bit Code:** `0x0050a023`

6. **`lw x5, 0(x10)`**
   - **Format:** I-type
   - **Binary Encoding:** `000000000000 01010 010 00101 0000011`
   - **32-bit Code:** `0x0000a283`

7. **`jal x0, 0x100`**
   - **Format:** J-type
   - **Binary Encoding:** `00000000000100000000 00000 1101111`
   - **32-bit Code:** `0x0000086f`

8. **`beq x1, x2, label`** (offset 0x4)
   - **Format:** B-type
   - **Binary Encoding:** `000000 00010 00001 000 00010 1100011`
   - **32-bit Code:** `0x00210063`

9. **`bne x1, x3, label`** (offset 0x4)
   - **Format:** B-type
   - **Binary Encoding:** `000000 00011 00001 001 00010 1100011`
   - **32-bit Code:** `0x00310063`

10. **`slli x5, x1, 1`**
    - **Format:** I-type
    - **Binary Encoding:** `0000000 00001 00101 001 00001 0010011`
    - **32-bit Code:** `0x00109093`

11. **`srli x6, x2, 2`**
    - **Format:** I-type
    - **Binary Encoding:** `0000000 00010 00110 101 00010 0010011`
    - **32-bit Code:** `0x0022b093`

12. **`and x3, x4, x5`**
    - **Format:** R-type
    - **Binary Encoding:** `0000000 00101 00100 111 00011 0110011`
    - **32-bit Code:** `0x005201b3`

13. **`or x2, x3, x4`**
    - **Format:** R-type
    - **Binary Encoding:** `0000000 00100 00011 110 00010 0110011`
    - **32-bit Code:** `0x004181b3`

14. **`sub x3, x5, x2`**
    - **Format:** R-type
    - **Binary Encoding:** `0100000 00010 00101 000 00011 0110011`
    - **32-bit Code:** `0x402282b3`

15. **`xor x1, x2, x3`**
    - **Format:** R-type
    - **Binary Encoding:** `0000000 00011 00010 100 00001 0110011`
    - **32-bit Code:** `0x003100b3`





