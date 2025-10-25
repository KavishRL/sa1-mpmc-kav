# sa1-mpmc-kav

NAME: KAVISH RAJESHKUMAR

REG NO: 212224060120 

AIM
To write and execute an Assembly language program to perform the factorial of a number using 8086.

APPARATUS REQUIRED


Personal computer with dosbox software
ALGORITHM
Step-by-Step Algorithm
```

1.Start

2.Clear the AX register (AX = 0) and copy AL to BL.

3.Load SI with address 2000h.

4.Read a byte from memory address 2000h into BL (BL = [2000h]).

5.Set AL = 1 (initial multiplier for factorial).

6.Loop:

Multiply AL by BL → store the result in AX.

Decrement BL by 1.

If BL ≠ 0, repeat the loop.

7.After the loop ends, store the result in AX at memory address 3000h.

8.Trigger interrupt 3 (int 3) for debugging.

9.End
```

PROGRAM
code segment
```
assume cs:code

start:
    xor ax,ax
    mov bl,al
    mov si,2000h
    mov bl,[si]
    mov al,01h

l1:
    mul bl
    dec bl
    jnz l1

    mov si,3000h
    mov[si],ax
    int 3

code ends
end start
```
OUTPUT

<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/9c6861a0-698e-4e9e-9cff-43de911135d3" />


RESULT

Thus, the factorial of a number was calculated and executed successfully using 8086.

