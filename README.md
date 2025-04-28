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

**Full Adder**
![image](https://github.com/user-attachments/assets/62b9edfb-062c-4295-87f2-7eb28f19a607)

**Full Subtractor**
![image](https://github.com/user-attachments/assets/a28ce83c-e592-405e-853e-65696c9143c9)

**Procedure**

Write the detailed procedure here

**Program:**

        module sample(a,b,cin,bin,sum_a,cout,diff_s,borr_s);
        input a,b,cin,bin;
        output sum_a,cout,diff_s,borr_s;
        assign sum_a=a^b^cin;
        assign cout=(a^b)&cin |(a&b);
        assign diff_s=a^b^bin;
        assign borr_s=(~a&~b&~bin)|(~a&b&~bin)|(~a&b&bin)|(a&b&bin);
        endmodule

**RTL Schematic**

![image](https://github.com/user-attachments/assets/f326527b-f5c1-4d92-b653-43d96f9e2d54)

**Output Timing Waveform**

![image](https://github.com/user-attachments/assets/784c773d-83ff-4a24-a247-d3b1d2f5738d)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
