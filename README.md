# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1200 : 12           |      1204 : 24           |
1201 : 34  |  1205 : 68
1202 : 12   | 1206 : 00
1203 : 34    |1207 : C4

#### Manual Calculations
![WhatsApp Image 2025-08-24 at 23 22 25_f5a06965](https://github.com/user-attachments/assets/87f2d114-e0af-49e2-ab0e-528f6140be23)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/c44f33b2-adc0-4ebf-9c81-3c52f4fb7860" />

## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
SUB AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```


#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|               1200 : 12          |      1204 : 00                    |
1201 : 34 | 1205 : 00
1202 : 12 | 1206 : 00
1203 : 34 | 1207 : C4

#### Manual Calculations

![WhatsApp Image 2025-08-24 at 23 22 26_f2e4c0a5](https://github.com/user-attachments/assets/6ca32c14-5a80-4fb7-a318-453ea0d71353)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/7cea47dc-44d5-4f14-87b0-6b9751310777" />

## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200 : 12                |       1204 : 44                   |
1201 : 34 | 1205 : 51
1202 : 12 | 1206 : 97
1203 : 34 | 1207 : 0A

#### Manual Calculations
![WhatsApp Image 2025-08-24 at 23 24 07_9e652b40](https://github.com/user-attachments/assets/d2bb58b2-43e0-4379-a8e0-345eb2f32998)



## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/1aacb66b-f70f-4c9b-a8ed-247566b3f6e5" />

## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table


| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200 : 12                  |              1204 : 01            |
1201 : 34 | 1205 : 00
1202 : 12 | 1206 : 00
1203 : 34 | 1207 : 00

#### Manual Calculations

![WhatsApp Image 2025-08-24 at 23 22 26_a7f2d797](https://github.com/user-attachments/assets/47d769b3-f066-4cce-a4fe-834f8cfc39f2)


---
## OUTPUT FROM MASM SOFTWARE
<img width="640" height="480" alt="Screenshot (13)" src="https://github.com/user-attachments/assets/5ff99a62-05b6-4b4a-aabb-245413645d81" />



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
