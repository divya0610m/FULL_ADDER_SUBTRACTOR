## NAME: DIVYA LAKSHMI M
## REG NO: 212224040082
## DATE: 15.04.2025

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

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.

**Program:**

module ex4(sum,cout,a,b,cin,df,bo,bin);
input a,b;
input cin,bin;
output sum,df;
output cout,bo;
wire w1,w2,w3,w4,w5,w6;
assign w1=a^b;
assign w2=a&b;
assign w3=w1&cin;
assign sum=w1^cin;
assign cout=w2|w3;
assign w4=a^b;
assign w5=(~a&b);
assign w6=(~w4&bin);
assign df=w4^bin;
assign bo=w5|w6;
endmodule

**Truthtable**

![ex4 table1](https://github.com/user-attachments/assets/447437f7-9b9f-44e5-8038-a1cfd2d12276)

![ex 4 table2](https://github.com/user-attachments/assets/6c58286f-0824-4e8c-8b7c-61a8578dc18e)


**RTL Schematic**

![ex4 dia](https://github.com/user-attachments/assets/ede5f2da-2e66-41e6-96cb-192cdbbbd91c)


**Output Timing Waveform**

![ex4 waveform](https://github.com/user-attachments/assets/a467b7aa-36b4-4fe2-8343-64d5f034db3b)

**Result:**

Thus ,The Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



