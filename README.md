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

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/aedcd37c-07ba-4693-b57e-408697b37505" /><br>
### 5) Instruction: addi a0, a0, 384<br>
<li>Opcode: 0010011 (7 bits)<br>
<li>Immediate: 384 (12 bits)<br>
<li>Source Register (rs1): a0 (x10, 5 bits)<br>
<li>Destination Register (rd): a0 (x10, 5 bits)<br>
<li>Function (funct3): 000 (3 bits)<br>

### Breakdown:<br>
<li>Immediate (12 bits): 0001 1000 0000<br>
<li>rs1 (a0 = x10): 01010<br>
<li>funct3: 000<br>
<li>rd (a0 = x10): 01010<br>
<li>Opcode: 0010011<br>

### Machine Code:<br>
<li>Binary: 0001 1000 0000 0101 0000 0101 0001 0011<br>
<li>Hex: 18050513<br>

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/80338182-445a-4dde-86a1-83f38cf968e6" /><br>
### 6) Instruction: sd ra, 8(sp)<br>
<li>Opcode: 0100011 (7 bits)<br>
<li>Immediate: 8 (12 bits, split into two parts: imm[11:5] and imm[4:0])<br>
<li>Source Register (rs2): ra (x1, 5 bits)<br>
<li>Base Register (rs1): sp (x2, 5 bits)<br>
<li>Function (funct3): 011 (3 bits)<br>
  
### Breakdown:<br>
<li>Immediate (8): 000000001000 (split into imm[11:5] = 0000000 and imm[4:0] = 01000)<br>
<li>rs2 (ra = x1): 00001<br>
<li>rs1 (sp = x2): 00010<br>
<li>funct3: 011<br>
<li>Opcode: 0100011<br>

### Machine Code:<br>
<li>Binary:  0000 0000 0001 0001 0011 0100 0010 0011 <br>
<li>Hex: 00113423<br>

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/cfab5b3b-1884-4904-90c0-71c7f723802d" /><b>
### 7) Instruction: jal ra, 10408(sp)<br>
<li>Opcode: 1101111 (7 bits)<br>
<li>Immediate: 10408 (20 bits)<br>
<li>Destination Register (rd): ra (x1, 5 bits)<br>

### Machine Code:<br>
<li>Binary:  0011 0100 0000 0000 0000 0000 1110 1111 <br>
<li>Hex: 340000ef<br>

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/b924293b-04c6-442b-99d3-4e9a04fcc94c" /><br>
### 8) Instruction: ld ra, 8(sp)<br>
<li>Opcode: 0000011 (7 bits)<br>
<li>Immediate: 8 (12 bits)<br>
<li>Source Register (rs1): sp (x2, 5 bits)<br>
<li>Destination Register (rd): ra (x1, 5 bits)<br>
<li>Function (funct3): 000 (3 bits)<br>
  
### Breakdown:<br>
<li>Immediate (8): 000000001000 <br>
<li>rd (ra = x1): 00001<br>
<li>rs1 (sp = x2): 00010<br>
<li>funct3: 011<br>
<li>Opcode: 0000011<br>

### Machine Code:<br>
<li>Binary:  0000 0000 1000 0001 0011 0000 1000 0011 <br>
<li>Hex: 00813083<br>

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/d32bf05a-f484-46fc-aaeb-858b46a4ba96" /><br>
### 9) Instruction: li a0, 0<br>
<li>Opcode: 0010011 (7 bits)<br>
<li>Immediate: 0 (12 bits)<br>
<li>Source Register (rs1): (00000 5 bits)<br>
<li>Destination Register (rd): a0 (x10, 5 bits)<br>
<li>Function (funct3): 000 (3 bits)<br>

### Breakdown:<br>
<li>Immediate (12 bits): 0000 0000 0000<br>
<li>rs1: 00000<br>
<li>funct3: 000<br>
<li>rd (a0 = x10): 01010<br>
<li>Opcode: 0010011<br>

### Machine Code:<br>
<li>Binary: 0000 0000 0000 0000 0000 0101 0001 0011<br>
<li>Hex: 00000513<br>

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/9bcc19af-cd39-40df-8128-0e9ad2b9e626" /><br>
### 10) Instruction: addi sp, sp, 16<br>
<li>Opcode: 0010011 (7 bits)<br>
<li>Immediate: 16 (12 bits)<br>
<li>Source Register (rs1): sp (x2, 5 bits)<br>
<li>Destination Register (rd): sp (x2, 5 bits)<br>
<li>Function (funct3): 000 (3 bits)<br>

### Breakdown:<br>
<li>Immediate (12 bits): 0000 0001 0000<br>
<li>rs1 (sp = x2): 00010<br>
<li>funct3: 000<br>
<li>rd (sp = x2): 00010<br>
<li>Opcode: 0010011<br>

### Machine Code:<br>
<li>Binary: 0000 0001 0000 0001 0000 0001 0001 0011<br>
<li>Hex: 01010113<br>

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/cb261b34-61f7-4a37-92a6-94c9e4e344bf" /><br>
### 11) Instruction: auipc a5, 0xffff0<br>
<li>Opcode: 0010111 (7 bits)<br>
<li>Immediate: 0xffff0 (20 bits)<br>
<li>Destination Register (rd): a5 (x15, 5 bits)<br>

### Breakdown:<br>
<li>Immediate (20 bits): 1111 1111 1111 1111 0000 <br>
<li>rd (a5 = x15): 01111<br>
<li>Opcode: 0010111<br>

### Machine Code:<br>
<li>Binary: 1111 1111 1111 1111 0000 0111 1001 0111<br>
<li>Hex: ffff0797<br>
