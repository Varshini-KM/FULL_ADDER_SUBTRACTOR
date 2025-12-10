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



<img width="242" height="208" alt="image" src="https://github.com/user-attachments/assets/7b46ae2c-052c-4d1a-ada6-5d4867c55979" />



FULL SUBTRACTOR

<img width="433" height="337" alt="image" src="https://github.com/user-attachments/assets/73e7b539-74d0-42ba-9048-29c10eb154e8" />




**Procedure**

1.Create a new Quartus project and add Verilog files for Full Adder and Full Subtractor.

2.Write and save the Verilog code defining inputs and outputs.

3.Compile the design to check for errors.

4.Create a simulation waveform (.vwf), add signals using Node Finder, and apply all input combinations.

5.Run functional simulation and verify the outputs with the truth table.

**Program:**

Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: RegisterNumber: 25018756

FULL ADDER
```
module fulladder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=((a ^ b)^cin);
assign carry= ( (a & b)| ( cin & a)| (cin & b));
endmodule
```

FULL SUBTRACTOR
```
module fullsub(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ((a ^ b)^bin);
assign borrow= (( ~a & b)|(~a & bin)|(b & bin));
endmodule
```




**RTL Schematic**

FULL ADDER



<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0766cab3-688e-464a-add1-21c801644018" />

FULL SUBTRACTOR


<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/f728799b-a961-4086-91c5-92ca5f44f8be" />



**Output Timing Waveform**

*FULL ADDER*



<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/0336ff3a-0e3a-4cd1-8936-6f7d8da94309" />




*FULL SUBTRACTOR*



<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/370e00af-e776-4c2b-ac0d-06ec8de690e5" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



