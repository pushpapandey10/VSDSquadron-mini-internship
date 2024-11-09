### Task 4: Functional Simulation of RISC-V Core Using Verilog Netlist and Testbench

Using the provided RISC-V core Verilog netlist and testbench, conduct a functional simulation experiment and upload waveform snapshots to your GitHub repository. The reference GitHub repo is located [here](https://github.com/vinayrayapati/rv32i).

#### Steps to Follow:

#### i) Create a Folder in Oracle VirtualBox
   - On the desktop in Oracle VirtualBox, create a new folder to store project files.

#### ii) Clone the GitHub Repository
   - Change the terminal directory to your new folder:
     ```bash
     cd path/to/folder
     ```
   - Clone the repository with the following command:
     ```bash
     git clone https://github.com/vinayrayapati/rv32i
     ```

#### iii) Navigate to the Cloned Repository
   - After cloning, move into the repository directory:
     ```bash
     cd rv32i
     ```

#### iv) Compile the Verilog Code and Testbench
   - Use **iverilog** to compile the Verilog source and testbench files:
     ```bash
     iverilog -o iiitb_rv32i iiitb_rv32i.v iiitb_rv32i_tb.v
     ```

#### v) Run the Simulation
   - After compiling, simulate the RISC-V core by executing the compiled file:
     ```bash
     ./iiitb_rv32i
     ```

#### vi) Capture and Upload Waveform Snapshots
   - After running the simulation, view and capture the waveform snapshots, and upload them to your GitHub repository for documentation and review.

### Functional Simulation of RISC-V Core Using Verilog Code and Testbench

Follow these steps to clone, compile, simulate, and visualize the RISC-V core Verilog code and testbench, with detailed steps to observe output waveforms in GTKWAVE.

---

#### 1. Clone the Repository

Use the following command to clone the RISC-V Verilog repository:

```bash
git clone https://github.com/vinayrayapati/rv321
```

#### 2. Navigate to the Cloned Directory

Change your directory to the cloned repository:

```bash
cd rv321
```

#### 3. Compile the Verilog Code and Testbench

Use the **iverilog** command to compile the Verilog source and testbench files:

```bash
iverilog -o iiitb_rv32i iiitb_rv32i.v iiitb_rv32i_tb.v
```

#### 4. Simulate the Verilog Code

After compiling, simulate the RISC-V core by running the compiled file:

```bash
./iiitb_rv321
```

---

### 5. View the Waveform in GTKWAVE

Once simulation is complete, a `.vcd` (Value Change Dump) file is generated. Use GTKWAVE to visualize the waveform:

```bash
gtkwave iiitb_rv321.vcd
```

- This command will open GTKWAVE. 
- In GTKWAVE, select the `iiitb_rv32i_tb` signal in the **SST** section and drag it to the **time** section to view the waveform.

---

### 6. Observing Waveforms for Each Instruction

Select the instructions from **EX_MEM_IR[31:0]** in GTKWAVE to analyze the output waveform for each instruction covered in Task 3:

#### Instruction Waveforms:

- **Instruction 1: `ADD r1, r1, r2`**

   ![ADD instruction waveform](https://github.com/user-attachments/assets/bc020bf1-4840-4837-9d89-38c06cec98bc)

- **Instruction 2: `SUB r3, r1, r2`**

   ![SUB instruction waveform](https://github.com/user-attachments/assets/1ae337fd-7d59-45a5-b357-3289e1235056)

- **Instruction 3: `AND r2, r1, r3`**

   ![AND instruction waveform](https://github.com/user-attachments/assets/0d56993f-a4b1-49dc-84a8-72ac4f1ea19c)

- **Instruction 4: `OR r8, r2, r5`**

   ![OR instruction waveform](https://github.com/user-attachments/assets/32ef522d-dfd1-4dca-b265-659528c0fd69)

- **Instruction 5: `XOR r8, r1, r4`**

   ![XOR instruction waveform](https://github.com/user-attachments/assets/5fb26807-d7c6-4d95-bbd6-855fbd14c0e3)

- **Instruction 6: `SLL r15, r11, r2`**

   ![SLL instruction waveform](https://github.com/user-attachments/assets/f0aeb7ce-a088-43dd-a54c-5e4887a4af6c)

- **Instruction 7: `SLT r10, r2, r4`**

   ![SLT instruction waveform](https://github.com/user-attachments/assets/edc69fdb-279c-430b-84a8-8279564fb6e4)

---

### Conclusion

GTKWAVE provides the output waveforms for each of the instructions listed above, allowing you to observe and analyze the functionality of the RISC-V core Verilog code.
