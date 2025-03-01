# samsung-riscv<br>
## 📌Task 1<br>
👉C program using leafpad editor in terminal on ubuntu<br>

<img width="960" alt="Screenshot 2025-01-06 192801" src="https://github.com/user-attachments/assets/f20799a3-58dc-474f-8e15-5aa4c79c781c" /><br>

👉c program code converted into assembly code<br>

<img width="960" alt="Screenshot 2025-01-07 213158" src="https://github.com/user-attachments/assets/1a542484-203d-4cdb-8498-aeb32e441237" /><br>
<img width="960" alt="Screenshot 2025-01-07 213352" src="https://github.com/user-attachments/assets/a2eca722-0ae6-4bb3-80f2-d3f9a9567b98" /><br>
<img width="960" alt="Screenshot 2025-01-07 213704" src="https://github.com/user-attachments/assets/77471fee-77e3-4555-9483-d2102e7dd644" /><br>


## 📌Task 2

### Run the simulation and observe the performance under the -O1 and -Ofast compiler optimization flags.<br>

👉-Ofast compiler optimization flag is used and debugging using the spike debugger<br>

<img width="960" alt="Screenshot 2025-01-12 094244" src="https://github.com/user-attachments/assets/95701be4-f5ed-40a8-a497-0add69554240" /><br>

👉-Ofast compiler optimization flag assembly code<br>

<img width="960" alt="Screenshot 2025-01-12 102118" src="https://github.com/user-attachments/assets/8cfb70d0-888c-4fe8-a1c4-86d1089a7cc6" /><br>

👉-O1 compiler optimization flag is used and debugging using the spike debugger<br>
<img width="960" alt="Screenshot 2025-01-12 101933" src="https://github.com/user-attachments/assets/f53b350b-5b17-4195-ba47-65e8abeb64cf" /><br>

👉-O1 compiler optimization flag assembly code<br>
<img width="960" alt="Screenshot 2025-01-12 102002" src="https://github.com/user-attachments/assets/657eddd6-d914-4981-b289-03d1971ff321" /><br>

## 📌Task 3
👉understand the R, I, S, B, U, and J instruction types.<br>
<li>R-type: Register type<br>
<li>I-type: Immediate type<br>
<li>S-type: Store type<br>
<li>B-type: Branch type<br>
<li>U-type: Upper immediate type<br>
<li>J-type: Jump type<br>
  
  <img width="531" alt="Image" src="https://github.com/user-attachments/assets/42c1083a-dd94-48bf-bf06-67472156d28d" /><br>
👉For those 15 instructions, determine the exact 32-bit instruction code in their respective instruction type formats.<br>

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

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/89880eec-a7fe-465d-813e-03e72c99ae06" /><br>
### 12) Instruction: addi a5, a5, -220<br>
<li>Opcode: 0010011 (7 bits)<br>
<li>Immediate: -220 (12 bits)<br>
<li>Source Register (rs1): a5 (x15, 5 bits)<br>
<li>Destination Register (rd): a5 (x15, 5 bits)<br>
<li>Function (funct3): 000 (3 bits)<br>

### Breakdown:<br>
<li>Immediate (12 bits): 1111 0100 0100 <br>
<li>rs1 (a5 = x15): 01111<br>
<li>funct3: 000<br>
<li>rd (a5 = x15): 01111<br>
<li>Opcode: 0010011<br>

### Machine Code:<br>
<li>Binary: 1111 0100 0100 0111 1000 0111 1001 0011<br>
<li>Hex: f2478793<br>

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/bbbbb0ef-cdc6-4140-821a-c2b67cb4ee0b" /><br>
### 13) Instruction: beqz a5, 100f4(sp)<br>
<li>Opcode: 1100011 (7 bits)<br>
<li>Immediate: 100f4(12 bits)<br>
<li>Destination Register (rd): a5 (x15, 5 bits)<br>
<li>funct3: 000<br>
  
