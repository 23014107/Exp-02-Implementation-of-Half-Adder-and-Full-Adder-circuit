# NAME: RAMYA.P
# REFERENCE NO:212223240137


# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry=AB

![163552156-a13e5a56-c638-4110-97d9-8896907c8d25](https://github.com/23014107/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151625620/11943a12-d3e1-47b5-890f-476ec6d98d84)

# PROGRAM:
                              module de3hafeez(a,b,sum,carry);
                              input a,b;
                              output sum,carry;
                              xor(sum,a,b);
                              and(carry,a,b);
                              endmodule 

# RTL REALIZATION:

![291238403-9aca016b-7128-4d2e-a901-ddaac9a35bec](https://github.com/23014107/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151625620/fb94d867-66b7-4d27-b90b-bd5f249f2a8f)

# TRUTH TABLE:
![291240788-11615dbf-2ba8-4e05-9fd9-334496a9e29f](https://github.com/23014107/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151625620/18463632-a4a2-4ccf-86df-15bc6f73b0c3)


# Timing diagram:
![291242520-99b728ac-2283-46ac-9177-ea99c810fa18](https://github.com/23014107/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151625620/e4e66abc-b567-4a01-af3c-a149c0de507b)

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)



#### Figure -02 FULL ADDER 

### Procedure:

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
# Program:
                      module de3_1(a,b,c,sum,carry);
                      input a,b,c;
                      output sum,carry;
                      xor(sum,a,b,c);
                      assign carry=a&b|b&c|a&c;
                      endmodule

# RTL realization:
![291243116-02586837-ef74-4e96-a02d-4600a635b24b](https://github.com/23014107/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151625620/30476681-c9b1-4dcf-bde1-8704b54fef98)

# TRUTH TABLE:
![291243734-6f9b5471-6948-4c7f-9864-9075adaf1c7b](https://github.com/23014107/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151625620/67e654e3-a818-4e8b-8f06-975d21be6976)

# Timing diagram:
![291243892-7c3a3c8d-f5d9-43ee-adb5-5b9ce2561be2](https://github.com/23014107/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/151625620/1874cc30-92a4-4be4-afd3-2271d3aeefa0)




### Result:
Thus the given logic functions are implemented and their operations are verified using verilog programming.
