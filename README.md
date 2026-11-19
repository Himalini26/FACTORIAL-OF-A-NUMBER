# FACTORIAL-OF-A-NUMBER
## FACTORIAL OF A NUMBER USING 8051 (Keil)
## AIM
To write and execute an Assembly language program to perform the factorial of a number using 8051 Keil.

## APPARATUS REQUIRED
Personal computer with Keil software

## ALGORITHM
Start
Input: Read the number n.
Initialize:
Set factorial to 1.
Set i to 1.
Loop: While i is less than or equal to n:
Multiply factorial by i.
Increment i by 1.
Output: Store or print the value of factorial.
End

## FLOWCHART
<img width="506" height="525" alt="image" src="https://github.com/user-attachments/assets/8bfd6fc3-2bde-43c0-9546-06bee2501d3b" />

## PROGRAM
ORG 0000H
MOV DPTR,#4500H
MOVX A,@DPTR
MOV R0,A
INC DPTR
ACALL FACTORIAL
MOVX @DPTR,A
SJMP THIN
FACTORIAL:DEC R0
CJNE R0,#01H,PRODUCT
SJMP THICK
PRODUCT:MOV B,R0
MUL AB
ACALL FACTORIAL
THICK: RET
THIN:RET
END

## OUTPUT
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/c804283f-b9af-4498-a340-3429fc1de882" />



## RESULT
Thus, the factorial of a number was calculated and executed successfully using 8051 Keil.
