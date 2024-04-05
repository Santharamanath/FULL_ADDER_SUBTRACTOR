# FULL_ADDER_SUBTRACTOR
# DEVELOPED BY : SANTHA RAMANATH M
# REGISTER NUMBER : 212223220097

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

**Truthtable**FULL ADDER

![318287418-d2ff3833-f609-4054-af8b-d834a088a135](https://github.com/Santharamanath/FULL_ADDER_SUBTRACTOR/assets/149035289/7189773a-4572-4538-9852-83dc480d4ef6)

FULL SUBRACTOR

![318287474-70d90a4d-3b7e-4fd9-9830-4d6cf3fb29c2](https://github.com/Santharamanath/FULL_ADDER_SUBTRACTOR/assets/149035289/1d95b990-e829-44c1-a691-fb6b31e00060)


**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.*/
```
module EX04(a,b,c,sum,carry,BO,DIFF);
input a,b,c;
output sum,carry,BO,DIFF;
//FULL ADDER
assign sum = a^b^c;
assign carry = (a&b) | (b&c) | (a&c);
wire a0;
not (a0,a);
//FUKK SUBTRACTOR
assign DIFF = a^b^c;
assign BO = (a0&b) | (b&c) | (a0&c);
endmodule

```

**RTL Schematic**

![318287206-c689f8bf-6987-441d-bbcd-4a7780cc638b](https://github.com/Santharamanath/FULL_ADDER_SUBTRACTOR/assets/149035289/dd1e51fc-abd7-44f5-8d73-0f6f4fdd094c)


**Output Timing Waveform**

![318287317-520d4182-9020-46f6-a9d7-cfe4a0719267](https://github.com/Santharamanath/FULL_ADDER_SUBTRACTOR/assets/149035289/3a36db2b-a242-424a-b175-f5a6fa6fcae6)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



