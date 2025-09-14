
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
|                         |                          |

#### Manual Calculations

<img width="1222" height="879" alt="Screenshot 2025-09-14 175319" src="https://github.com/user-attachments/assets/652be0ef-21d7-4cd1-b283-f514b4002abb" />


## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-09-14 at 17 47 09_d86349e5](https://github.com/user-attachments/assets/f85ab38e-89d2-4d7f-8e10-642026f8aba3)
![WhatsApp Image 2025-09-14 at 17 47 10_7fdf72ac](https://github.com/user-attachments/assets/5ebf633a-c767-4a04-a8db-8d711416e34d)



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
|                         |                          |

#### Manual Calculations

<img width="1065" height="782" alt="Screenshot 2025-09-14 175330" src="https://github.com/user-attachments/assets/439412b5-86ef-4c1d-ad01-4dcd14a3d576" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="687" height="399" alt="Screenshot 2025-09-14 174759" src="https://github.com/user-attachments/assets/70ef06db-72cb-4b36-9fbc-aff6325836f2" />
<img width="784" height="481" alt="Screenshot 2025-09-14 174809" src="https://github.com/user-attachments/assets/064e7c24-18d5-440c-9ac3-bfef8f809c08" />



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
|                         |                          |

#### Manual Calculations

<img width="696" height="913" alt="Screenshot 2025-09-14 175404" src="https://github.com/user-attachments/assets/b131e3a9-49db-402a-b7d5-8f6bcb56ad91" />


## OUTPUT SCREEN FROM MASM SOFTWARE
<img width="769" height="453" alt="Screenshot 2025-09-14 174849" src="https://github.com/user-attachments/assets/18c545c5-3aeb-43a7-8f5b-1754822459db" />
<img width="786" height="522" alt="Screenshot 2025-09-14 174909" src="https://github.com/user-attachments/assets/0d5157fb-be3f-45e9-8027-52827736211f" />



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
|                         |                          |

#### Manual Calculations
<img width="1137" height="873" alt="Screenshot 2025-09-14 175414" src="https://github.com/user-attachments/assets/e6474f9a-676d-480c-951e-e1ed9d6bd1a1" />



## OUTPUT FROM MASM SOFTWARE
<img width="782" height="445" alt="Screenshot 2025-09-14 175000" src="https://github.com/user-attachments/assets/11416e8d-a5c8-4419-83ad-6a1e7bd5462c" />

<img width="796" height="519" alt="Screenshot 2025-09-14 175019" src="https://github.com/user-attachments/assets/e887d635-4ce6-4a88-beba-3b7e6e9b143f" />







## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.

