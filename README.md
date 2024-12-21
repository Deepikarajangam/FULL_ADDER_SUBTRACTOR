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
![image](https://github.com/user-attachments/assets/242858ec-a14d-4534-8176-e6b77267beda)
FULL SUBRACTOR
![image](https://github.com/user-attachments/assets/19608c0c-300a-4909-bf4a-c37c60a16661)



**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:R.DEEPIKA RegisterNumber:24900220
full adder
*/
```
module exfa(a,b,cin,sum,cout);
input a,b,cin;
output sum,cout;
assign sum=a^b^cin;
assign cout=(a&b)|(a&cin)|(b&cin);
endmodule
full subractor
module fas(a,b,bin,diff,bout);
input a,b,bin;
output diff,bout;
assign diff=a^b^bin;
assign bout=(~a&b)|(~a&bin)|(b&bin);
endmodule
```

**RTL Schematic**
FULL ADDER
![image](https://github.com/user-attachments/assets/560570b2-ad6d-4ae7-8560-5d611fc2d247)
FULL SUBRACTOR
![image](https://github.com/user-attachments/assets/80add7be-e628-4bf7-b7cd-495fdfdb4b3c)



**Output Timing Waveform**
FULL ADDER
![image](https://github.com/user-attachments/assets/eed38d9c-e33d-44cc-ba30-34aa9f68af0d)
FULL SUBRACTOR
![image](https://github.com/user-attachments/assets/796a048d-9b0b-446d-b9e3-01bb1cb9f539)





**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



