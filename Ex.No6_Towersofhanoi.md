# Ex.No: 6   Logic Programming – Factorial of number   
### DATE: 23.03.2024                                                                        
### REGISTER NUMBER : 212221060145
### AIM: 
To  write  a logic program  to solve Towers of Hanoi problem  using SWI-PROLOG. 
### Algorithm:
1. Start the program
2.  Write a rules for finding solution of Towers of Hanoi in SWI-PROLOG.
3.  a )	If only one disk  => Move disk from X to Y.
4.  b)	If Number of disk greater than 0 then
5.        i)	Move  N-1 disks from X to Z.
6.        ii)	Move  Nth disk from X to Y
7.        iii)	Move  N-1 disks from Y to X.
8. Run the program  to find answer of  query.

### Program:

'''
% Define the predicate hanoi/3 to solve the Towers of Hanoi problem
hanoi(1, X, Y) :-
    write('Move disk from '), write(X), write(' to '), write(Y), nl.

hanoi(N, X, Y) :-
    N > 1,
    M is N - 1,
    hanoi(M, X, Z),
    hanoi(1, X, Y),
    hanoi(M, Z, Y).
'''


### Output:
![image](https://github.com/Logesh-KS/AI_Lab_2023-24/assets/113246318/17b393b5-7594-47f4-8a11-85c75c08a294)



### Result:
Thus the solution of Towers of Hanoi problem was found by logic programming.