### Machine Code:<br>
<li>Binary:  0000 0000 0000 0111 1000 1000 0110 0011 <br>
<li>Hex: 00078863<br>

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/d1316c6e-907a-47bb-8274-455e1edb9056" /><br>
### 14) Instruction: auipc a0, 0x0<br>
<li>Opcode: 0010111 (7 bits)<br>
<li>Immediate: 0x0(20 bits)<br>
<li>Destination Register (rd): a0 (x10, 5 bits)<br>

### Breakdown:<br>
<li>Immediate (20 bits): 0000 0000 0000 0000 0000 <br>
<li>rd (a0 = x10): 01111<br>
<li>Opcode: 0010111<br>

### Machine Code:<br>
<li>Binary: 0000 0000 0000 0000 0000 0101 0001 0111<br>
<li>Hex: 00000517<br>

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/51651d5a-0b5e-4bc7-8140-c59ceff17a77" /><br>
### 15) Instruction: addi a0, a0, 272<br>
<li>Opcode: 0010011 (7 bits)<br>
<li>Immediate: 272 (12 bits)<br>
<li>Source Register (rs1): a0 (x10, 5 bits)<br>
<li>Destination Register (rd): a0 (x10, 5 bits)<br>
<li>Function (funct3): 000 (3 bits)<br>

### Breakdown:<br>
<li>Immediate (12 bits): 0001 0001 0000  <br>
<li>rs1 (a0 = x10): 01010<br>
<li>funct3: 000<br>
<li>rd (a0 = x10): 01010<br>
<li>Opcode: 0010011<br>

### Machine Code:<br>
<li>Binary:0001 0001 0000 0101 0000 0101 0001 0011<br>
<li>Hex: 11050513<br>

## 📌Task 4
### 👉Functional Simulation of RISC-V Core
### Set Up Simulation Environment:<br>
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/42e468ef-b947-4dd2-b13e-02bc8d2e784e" /><br>
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/904e09b8-b649-467c-b5c1-fcc7d44f49ae" /><br>
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/021ab6b0-3aa3-4c35-a1e2-834c38dc6f2e" /><br>
### 👉Run Functional Simulation:
NOTE<br>
<li>ID_EX_A`: Register A.<br>
<li>ID_EX_B`: Register B.<br>
Memory Stage<br>
<li>EX_MEM_IR`: Instruction Register.<br>
Execution Stage<br>
<li>EX_MEM_ALUOUT`: ALU output.<br>
  
### HARDCODED ISA
<li>MEM[0] <= 32'h02208300;         // add r6,r1,r2.(i1)<br>
<li>MEM[1] <= 32'h02209380;         //sub r7,r1,r2.(i2)<br>
<li>MEM[2] <= 32'h0230a400;         //and r8,r1,r3.(i3)<br>
<li>MEM[3] <= 32'h02513480;         //or r9,r2,r5.(i4)<br>
<li>MEM[4] <= 32'h0240c500;         //xor r10,r1,r4.(i5)<br>
<li>MEM[5] <= 32'h02415580;         //slt r1,r2,r4.(i6)<br>
<li>MEM[6] <= 32'h00520600;         //addi r12,r4,5.(i7)<br>
<li>MEM[7] <= 32'h00209181;         //sw r3,r1,2.(i8)<br>
<li>MEM[8] <= 32'h00208681;         //lw r13,r1,2.(i9)<br>
  
## 📍ADD
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/a8237edf-f024-4f70-b71e-d0cfe529eb68" /><br>
### Values Stored in Two Different Registers:
<li>The waveform indicates that the values 1 and 2 are stored in registers r1 and r2 respectively (ID_EX_A and ID_EX_B).<br>
  
### 32-bit Instruction for ADD R6, R2, R1:
<li>The instruction 0x02208300 represents the operation add r6, r1, r2. This instruction tells the processor to add the values in registers r1 and r2 and store the result in register r6.<br>

### Output of ADD Operation:
<li>The ALU performs the addition 1 + 2, resulting in 3, which is shown in the EX_MEM_ALUOUT signal.<br>

