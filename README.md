# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by: saran . R

RegisterNumber: 212224050042

```
module verilog1(a,b,c,d,w,x,y,z,F1,F2);
input a,b,c,d,w,x,y,z;
output F1,F2;
wire A1,A2,A3,A4,A5,B1,B2,B3,B4,B5;
assign A1= (~a&(~b)&(~c)&(~d));
assign A2= (a&c&(~d));
assign A3= ((~b)&c&(~d));
assign A4= (~a&b&c&d);
assign A5= (b&(~c)&d);
assign F1= A1|A2|A3|A4|A5;
assign B1= (x&(~y)&z);
assign B2= (~x&(~y)&z);
assign B3= (~w&x&y);
assign B4= (w&(~x)&y);
assign B5= (w&y&z);
assign F2= B1|B2|B3|B4|B5;
endmodule

```


**RTL realization**

![image](https://github.com/Priyangarajapandiyan/BOOLEAN_FUNCTION_MINIMIZATION/assets/144872535/7d7d85a2-a892-4e47-b85f-8acb7f84eea0)

**TruthTable**

![image](https://github.com/Priyangarajapandiyan/BOOLEAN_FUNCTION_MINIMIZATION/assets/144872535/2b28204c-9dd3-4d8c-9d99-05195cc2e657)

**Timing Diagram**

![image](https://github.com/Priyangarajapandiyan/BOOLEAN_FUNCTION_MINIMIZATION/assets/144872535/f5e60235-a4a3-46fc-aad4-e2152cd96951)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

