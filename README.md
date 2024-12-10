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
![truthtable1](https://github.com/user-attachments/assets/564675ce-92ff-4dff-92c1-961db2fba381)

![truthtable2](https://github.com/user-attachments/assets/7a5b7fa1-3f8d-42b6-8dfa-a2fe56fb86d1)

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber: 24900162
*/
```
module Ful_adder(input a,b,cin,output sum,carry);
assign sum = a ^ b ^ cin;
assign carry = (a & b) | (b & cin) | (cin & a);
endmodule

module full_subtractor (input A,input B,input Bin,output D,output Bout);
assign D = A ^ B ^ Bin;
assign Bout = (~A & B) | ((~A | B) & Bin);
endmodule
```

**RTL Schematic**

**Logic Diagram**
![fulladder](https://github.com/user-attachments/assets/47d7f1b2-153e-4b6c-b61a-eae86cdcf140)

![fullsubracter](https://github.com/user-attachments/assets/9876deec-eea8-406f-a9ea-c8c64a1839ba)

**Output Timing Waveform**
![wave fa](https://github.com/user-attachments/assets/181dbf76-d940-4b77-ba3b-d7d835af5895)

![wave fs](https://github.com/user-attachments/assets/8c3ef2b0-d2bf-4f9b-bc01-6f97f0b68f52)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