## 📍SUB
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/8c3a8131-6a26-4777-9dbe-b44ee129ab07" /><br>
### Values Stored in Registers:
<li>ID_EX_A holds 1, corresponding to the value in register R1.<br>
<li>ID_EX_B holds 2, corresponding to the value in register R2.<br>
  
### Instruction Fetching:<br>
<li>EX_MEM_IR signal shows the value 0x02209380, which is the 32-bit instruction for SUB R7, R1, R2.<br>
  
### ALU Operation:<br>
<li>The output of the ALU operation EX_MEM_ALUOUT shows F. This is the result of the subtraction operation 1 & 2:<br>
<li>1 in binary is 0001<br>
<li>2 in binary is 0010<br>
<li>subtraction of 0001 - 0010 results in FFFF, which is F in hexadecimal.<br>
  
## 📍AND
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/2a2c9a5e-db77-4278-a8eb-51e3ba7d4385" /><br>
### Values Stored in Registers:
<li>ID_EX_A holds 1, corresponding to the value in register R1.<br>
<li>ID_EX_B holds 3, corresponding to the value in register R3.<br>
  
### Instruction Fetching:<br>
<li>EX_MEM_IR signal shows the value 0x0230A400, which is the 32-bit instruction for AND R8, R1, R3.<br>
  
### ALU Operation:<br>
<li>The output of the ALU operation EX_MEM_ALUOUT shows 1. This is the result of the bitwise AND operation 3 & 1:<br>
<li>3 in binary is 0011<br>
<li>1 in binary is 0001<br>
<li>Bitwise AND of 0011 & 0001 results in 0001, which is 1 in decimal.<br>
  
## 📍OR
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/91cd8741-8feb-4cea-b2d4-73ded3f1a15c" /><br>
### Values Stored in Registers:
<li>ID_EX_A holds 2, corresponding to the value in register R2.<br>
<li>ID_EX_B holds 5, corresponding to the value in register R5.<br>
  
### Instruction Fetching:<br>
<li>EX_MEM_IR signal shows the value 0x02513480, which is the 32-bit instruction for AND R9, R2, R5.<br>
  
### ALU Operation:<br>
<li>The output of the ALU operation EX_MEM_ALUOUT shows 1. This is the result of the bitwise OR operation 2 & 5:<br>
<li>2 in binary is 0010<br>
<li>5 in binary is 0101<br>
<li>The bitwise OR operation (0010 | 0101) results in 7 (binary: 0111)..<br>
  
## 📍XOR
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/0157426e-1dbe-4351-87f0-023bee90b0ed" /><br>
### Values Stored in Registers:
<li>ID_EX_A holds 1, corresponding to the value in register R1.<br>
<li>ID_EX_B holds 4, corresponding to the value in register R4.<br>
  
### Instruction Fetching:<br>
<li>EX_MEM_IR signal shows the value 0x0240c500, which is the 32-bit instruction for XOR R10, R1, R4.<br>
  
### ALU Operation:<br>
<li>The output of the ALU operation EX_MEM_ALUOUT shows 5. This is the result of the bitwise OR operation 1 & 4:<br>
<li>1 in binary is 0001<br>
<li>4 in binary is 0100<br>
<li>The bitwise XOR operation (0001 ^ 0100) results in 5 (binary: 0101)..<br>

 ## 📍SLT 
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/45ccfe89-9514-47fb-9924-02a76b00b5d5" /><br>
### Instruction: SLT R1, R2, R4<br>
<li>This instruction performs a "Set Less Than" (SLT) operation. It compares the values in registers R2 and R4 and sets the destination register R1 to 1 if the value in R2 is less than the value in R4; otherwise, it sets R1 to 0.<br>
  
### Waveform Signals:<br>
<li>EX_MEM_IR[31:0]: The instruction register for the Execution/Memory (EX/MEM) pipeline stage, holding the 32-bit instruction 0x02415580.<br>
<li>ID_EX_A[31:0]: The value of register R2.<br>
<li>ID_EX_B[31:0]: The value of register R4.<br>
<li>EX_MEM_ALUOUT[31:0]: The output of the Arithmetic Logic Unit (ALU) after performing the SLT operation.<br>
  
