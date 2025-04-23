# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**
~~~
FULL ADDER

module FH(a,b,c,sum, carry);
input a,b,c;
output sum, carry;
wire w1,w2,w3;
assign sum=a^b^c;
assign w1=a&b;
assign w2=b&c;
assign w3=c&a;
assign carry=w1|w2|w3;
endmodule;

FULL SUBTRACTOR

module FH(difference, borrow, a, b, bin);
input a,b,bin;
output differencef,borrow;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign difference=w1^bin;
assign borrow=w2|w3;
endmodule;
~~~

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**

![image](https://github.com/user-attachments/assets/e1416475-ad45-41bd-88b9-3f460fcbcb84)

![image](https://github.com/user-attachments/assets/b0b6b433-b6b5-450e-b55f-ce7208900183)


**Output Timing Waveform**

![image](https://github.com/user-attachments/assets/3b378d00-a10e-44c1-bca2-aab1ded47b19)

![image](https://github.com/user-attachments/assets/1d748a9d-8e18-43a7-8510-38283c69b356)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



