# samsung-riscv
## 📌Task 1

C program using leafpad editor in terminal on ubuntu

<img width="960" alt="Screenshot 2025-01-06 192801" src="https://github.com/user-attachments/assets/f20799a3-58dc-474f-8e15-5aa4c79c781c" />

c program code converted into assembly code

<img width="960" alt="Screenshot 2025-01-07 213158" src="https://github.com/user-attachments/assets/1a542484-203d-4cdb-8498-aeb32e441237" />
<img width="960" alt="Screenshot 2025-01-07 213352" src="https://github.com/user-attachments/assets/a2eca722-0ae6-4bb3-80f2-d3f9a9567b98" />
<img width="960" alt="Screenshot 2025-01-07 213704" src="https://github.com/user-attachments/assets/77471fee-77e3-4555-9483-d2102e7dd644" />


## 📌Task 2

Run the simulation and observe the performance under the -O1 and -Ofast compiler optimization flags.

👉-Ofast compiler optimization flag is used and debugging using the spike debugger

<img width="960" alt="Screenshot 2025-01-12 094244" src="https://github.com/user-attachments/assets/95701be4-f5ed-40a8-a497-0add69554240" />

-Ofast compiler optimization flag assembly code

<img width="960" alt="Screenshot 2025-01-12 102118" src="https://github.com/user-attachments/assets/8cfb70d0-888c-4fe8-a1c4-86d1089a7cc6" />

👉-O1 compiler optimization flag is used and debugging using the spike debugger
<img width="960" alt="Screenshot 2025-01-12 101933" src="https://github.com/user-attachments/assets/f53b350b-5b17-4195-ba47-65e8abeb64cf" />

-O1 compiler optimization flag assembly code
<img width="960" alt="Screenshot 2025-01-12 102002" src="https://github.com/user-attachments/assets/657eddd6-d914-4981-b289-03d1971ff321" />

## 📌Task 3
👉understand the R, I, S, B, U, and J instruction types.

👉For those 15 instructions, determine the exact 32-bit instruction code in their respective instruction type formats.
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/56253731-abb4-44b5-b759-3fd662649821" /><br>
### 1) Instruction: lui a0, 0x21<br>
<li>Opcode: 0110111 (7 bits)<br>
<li>Immediate: 0x21 (20 bits)<br>
<li>Destination Register (rd): a0 (x10, 5 bits)<br>

### Breakdown:<br>
<li>Immediate (20 bits): 0000 0000 0000 0010 0001<br>
<li>rd (a0 = x10): 01010<br>
<li>Opcode: 0110111<br>

### Machine Code:<br>
<li>Binary: 0000 0000 0000 0010 0001 0101 0011 0111<br>
<li>Hex: 00021537<br>
  
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/33f1af12-9f3f-4eb7-aa4f-4c271ead71d2" /><br>
### 2) Instruction: addi sp, sp, -16<br>
<li>Opcode: 0010011 (7 bits)<br>
<li>Immediate: -16 (12 bits)<br>
<li>Source Register (rs1): sp (x2, 5 bits)<br>
<li>Destination Register (rd): sp (x2, 5 bits)<br>
<li>Function (funct3): 000 (3 bits)<br>

### Breakdown:<br>
<li>Immediate (12 bits): 1111 1111 0000<br>
<li>rs1 (sp = x2): 00010<br>
<li>funct3: 000<br>
<li>rd (sp = x2): 00010<br>
<li>Opcode: 0010011<br>

### Machine Code:<br>
<li>Binary: 1111 1111 0000 0001 0000 0001 0001 0011<br>
<li>Hex: ff010113<br>

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/c085695d-6951-4e19-be49-8fc8b6edcd4a" /><br>
### 3) Instruction: li a2, 210<br>
<li>Opcode: 0010011 (7 bits)<br>
<li>Immediate: 210 (12 bits)<br>
<li>Source Register (rs1): (00000 5 bits)<br>
<li>Destination Register (rd): a2 (x12, 5 bits)<br>
<li>Function (funct3): 000 (3 bits)<br>

### Breakdown:<br>
<li>Immediate (12 bits): 0000 1101 0010<br>
<li>rs1: 00000<br>
<li>funct3: 000<br>
<li>rd (a2 = x12): 01100<br>
<li>Opcode: 0010011<br>

### Machine Code:<br>
<li>Binary: 0000 1101 0010 0000 0000 0110 0001 0011<br>
<li>Hex: 0d200613<br>

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/e97828aa-c277-40a6-9bf5-dbeeb4bff6fa" /><br>
### 4) Instruction: li a1, 20<br>
<li>Opcode: 0010011 (7 bits)<br>
<li>Immediate: 20 (12 bits)<br>
<li>Source Register (rs1): (00000 5 bits)<br>
<li>Destination Register (rd): a1 (x11, 5 bits)<br>
<li>Function (funct3): 000 (3 bits)<br>

### Breakdown:<br>
<li>Immediate (12 bits): 0000 0001 0100<br>
<li>rs1: 00000<br>
<li>funct3: 000<br>
<li>rd (a1 = x11): 01011<br>
<li>Opcode: 0010011<br>

### Machine Code:<br>
<li>Binary: 0000 0001 0100 0000 0000 0101 1001 0011<br>
<li>Hex: 01400593<br>