### Waveform Details:<br>
<li>Values in Registers: The values stored in R2 and R4 are 2 and 4, respectively.<br>
<li>SLT Operation: The SLT operation compares these values. Since 2 < 4, the output is 1, indicating R2 is less than R4.<br>
  
### Annotations:<br>
<li>Output of SLT will be 1: Explains that if the value in R2 is less than R4, the result will be 1; otherwise, it will be 0.<br>
<li>32 bits instruction for SLT R1, R2, R4: Shows the binary representation of the SLT instruction.<br>

## 📍ADDI
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/136b1cfa-4e2e-4305-b65f-71af7fab03d0" /><br>
### Instruction: ADDI R12, R4, 5<br>
<li>This instruction performs an "Add Immediate" (ADDI) operation. It adds the immediate value 5 to the value in register R4 and stores the result in register R12..<br>
  
### Waveform Signals:<br>
<li>EX_MEM_IR[31:0]: The instruction register for the Execution/Memory (EX/MEM) pipeline stage, holding the 32-bit instruction 0x00520600.<br>
<li>ID_EX_A[31:0]: The value of register R4.<br>
<li>ID_EX_IMMEDIATE[31:0]: The value of register 5.<br>
<li>EX_MEM_ALUOUT[31:0]: The output of the Arithmetic Logic Unit (ALU) after performing the ADDI operation.<br>
  
### Waveform Details:<br>
<li>Values in Registers and Immediate: The value stored in R4 is 4, and the immediate value is 5.<br>
<li>ADDI Operation: The ADDI operation adds these values. The result is 9, which is stored in R12..<br>
  
### Annotations:<br>
<li>Output of ADDI will be 9: Explains that the value in R4 (4) added to the immediate value (5) results in 9..<br>
<li>32 bits instruction for ADDI R12, R4, 5: Shows the binary representation of the ADDI instruction..<br>

## 📍SW                                                                                                        
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/28dd1778-5341-46d5-ab54-a917f8abc84b" /><br>
### Instruction: SW R3,R1,2<br>
<li>This instruction performs an "Store Word" (SW) operation. It stores the immediate value 2 to the value in register R1 and stores the result in register R3..<br>
  
### Waveform Signals:<br>
<li>EX_MEM_IR[31:0]: The instruction register for the Execution/Memory (EX/MEM) pipeline stage, holding the 32-bit instruction 0x00209181.<br>
<li>ID_EX_A[31:0]: The value of register R1.<br>
<li>ID_EX_IMMEDIATE[31:0]: The value of register 2.<br>
<li>EX_MEM_ALUOUT[31:0]: The output of the Arithmetic Logic Unit (ALU) after performing the SW operation.<br>
  
### Waveform Details:<br>
<li>Values in Registers and Immediate: The value stored in R1 is 1, and the immediate value is 2.<br>
<li>SW Operation: The SW operation adds these values. The result is 3, which is stored in R3..<br>

  ## 📍LW   
<img width="960" alt="Image" src="https://github.com/user-attachments/assets/b5899390-3ba7-406e-8978-c4b0391cd987" /><br>
### Instruction: LW R13,R1,2<br>
<li>This instruction performs an "Load Word" (lW) operation. It stores the immediate value 2 to the value in register R1 and stores the result in register R13..<br>
  
### Waveform Signals:<br>
<li>EX_MEM_IR[31:0]: The instruction register for the Execution/Memory (EX/MEM) pipeline stage, holding the 32-bit instruction 0x00208681.<br>
<li>ID_EX_A[31:0]: The value of register R1.<br>
<li>ID_EX_IMMEDIATE[31:0]: The value of register 2.<br>
<li>EX_MEM_ALUOUT[31:0]: The output of the Arithmetic Logic Unit (ALU) after performing the SW operation.<br>
  
