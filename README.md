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
FULL ADDER

<img width="766" height="532" alt="502669814-e6553a6e-5161-4e8c-bb28-838797016350" src="https://github.com/user-attachments/assets/f87c443c-f98b-4a29-b724-de06107066b4" />
FULL SUBTRACTOR

<img width="647" height="666" alt="502670245-52d0a8c5-adca-4cab-b762-97049c022d10" src="https://github.com/user-attachments/assets/642c5c03-4cb2-4524-b1d7-b9c5bc2b3ce5" />

**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: Sreejaa RegisterNumber: 25015302

FULL ADDER

module experiment4(sum,cout,a,b,cin);
output sum;
output cout;
input a;
input b;
input cin;
//internal nets
wire s1,c1,c2;
//Instantiate logic gate primitives
xor (s1,a,b);
and(c1,a,b);
xor(sum,s1,cin);
and(c2,s1,cin);
or(cout,c2,c1);
endmodule


FULL SUSTRACTOR


module experiment4a (df, bo, a, b, bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2, w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(-w1&bin);
assign df-w1^bin;
assign bo-w2/w3;
endmodule

**RTL Schematic**
#FULL ADDER

<img width="547" height="343" alt="502668652-3eb811a1-8385-43de-9a65-7024eee747b2" src="https://github.com/user-attachments/assets/b86993d1-b6d9-4e5d-b596-a9e310caccb3" />
#FULL SUBTRACTOR

<img width="372" height="220" alt="502668759-53fc8857-794f-4b49-a8b6-cb8b145174ce" src="https://github.com/user-attachments/assets/02b98c47-d690-424b-a57e-12aa76a25775" />

**Output Timing Waveform**
#FULL ADDER

<img width="826" height="275" alt="502667939-6cb7b49c-ed3d-46c3-9a3b-726906b32009" src="https://github.com/user-attachments/assets/f6144cf9-d0fd-4e89-a2f7-549b61ba6f45" />

#FULL SUBTRACTOR
<img width="835" height="395" alt="502668074-f720de5a-dbea-44e0-a758-2c6251a8dae1" src="https://github.com/user-attachments/assets/789ae6b2-a676-492c-89c0-d103eecccaee" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



