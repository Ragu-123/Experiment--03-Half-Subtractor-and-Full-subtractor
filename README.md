# Experiment--03-Half-Subtractor-and-Full-subtractor
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

/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: RAGUNATH R
RegisterNumber:  22008922
*/

## Output:
HALF SUBBTRACTOR
module expthree(output b,d,input x,y);
assign d = (x ^ y);
assign b = (~x & y);
endmodule
FULL SUBTRACTOR
module expthree(a,b,c,diff,borr);
input a,b,c;
output diff,borr;
assign borr=(~a&(b^c)|(b&c));
assign diff=(a^b^c);
endmodule

## Truthtable
HALF SUBTRACTOR
![image](https://user-images.githubusercontent.com/113915622/211126547-5de5f564-8f96-433e-a2ce-390f668d4072.png)
FULL SUBTRACTOR
![image](https://user-images.githubusercontent.com/113915622/211126601-62daa3f9-2fac-43a0-9a86-4f5e2ce18adb.png)





##  RTL realization
HALF SUBBTRACTOR
![Screenshot_20230107_072737](https://user-images.githubusercontent.com/113915622/211126787-bd53d0ed-398a-422d-a34f-322b723b562e.png)
FULL SUBTRACTOR
![WhatsApp Image 2023-01-07 at 07 40 11](https://user-images.githubusercontent.com/113915622/211126812-b99bab7a-0933-4493-afcc-f6bbf17ab268.jpg)




## Timing diagram 
HALF SUBTRACTOR
![Screenshot_20230104_021547](https://user-images.githubusercontent.com/113915622/211126872-1dc272fd-6f0d-47ab-8dfc-a7122a5dee65.png)
FULL SUBTRACTOR
![image](https://user-images.githubusercontent.com/113915622/211126919-ace03f3e-7bd9-4fc3-87fb-74f82bc2b2cd.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
