
# SORTING---8051

**AIM:**

To write and execute Assembly language Program for sorting of data using 8051 keil.

**APPARATUS REQUIRED: Personal computer with Keil software**

**(i) Descending order ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is low, then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H 

MOV R6,#04

LOOP: MOV A,@R0 

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT 

SJMP DOWN 

NEXT:JNC DOWN 

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END


**OUTPUT:**
INPUT 
![WhatsApp Image 2025-10-30 at 22 58 53_e6d851d5](https://github.com/user-attachments/assets/a757a03f-7528-4434-afb9-cc0dd67bbc9a)
OUTPUT
![WhatsApp Image 2025-10-30 at 22 58 04_7f94d32c](https://github.com/user-attachments/assets/cf93602f-1ee5-4a85-a504-2ec268a56343)

**MEMORY WINDOW:**

Before execution: D:0x40H:
<BR>
<BR>
<BR>
After execution: D:0x40H:
<BR>
<BR>
<BR>


**(ii)	Ascending order**
 
**ALGORITHM:**

1.	Initialize the register r7 with count.
2.	Get first two elements in two registers.
3.	Compare the two elements of data. If value of R0 register is high then exchange A & R0 data else increment pointer and decrement register R7.
4.	Check R7 is zero, and then move the register R0 & A.
5.	Again increment pointer and decrement R7,
6.	Check R7 is zero. If no repeat the process from step 2.
7.	Otherwise stop the program.

**PROGRAM:**

ORG 0000H 

MOV R7,#4

LOOP1:MOV R0,#40H

MOV R6,#04

LOOP: MOV A,@R0

INC R0

MOV 50H,@R0 

CJNE A,50H,NEXT

SJMP DOWN 

NEXT:JC DOWN

MOV @R0,A

DEC R0

MOV @R0,50H 

DOWN:DJNZ R6,LOOP 

DJNZ R7,LOOP1

END

**OUTPUT:**
INPUT
![WhatsApp Image 2025-10-30 at 23 29 08_c285780e](https://github.com/user-attachments/assets/671aaa10-74b8-403b-8725-2bbebd0b07f3)
OUTPUT
![WhatsApp Image 2025-10-30 at 23 28 39_157e2a4e](https://github.com/user-attachments/assets/66baafda-2f47-49db-98b2-7f3bcc9ad6bf)


**MEMORY WINDOW:** 

**Before execution:**
D:0x40H:
<BR>
<BR>
<BR>
<BR>
After execution:
D:0x40H:
<BR>
<BR>
<BR>
**Result:**

Thus the sorting of given data was done using 8051 keil and shown the output.

