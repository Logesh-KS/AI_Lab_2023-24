# Ex.No: 7  Logic Programming –  Logic Circuit Design
### DATE:   23.03.2024                                                                         
### REGISTER NUMBER : 212221060145
### AIM: 
To write a logic program to design a circuit like half adder and half subtractor.
###  Algorithm:
1. Start the Program
2. Design a AND gate logic if both inputs are 1 then output is 1.
3. Design a OR gate logic if any one of input is 1 then output is 1.
4. Design a XOR gate logic if both inputs are different then output is 1.
5. Design a NOT gate logic if input is 0 then output is 1.
6. Design a half adder and half subtractor using the rules.
7. Test the logic.
8. Stop the program.

### Program:
'''
% Define logic gates
and_gate(1, 1, 1).
and_gate(_, _, 0).

or_gate(0, 0, 0).
or_gate(_, _, 1).

xor_gate(0, 0, 0).
xor_gate(1, 0, 1).
xor_gate(0, 1, 1).
xor_gate(1, 1, 0).

not_gate(0, 1).
not_gate(1, 0).

% Half Adder
half_adder(A, B, Sum, Carry) :-
    xor_gate(A, B, Sum),
    and_gate(A, B, Carry).

% Half Subtractor
half_subtractor(A, B, Difference, Borrow) :-
    xor_gate(A, B, Difference),
    not_gate(B, B_not),
    and_gate(A, B_not, Borrow).
'''


### Output:

![image](https://github.com/Logesh-KS/AI_Lab_2023-24/assets/113246318/12ad2305-f47b-4394-b264-abfaa85a8137)



### Result:
Thus the truth table of circuit verified sucessfully.
