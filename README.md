NAME: JISHNUPRIYAN S

REFERENCE NUMBER: 23008936
# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

#### Figure -01 HALF ADDER 
![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

### Procedure

Connect the supply (+5V) to the circuit switch ON the main switch .If the output is 1, then the led glows.

### Program:
/*Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
```module exp3(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```
## RTL Realisation:
![Screenshot 2023-12-18 122410](https://github.com/jishnusankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979369/4b99f9aa-97df-47bd-93fd-10d67fde4f65)

## TIMING DIAGRAM:
![Screenshot 2023-12-18 122601](https://github.com/jishnusankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979369/37a66d69-d43e-46b3-844e-56478b80631c)

## TRUTH TABLE:
![Screenshot 2023-12-18 122623](https://github.com/jishnusankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979369/ce8fa62d-e469-481e-bbff-8ca43075be62)


### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

#### Figure -02 FULL ADDER
![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

## Program:
```
module exp3(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b | b&c | a&c;
endmodule
```

## RTL Realisation:
![Screenshot 2023-12-18 122521](https://github.com/jishnusankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979369/4e136a91-f09d-44a6-a73c-924d2978657c)

## TIMING DIAGRAM


![Screenshot 2023-12-18 122645](https://github.com/jishnusankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979369/d305e1c7-b652-47df-a34e-d0bd4cb4ca0c)


## TRUTH TABLE
![Screenshot 2023-12-18 122658](https://github.com/jishnusankaran/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144979369/c2848792-e393-4d8b-94a7-dcb10b4dc1ca)


### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming
