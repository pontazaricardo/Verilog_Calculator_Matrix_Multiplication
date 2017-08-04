# Verilog_Calculator_Matrix_Multiplication

This project shows how to make some basic matrix multiplication in Verilog. 

## Characteristics

There are some details about this implementation:
1. Three by three matrixes are used.
2. Each matrix input is a two byte container, so the maximum value (in decimal) it can hold is 65,535. If you need to increase this value, then modify 

```verilog
reg [15:0] A1 [0:2][0:2];
```