# SortingNumbers-8051
## 5. Sorting of Numbers using 8051

### AIM
To write and execute an Assembly Language Program for sorting data in ascending and descending order using 8051 microcontroller on Keil software.

---

### APPARATUS REQUIRED
- Personal Computer  
- Keil µVision Software  

---

### ALGORITHM (ASCENDING ORDER)

- Initialize register R7 with count (number of elements)  
- Load first two elements into registers  
- Compare the two elements  
- If A < B → swap values  
- Else → move to next element  
- Decrement counter  
- Repeat until all elements are sorted  
- Stop the program  

---

### PROGRAM (Ascending Order)

```assembly
MOV R7,30H     
DEC R7         

LOOP1: MOV R0,#40H
       MOV R6,30H
       DEC R6

LOOP:  MOV A,@R0
       INC R0
       MOV B,@R0
       CJNE A,B,NEXT

NEXT:  JC DOWN

       MOV @R0,A
       DEC R0
       MOV @R0,B
       INC R0

DOWN:  DJNZ R6,LOOP
       DJNZ R7,LOOP1

HERE:  SJMP HERE

END
```
# OUTPUT (Ascending Order)

Number of elements stored in location 30H
![WhatsApp Image 2026-03-22 at 8 41 43 PM](https://github.com/user-attachments/assets/e83748c2-48c2-4628-bf4a-d924c1fa4cfb)


Data stored starting from 40H
![WhatsApp Image 2026-03-22 at 8 42 21 PM](https://github.com/user-attachments/assets/d62c8d22-5879-4a39-9861-a06314627a6a)


# 5.SortingNumbers-8051
sorting-of-numbers
# Aim
To write and execute an Assembly Language Program for sorting data in Ascending and descending order using 8051 microcontroller on Keil software.
# Apparatus Required
Personal Computer
Keil µVision software
# Algorithm(ASCENDING ORDER)
Initialize the register R7 with count (number of elements).
Get the first two elements into two registers.
Compare the two elements:
If the value in register R0 is lower, exchange A and R0 data.
Otherwise, increment pointer and decrement register R7.
Check if R7 = 0 → if yes, move the register R0 & A.
Increment pointer and decrement R7.
If R7 ≠ 0, repeat from Step 2.
Otherwise, stop the program.
# Program (Ascending order)
```
       MOV R7,30H     
       DEC R7         

LOOP1: MOV R0,#40H
       MOV R6,30H
       DEC R6

LOOP:  MOV A,@R0
       INC R0
       MOV B,@R0
       CJNE A,B,NEXT

NEXT:  JC DOWN

       MOV @R0,A
       DEC R0
       MOV @R0,B
       INC R0

DOWN:  DJNZ R6,LOOP
       DJNZ R7,LOOP1

HERE:  SJMP HERE

END
```

# OUTPUT(Ascending order)
Entering the number of elements to be stored in 30H

image
Entering the elements in 40H

image image image
Algorithm(Descending order)
Initialize the register R7 with count.
Get first two elements in two registers.
Compare the two elements of data:
If the value of R0 register is high, then exchange A and R0 data.
Else, increment pointer and decrement register R7.
Check if R7 = 0, then move the contents of R0 and A.
Again increment pointer and decrement R7.
Check if R7 = 0:
If No, repeat the process from Step 2.
If Yes, stop the program.
# Program (Descending order)
```
LOOP1:MOV R0,#40H
MOV R6,#04h
DEC R6
LOOP:MOV A,@R0
INC R0
MOV B,@R0
CJNE A,B,NEXT
NEXT:JNC DOWN
MOV@R0,A
DEC R0
MOV@R0,B
INC R0
DOWN:DJNZ R6,LOOP
MOV R1,#04h
DJNZ R1,LOOP1
END
```












# OUTPUT(Descending order)
![WhatsApp Image 2026-03-22 at 8 43 00 PM](https://github.com/user-attachments/assets/36348765-ec19-4429-a8d2-dab7059fb9c1)
# RESULT:
Thus the sorting of given data was done using 8051 keil software.