### Waveform Details:<br>
<li>Values in Registers and Immediate: The value stored in R1 is 1, and the immediate value is 2.<br>
<li>LW Operation: The LW operation adds these values. The result is 3, which is stored in R13..<br>
  
## 📌Task 5<br>
This task contains documentation for the implementation of a Modulo Counter (0–7) using the VSDSquadron Mini. The project showcases the practical application of digital logic and RISC-V architecture to perform a simple counting operation with user-defined input.

### Overview
The Modulo Counter increments values from 0 up to a user-specified input (via push buttons) and resets to 0. The current state of the counter is displayed on LEDs, providing a visual representation of the operation. This project uses GPIO pins for input (push buttons) and output (LEDs), configured using the PlatformIO IDE.

### Counter Truth Table:

| Input (Binary) | Count Sequence |<br>
| -------------- | :------------- |
| 0              |  0               |<br>
| 1              |0 → 1           |<br>
| 2	             |0 → 1 → 2       |<br>
| 3	             |0 → 1 → 2 → 3   |<br>
| 4              |0 → 1 → 2 → 3 → 4 |<br>
| 5              |0 → 1 → 2 → 3 → 4 → 5 |<br>
| 6	             |0 → 1 → 2 → 3 → 4 → 5 → 6 |<br>
| 7              |0 → 1 → 2 → 3 → 4 → 5 → 6 → 7 |<br>

### Components Required

<li>VSDSquadron Mini : RISC-V based SoC development kit.<br>
<li>Push Buttons (3): For binary input (connected to GPIO pins).<br>
<li>LEDs (3): To display the counter values.<br>
<li>Breadboard and Jumper Wires: For prototyping and connections.<br>
<li>Visual Studio Code: For software development.<br>
<li>PlatformIO IDE: A professional IDE for embedded development.<br>

## Hardware Connections

## Inputs (Push Buttons):

<li>Button 1: Connected to PD3 (Least Significant Bit - LSB) ->: Rightmost button in the video<br>
<li>Button 2: Connected to PD4 (Bit 1)<br>
<li>Button 3: Connected to PD5 (Most Significant Bit - MSB) ->: Lefttmost button in the video<br>

### Outputs (LEDs):

<li>LED 1: Connected to PD0 (Least Significant Bit - LSB) ->: Yellow/ Rightmost lED in the video<br>
<li>LED 2: Connected to PD6 (Bit 1)<br>
<li>LED 3: Connected to PD2 (Most Significant Bit - MSB) ->: RED/ Leftmost lED in the video<br>

