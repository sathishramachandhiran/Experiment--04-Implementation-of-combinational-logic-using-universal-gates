# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
1.Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.

## Program:

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: SATHISH R
RegisterNumber:22009045  
```
## PROGRAM 1
module expfour(a,b,c,d,f);
input a,b,c,d;
output f;
wire f1,f2,f3;
assign f1 = (~c&~b&~a);
assign f2 = (~d&~c&~a);
assign f3 = (c&~(~b)&~a);
assign f= f1&~f2&~f3;
endmodule
```
```
## PROGRAM 2
module expfourtwo(a,b,c,d,f);
input a,b,c,d;
output f;
wire f1,f2,f3,f4;
assign f1 = c&(~b)&a;
assign f2 = d&(~c)&a;
assign f3 = c&(~b)&a;
assign f4 = ~(f1|f2|f3);
not(f,f4);
endmodule
```

## Output:

## RTL
## PROGRAM 1
![f1 rtl](https://user-images.githubusercontent.com/120574768/211187794-08f839a3-3526-4f0a-9b88-25337aceb8c0.png)

# PROGRAM 2

![f2 rtl](https://user-images.githubusercontent.com/120574768/211187793-0b5c015d-2ca9-4ae9-95a6-593894f9302d.png)

## Timing Diagram
## PROGRAM 1
![f1 td](https://user-images.githubusercontent.com/120574768/211187815-4f61f7ee-45c9-4bd4-a51a-189fab6fca13.png)

## PROGRAM 2
![f2 td](https://user-images.githubusercontent.com/120574768/211187817-c2db30b1-9c37-48ec-a82f-0e2b26eb1cbb.png)

## TRUTH TABLE
## PROGRAM 1
![f1 tt](https://user-images.githubusercontent.com/120574768/211187830-a2b12d4a-0480-47de-a24a-816eb3b03159.png)

## PROGRAM 2
![f2 tt](https://user-images.githubusercontent.com/120574768/211187833-46a01e0d-3345-4f11-aaa5-d7e7d85b0077.png)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
