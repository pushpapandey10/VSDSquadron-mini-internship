### Step 1: Download Oracle VM VirtualBox

1. **Visit the Official Website**:
   - Navigate to the official Oracle VM VirtualBox download page.
   
2. **Select Your Operating System**:
   - Based on your operating system (Windows, macOS, Linux, etc.), download the appropriate version of VirtualBox.

### Step 2: Install Oracle VM VirtualBox

Follow the instructions provided by the installer for your specific operating system to complete the installation process.

### Step 3: Create and Configure a Virtual Machine

1. **Launch VirtualBox**:
   - Open VirtualBox from the Start Menu (for Windows) or the Applications menu (for other OS).
   
2. **Create a New Virtual Machine**:
   - Click the "New" button.
   - Enter a name for your virtual machine and select the operating system you plan to install.
   - Choose the amount of memory (RAM) to allocate for the VM. It's recommended to set at least 2GB (4096 MB) for modern OS.
   - Create a virtual hard disk (VDI format is typically used).

3. **Install an Operating System**:
   - After creating the VM, click "Start."
   - When prompted to select a startup disk, choose the ISO file for the operating system you want to install. In this case, select the ISO file for Ubuntu 18.04.
   - Proceed with the installation steps for Ubuntu.

![1 png](https://github.com/user-attachments/assets/401a7043-5ccd-4bf0-8191-d4f18eb84ff5)

### Step 4: Write the `cd` Command and C Program

1. **Open Gedit**:
   - Before proceeding, ensure that **Leafpad** is installed on your system.
   
2. **Write the C Program**:
   - Open Leafpad and write a `cd` command.
   - Then, write a C program to calculate the sum of `n` numbers.

![2 png](https://github.com/user-attachments/assets/4b2bd4ab-9b12-40c0-a668-1454cad93280)

### Step 5: Verify Output

Once the program is written and executed, you should be able to see the output.

![3 png](https://github.com/user-attachments/assets/0b8b25ec-6b3d-4e6a-ae67-1de976ba9aef)

### Step 6: Compile and Run with RISC-V Simulator

1. **Compile the C Program**:
   - Now, compile and run the C code using the RISC-V Simulator.

2. **Locate the `main` Function**:
   - To find the `main` function in the compiled object file, use the following command:
     ```bash
     riscv64-unknown-elf-objdump -d sum.o | less
     ```
   - Then, search for `main` by typing `/main`.

![image](https://github.com/user-attachments/assets/d338286a-0330-4fd9-8333-e339a8425565)

### Step 7: Further Execution

Continue the process as required for your program setup and ensure everything runs smoothly.

![image](https://github.com/user-attachments/assets/b0afa3d2-82f8-44a0-8e89-82772c597c77)

### Step 8: Final Verification

Complete the steps necessary for verifying the program's correctness and functionality.

![image](https://github.com/user-attachments/assets/2280a39a-1636-40e1-96df-d9c09ecf08ae)

This completes the task of setting up and running your virtual machine and program.