## Circuit Diagram
![Image](https://github.com/user-attachments/assets/81425b35-1e2c-4e8e-9fb6-ec19a270a140)<br>

### CODE

// Modulo counter implementation<br>
#include <ch32v00x.h>  // Include the register definitions for the CH32V003<br>

// LED Pin Definitions (connected to PD0, PD6, PD2)<br>
#define LED1 GPIO_Pin_0  // LED 1 (LSB) - PD0<br>
#define LED2 GPIO_Pin_6  // LED 2 (Bit 1) - PD6<br>
#define LED3 GPIO_Pin_2  // LED 3 (MSB) - PD2<br>

// Push Button Pin Definitions (connected to PD3, PD4, PD5)<br>
#define BTN1 GPIO_Pin_3  // Push Button 1 (LSB) - PD3<br>
#define BTN2 GPIO_Pin_4  // Push Button 2 (Bit 1) - PD4<br>
#define BTN3 GPIO_Pin_5  // Push Button 3 (MSB) - PD5<br>

void GPIO_Config(void);<br>
void Delay(uint32_t delay);<br>
uint8_t Read_Button_Input(void);<br>

int main(void)<br>
{
    uint8_t target_value = 0;  // Holds the binary input value (0–7)<br>
    uint8_t counter = 0;       // Current counter value<br>
    SystemInit();      // System initialization<br>
    GPIO_Config();     // Configure GPIO for LEDs and buttons<br>

  // Initialize LEDs to OFF state (PD0, PD6, PD2 are all LOW)<br>
    GPIO_WriteBit(GPIOD, LED1, Bit_RESET);  // LED1 (PD0) OFF<br>
    GPIO_WriteBit(GPIOD, LED2, Bit_RESET);  // LED2 (PD6) OFF<br>
    GPIO_WriteBit(GPIOD, LED3, Bit_RESET);  // LED3 (PD2) OFF<br>

   while (1)<br>
   {
        // Read the input from the 3 push buttons (binary value 0–7)<br>
        target_value = Read_Button_Input();<br>

   // Wait until the user releases the buttons after holding<br>
        while (GPIO_ReadInputDataBit(GPIOD, BTN3) || GPIO_ReadInputDataBit(GPIOD, BTN2) || GPIO_ReadInputDataBit(GPIOD, BTN1));<br>

   // Run the counter from 0 to the target value<br>
        while (counter <= target_value)<br>
        {<br>
            // Display the current counter value on LEDs<br>
            GPIO_WriteBit(GPIOD, LED1, (counter & 0x01) ? Bit_SET : Bit_RESET);<br>
            GPIO_WriteBit(GPIOD, LED2, (counter & 0x02) ? Bit_SET : Bit_RESET);<br>
            GPIO_WriteBit(GPIOD, LED3, (counter & 0x04) ? Bit_SET : Bit_RESET);<br>
    Delay(5000000);  // Wait 5 seconds for each count (5000000 cycles)<br>
            counter++;  // Increment the counter<br>
        }<br>
    // Once the counter reaches the target value, stop the counting<br>
        // All LEDs will stay at the final state<br>
    // Reset counter for the next input<br>
        counter = 0;<br>

   // Add a small delay before accepting the next input<br>
    Delay(1000000);  // 1-second delay before the next input<br>
    }<br>
}<br>

void GPIO_Config(void)<br>
{
    GPIO_InitTypeDef GPIO_InitStructure = {0};<br>
   // Enable clocks for GPIOD<br>
    RCC_APB2PeriphClockCmd(RCC_APB2Periph_GPIOD, ENABLE);<br>

  // Configure LEDs (PD0, PD6, PD2) as outputs<br>
    GPIO_InitStructure.GPIO_Pin = LED1 | LED2 | LED3;<br>
    GPIO_InitStructure.GPIO_Speed = GPIO_Speed_50MHz;<br>
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_Out_PP;  // Push-pull output<br>
    GPIO_Init(GPIOD, &GPIO_InitStructure);<br>

   // Configure push buttons (PD3, PD4, PD5) as inputs with pull-down resistors<br>
    GPIO_InitStructure.GPIO_Pin = BTN1 | BTN2 | BTN3;<br>
    GPIO_InitStructure.GPIO_Mode = GPIO_Mode_IPD;  // Input with pull-down<br>
    GPIO_Init(GPIOD, &GPIO_InitStructure);<br>
}<br>

void Delay(uint32_t delay)<br>
{<br>
    while (delay--)<br>
        __NOP();  // Simple delay loop<br>
}<br>

uint8_t Read_Button_Input(void)<br>
{<br>
    // Read the input from the 3 push buttons (binary value 0-7)<br>
    uint8_t input = 0;<br>
    if (GPIO_ReadInputDataBit(GPIOD, BTN3) == Bit_SET) {<br>
        input |= 0x04;  // Set bit 2 if BTN3 is pressed (4)<br>
    }<br>
    if (GPIO_ReadInputDataBit(GPIOD, BTN2) == Bit_SET) {<br>
        input |= 0x02;  // Set bit 1 if BTN2 is pressed (2)<br>
    }<br>
    if (GPIO_ReadInputDataBit(GPIOD, BTN1) == Bit_SET) {<br>
        input |= 0x01;  // Set bit 0 if BTN1 is pressed (1)<br>
    }<br>

   return input;  // Return the binary input (0 to 7)<br>
}<br>

## DEMO VIDEO
https://drive.google.com/file/d/169gyW3IAZtgoplCMon605uEg4xyYkEJX/view?usp=sharing<br>
