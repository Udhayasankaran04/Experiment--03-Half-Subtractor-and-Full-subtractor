# Experiment--04-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure



Write the detailed procedure here 


## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: UDHAYA SANKARAN M 
RegisterNumber: 212222110051


## Output:

## HALF SUBTRACTOR
```
module HALF_SUB(a,b,di,bo);
input a,b;
output di,bo;
assign di=(a^b);
assign bo=((~a)&b);
endmodule 
```

## FULL SUBTRACTOR
```
module FULL_SUB(a,b,bin,di,bo);
input a,b,bin;
output di,bo;
assign di=a^b^bin;
assign bo=((~a&b))|(b&bin)|((~a)&bin);
endmodule
```
## Truthtable
## HALF SUBTRACTOR
![image](https://github.com/Udhayasankaran04/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119393933/fe7d7ece-347d-4628-8387-2b20f2341b7c)
## FULL SUBTRACTOR
![image](https://github.com/Udhayasankaran04/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119393933/36340f80-1a90-4213-8946-98b747ea3f40)

##  RTL realization
## HALF SUBTRACTOR
![image](https://github.com/Udhayasankaran04/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119393933/f5f29085-01cd-409a-85b6-ad1418552378)
## FULL SUBTRACTOR
![image](https://github.com/Udhayasankaran04/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119393933/4eb135ac-a1e9-4bae-88bc-c304f899bd59)

## Timing diagram 
## HALF SUBTRACTOR
![image](https://github.com/Udhayasankaran04/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119393933/edc2f1f2-ed83-4552-9526-7cd97e594998)

## FULL SUBTRACTOR
![image](https://github.com/Udhayasankaran04/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119393933/f07b4d3a-273b-4a1d-9a79-877cd58dd0ec)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
