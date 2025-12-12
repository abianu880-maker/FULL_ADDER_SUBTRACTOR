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
<img width="1215" height="510" alt="Screenshot 2025-12-12 153654" src="https://github.com/user-attachments/assets/b1a3b863-5e6b-4472-a7be-71bcdfce012d" />

**Procedure**

1.Type the program in Quartus software.

2.Compile and run the program.

3.Generate the RTL schematic and save the logic diagram.

4.Create nodes for inputs and outputs to generate the timing diagram.

5.For different input combinations generate the timing diagram.
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:

```
module full_adder(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=(a^b^c);
assign carry=(a&b)|(b&c)|(c&a);
endmodule
```
```
module full_subtractor(a,b,c,diff,borrow);
input a,b,c;
output diff,borrow;
assign diff=(a^b^c);
assign borrow=(~a&c)|(~a&b)|(b&c);
endmodule
```
**RTL Schematic**
<img width="1335" height="712" alt="Screenshot 2025-12-12 153717" src="https://github.com/user-attachments/assets/5222d4d9-ed01-4baf-ad14-54b44b063d7f" />
<img width="1165" height="592" alt="Screenshot 2025-12-12 153730" src="https://github.com/user-attachments/assets/8daf68bd-2ac2-4841-9a06-02420b21b601" />

**Output Timing Waveform**
<img width="1881" height="493" alt="Screenshot 2025-12-12 153738" src="https://github.com/user-attachments/assets/74cc5d63-51d0-4de8-b40c-734e17113631" />
<img width="1887" height="480" alt="Screenshot 2025-12-12 153755" src="https://github.com/user-attachments/assets/96ffd874-649f-42b7-8915-5a5ad66e636c" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



