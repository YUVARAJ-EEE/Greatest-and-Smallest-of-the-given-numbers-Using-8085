# Greatest-and-Smallest-of-the-given-numbers-Using-8085

## Aim:

To write 8085 microprocessor programs to find the greatest and smallest number from the given 8-bit numbers.

## Apparatus Required:

•	Laptop with an internet connection

## Finding the Greatest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the greatest).
3.	Load the next number and compare it with A.
4.	If the new number is greater, update A.
5.	Repeat the process for all numbers.
6.	Store the greatest number in 4300H.

## Program:
```
LDA 4200H
MOV C,A
LXI H,4201H
MOV A,M
INX H
DCR C
LOOP:CMP M
JNC NEXT
MOV A,M
NEXT:INX H
DCR C
JNZ LOOP
STA 4300H
HLT
```
## Theory:
![WhatsApp Image 2026-02-13 at 6 07 56 PM](https://github.com/user-attachments/assets/d273ae02-ac89-434a-9697-5f05f6bdbf41)
![WhatsApp Image 2026-02-13 at 6 07 57 PM](https://github.com/user-attachments/assets/db5eeaa3-6c26-4335-9ba3-0bc6e5db591a)
![WhatsApp Image 2026-02-13 at 6 07 57 PM (1)](https://github.com/user-attachments/assets/83dea688-23b3-4f2e-9b7a-2725f2725085)

## Output:
<img width="1872" height="897" alt="Screenshot 2026-02-13 151728" src="https://github.com/user-attachments/assets/55826b6f-58ae-4f3b-807f-e94c5817b49d" />

<img width="1870" height="895" alt="Screenshot 2026-02-13 151836" src="https://github.com/user-attachments/assets/9c5413a4-8faa-4038-b174-cd6d6edc2c47" />

## Finding the Smallest Number

## Algorithm:

1.	Load the count of numbers from memory location 4200H into register C.
2.	Load the first number from 4201H into register A (Assume it as the smallest).
3.	Load the next number and compare it with A.
4.	If the new number is smaller, update A.
5.	Repeat the process for all numbers.
6.	Store the smallest number in 4301H.

## Program:
```
LDA 4200H
MOV C,A
LXI H,4201H
MOV A,M
INX H
DCR C
LOOP:CMP M
JC NEXT
MOV A,M
NEXT:INX H
DCR C
JNZ LOOP
STA 4301H
HLT
```
## Theory:
![WhatsApp Image 2026-02-13 at 6 11 56 PM](https://github.com/user-attachments/assets/2ba7dad2-b075-4804-b3a1-13dc19e64e74)
![WhatsApp Image 2026-02-13 at 6 11 57 PM](https://github.com/user-attachments/assets/f67cd322-87c8-4232-bd31-bb9e611650c3)
![WhatsApp Image 2026-02-13 at 6 11 57 PM (1)](https://github.com/user-attachments/assets/ad78e551-86d9-4d73-9d09-bd6f9622cbd8)

## Output:

<img width="1877" height="891" alt="Screenshot 2026-02-13 153547" src="https://github.com/user-attachments/assets/955371cd-1b3a-4fea-8ebd-d931201c0dc6" />
<img width="1872" height="892" alt="Screenshot 2026-02-13 153605" src="https://github.com/user-attachments/assets/4f043a5a-fd17-4bb9-bbcc-098fa001e2cd" />

## Result:

The 8085 microprocessor successfully finds the greatest and smallest numbers from multiple inputs and stores them in memory.
