# Verilog_Calculator_Matrix_Multiplication

This project shows how to make some basic matrix multiplication in Verilog. 

## Characteristics

There are some details about this implementation:
1. Three by three matrixes are used.
2. Each matrix input is a two byte container, so the maximum value (in decimal) it can hold is 65,535. 

## Scalability

If you need to increase the maximum value (65,535), then modify 
```verilog
reg [15:0] A1 [0:2][0:2];
```
to something like 
```verilog
reg [63:0] A1 [0:2][0:2];
```
in the case you want to work with 64 bits. Also remember to modify
```verilog
input [143:0] A;
```
to
```verilog
input [575:0] A;
```
(The value of 575 comes from having 9 spaces of 64 bits).

Similarly, if you need to modify the program to work with a *n***n* matrix, 