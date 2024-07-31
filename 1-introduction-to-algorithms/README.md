### ⬛ Introduction to Algorithms : Introduction	
The word algorism, came from the 9th century Persian mathematician "Abu Abdullah Muhammad bin Musa **al-Khwarizmi**" , which means the method of doing arithmetic using Indo-Arabic decimal system. It is also the   root of the word "algorithm" .

An algorithm is a well defined computational method that takes some value(s) as input and produce some value(s) as output. In other words, an algorithm is a sequence of computational steps that transforms input(s)  into output(s).

An algorithm is correct if for every input, it halts with correct output. A correct algorithm solves the given problem,  where as an incorrect algorithm might not halt at all on some input instance, or it might halt with other than  designed answer.

Each algorithm must have
* Specification: Description of the computational procedure.
* Pre-conditions: The condition(s) on input.
* Body of the Algorithm: A sequence of clear and unambiguous instructions.
* Post-conditions: The condition(s) on output.
* Algorithms are written in pseudo code that resembles programming languages like **C** and **Pascal**.
* Consider a simple algorithm for finding the factorial of n.

```C
Algorithm Factorial (n)

Step 1:	FACT = 1					
Step 2:	for i = 1 to n do					
Step 3:	FACT = FACT * i							
Step 4:	print FACT				
``` 										
Specification: Computes n!.

Pre-condition: n >= 0

Post-condition: FACT = n!

 										
* For better understanding conditions can also be defined after any statement, to specify values in particular variables.
* Pre-condition and post-condition can also be defined for loop, to define conditions satisfied before starting and after completion of loop respectively.
* What is remain true before execution of the ith iteration of a loop is called "loop invariant".
* These conditions are useful during debugging proces of algorithms implementation.
* Moreover, these conditions can also be used for giving correctness proof.
