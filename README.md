# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

NAME; S.D.SURENDAR, REG.NO:24901073

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
\\
FULL ADDER:

  ![Screenshot 2024-12-11 102334](https://github.com/user-attachments/assets/7983e997-caad-4a91-88e5-7fcf8b1e3f45)
  
FULL SUBTRACTOR:

  ![Screenshot 2024-12-11 102425](https://github.com/user-attachments/assets/4e73069f-f78a-4a18-b8d5-0dcae025aee0)


**Procedure**
Type the program in Quartus software.
Compile and run the program.
Generate the RTL schematic and save the logic diagram.
Create nodes for inputs and outputs to generate the timing diagram.
For different input combinations generate the timing diagram.


**Program:**

FULL ADDER:
module fulladder(a,b,c,sum,carry); input a,b,c; output sum,carry; wire w1,w2,w3; assign
sum=a^b^c; assign w1=a&b; assign w2=a&b; assign w3=a&b; assign carry=w1|w2|w3;
endmodule
FULL SUBTRACTOR:
module fullsub(a,b,bin,diff,borr); input a,b,bin; output diff,borr; wire w1,w2,w3,w4,w5,w6;
xor g1(diff,a,b,bin); and g2(w4,w2,b); and g3(w5,w1,b); and g4(w6,b,bin); or
g5(borr,w4,w5,w6); endmodule

**RTL Schematic**
FULL ADDER:
\\\
  ![Screenshot 2024-12-11 101626](https://github.com/user-attachments/assets/7aab30a0-db8f-4723-a4c9-c915d160b118)
\\\
FULL SUBTRACTOR:
\\\
  ![Screenshot 2024-12-11 101639](https://github.com/user-attachments/assets/b9e1dd1a-49ed-4f3a-930b-b42a6b5a7aae)


**Output Timing Waveform**

FULL ADDER:
\\\

  ![Screenshot 2024-12-11 101654](https://github.com/user-attachments/assets/71b8a84b-74f1-4000-8a55-a58d738ea430)
\\\
FULL SUBTRACTOR:
\\\

  ![Screenshot 2024-12-11 101709](https://github.com/user-attachments/assets/6260a014-73c0-4223-a9bf-08fcf9db9bfa)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



