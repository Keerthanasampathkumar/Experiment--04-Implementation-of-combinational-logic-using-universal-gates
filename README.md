# Experiment--02-Implementation-of-combinational-logic-using-universal-gates
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

## Procedure
Step 1:
Create a project with required entities.

Step 2:
Create a module along with respective file name.

Step 3:
Run the respective programs for the given boolean equations.

Step 4:
Run the module and get the respective RTL outputs.

Step 5:
Create university program(VWF) for getting timing diagram.

Step 6:
Give the respective inputs for timing diagram and obtain the results.
## Program:
/*

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.

Developed by: KEERTHANA S

RegisterNumber: 212222230066

### Using NAND operation
module fourexp(A,B,C,D,F);  
input A,B,C,D;  
output F;  
wire P,Q,R;  
assign P = C&(~B)&(~A);  
assign Q = D&(~C)&(~A);  
assign R = (~C)&B&(~A);  
assign F = (~P&~Q&~R);  
endmodule 

### Using NOR operation
module fourexp(A,B,C,D,F);  
input A,B,C,D;  
output F;  
wire P,Q,R,S;  
assign P = C&(~B)&A;  
assign Q = D&(~C)&A;  
assign R = C&(~B)&A;  
assign S = ~(P|Q|R);  
assign F = ~S;  
endmodule  
*/
## RTL realization
### For NAND
![p1](https://user-images.githubusercontent.com/119477890/231795577-b4dc2fc9-a3ae-4cb2-ab55-ad3cd386f421.png)
### For NOT
![p2](https://user-images.githubusercontent.com/119477890/231795621-f9f86733-6f8e-4da2-bd1d-40fd5e7c388b.png)

## Output:
## Timing Diagram:
### For NAND
![p3](https://user-images.githubusercontent.com/119477890/231795987-1afc97a9-67ca-452a-90ee-04b3b277d7cf.png)
### For NOR
![p4](https://user-images.githubusercontent.com/119477890/231796015-cb49b423-368a-4c42-a4cb-c13ae96d3a8b.png)

### TRUTHTABLE
### For NAND
![p5](https://user-images.githubusercontent.com/119477890/231796156-998ed3d4-cfe8-4a53-a874-2da6b718adde.png)
### For NOR
![p6](https://user-images.githubusercontent.com/119477890/231796366-a2dd9936-5408-49e4-b427-8ffd8e61f779.png)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
