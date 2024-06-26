# Implementation-of-Half-Adder-and-Half Subtractor-circuit

Developed By : AKSHAYAA M T

Register Number : 212223110002

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![300513057-bd4a0b2c-cdbc-4184-ab08-81578f121e1f](https://github.com/Akshayaamt/HALF_ADDER_SUBTRACTOR/assets/144870472/4ab3c860-edaf-4008-a211-a8d9f7640278)


Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![300513222-d76b099c-513f-4e7c-843a-e2fd028a531a](https://github.com/Akshayaamt/HALF_ADDER_SUBTRACTOR/assets/144870472/9db56673-c09a-4836-b6dd-2c27d90b84a2)


Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**

*Half_adder*
```
module halfadd_top(a,b,sum,carry);
input a,b;
output sum,carry; 
 assign sum = a^b;
 assign carry = a & b;
endmodule
```
*Half_subtractor*
```
module halfsub_top(a,b,D,Bo);
input a,b;
output D,Bo; // Outputs sum and carry for half adder:Outputs difference D,Borrow Bo for half subtractor
assign D = a ^ b;
  assign Bo = ~a & b;
endmodule
```
```
Developed by: AKSHAYAA M T

RegisterNumber:212223110002

*/
```
**RTL Schematic**
![319517265-a161dc0f-3fca-40af-b323-b9db1e666429](https://github.com/Akshayaamt/HALF_ADDER_SUBTRACTOR/assets/144870472/b40ac750-4274-4a94-962c-ee173737cf3b)


**Output/TIMING Waveform**
![319517867-ef6d349d-59a7-4136-9f52-7888de577f5a](https://github.com/Akshayaamt/HALF_ADDER_SUBTRACTOR/assets/144870472/466c0b86-5ee1-4790-8fee-172ed4578fd2)


HALF ADDER:

![DE 3B](https://github.com/Rama-Lekshmi/HALF_ADDER_SUBTRACTOR/assets/118541549/ef6d349d-59a7-4136-9f52-7888de577f5a)

HALF SUBTRACTOR:

![DE 3C](https://github.com/Rama-Lekshmi/HALF_ADDER_SUBTRACTOR/assets/118541549/6249ee00-ee4a-4f3e-bd4f-bbb70f7f5f90)

**Result:**

Thus a  a half adder and half subtractor circuit is designed and its truth table in Quartus using Verilog programming is verified.
