# Experiment--02-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime

## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Procedure
Step 1:
Create a project with required entities.

Step 2:

Create a module along with respective file name.

Step 3:

Run the respective programs for the given equations.

Step 4:

Run the module and get the respective RTL outputs.

Step 5:

Create university program(VWF) for getting timing diagram.

Step 6:

Give the respective inputs for timing diagram and obtain the results.
## Program:
/*
Program to implement the given logic function and to verify its operations in quartus using Verilog programming.

Developed by: KEERTHANA S

RegisterNumber: 212222230066

F1:
 module ff(a,b,c,d,f1);
 
 input a,b,c,d; 
 
 output f1; 
 
 assign f1 = (~b&~d) | (~a&b&d) | (a&b&~c);
 
 endmodule
 
F2:
module de (w,x,y,z,f2);

input w,x,y,z;

output f2; 

assign f2 = (x&y)|(w&y)|(~y&z);

endmodule
 
*/
## RTL realization
### For F1
![new 1](https://user-images.githubusercontent.com/119477890/234772789-8a2f7c59-7d6d-4a09-b736-877fb4ffb960.png)

### For F2
![new 2](https://user-images.githubusercontent.com/119477890/234772835-161f6eeb-4873-4cbe-a0ec-5ebd1827e425.png)

## Output:
## Timing Diagram:
### For F1
![new 2 1](https://user-images.githubusercontent.com/119477890/234773041-da12a43a-9597-4bd8-846c-c0016e451bf4.png)

### For F2
![new 2 2](https://user-images.githubusercontent.com/119477890/234773121-59162ff2-5c29-4b6d-b9d5-1e6abac13b8f.png)

### TRUTHTABLE:
![Uploading truth table.jpg…]()


## Result:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.
