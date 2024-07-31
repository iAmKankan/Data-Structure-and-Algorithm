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

### 🔲 A Sorting Algorithm
* Now, we take a more complex problem called sorting.
* Problem Definition: Sort given n numbers by non-descending order.
* There are many sorting algorithm. Insertion sort is a simple algorithm.
* Insertion Sort: We can assume up to first number is sorted. Then sort up    to two numbers. Next, sort up to three numbers. This process continue till    we sort all n numbers.
* Consider the following example of five integer:
```
       79 43 39 58 13 : Up to first number, 79, is sorted.
       43 79 39 58 13 : Sorted up to two numbers.
       39 43 79 58 13 : Sorted up to three numbers.
       39 43 58 79 13 : Sorted up to four numbers.
       13 39 43 58 79 : Sorted all numbers.
```

<p align="center">
 <img src="https://github.com/user-attachments/assets/e8ce653b-b7b6-4bd8-a318-56e51ba3b30b" width=20%/>
</p> 

That is, if first (i-1) numbers are sorted then insert ith number into its correct     position. This can be done by shifting numbers right one number at a time     till a position for ith number is found.
That is, shift number at (i-1)th position to ith position, number in (i-2)th position to (i-1)th position, and so on, till we find a correct position for the number in ith     position. This method is depicted in the figure on right side.

 The algorithmic description of insertion sort is given below.

 	 		 					
```C
Algorithm Insertion_Sort (a[n])

Step 1:	for i = 2 to n do	
Step 2:	current_num = a[i]	
Step 3:	j = i
Step 4:	 while (( j >1) and (a[j-1] > current_num)) do
Step 5:			 a[j] = a[j-1]
Step 6:			 j = j-1

Step 7:	a[j] = current_num	
``` 								
 More about sorting algorithms are discussed in the modules 5 and 10.


### ⬛ Time Complexity
* Execution time of an algorithm depends on numbers of instruction executed.
* Consider the following algorithm fragment:

```pascal
for i = 1 to n do
        sum = sum + i ;
```

* The for loop executed n+1 times for i values 1,2,....... n, n+1. Each instruction in the body of the loop is executed once for each value of i = 1,2,......, n. So number of steps executed is 2n+1.
* Consider another algorithm fragment:

```pascal
for i = 1 to n do	 	 	
 	for j = 1 to n do	 	
            k = k +1	
```
* From prevoius example, number of instruction executed in the inner loop is  which is the body of outer loop.
* Total number of instruction executed is

$$\Large{\color{Purple}\begin{matrix*}[l]
&=& n+1+n(2n+1) \\
&=& 2n^2+2n +1 \\
\end{matrix*}}$$


* To measure the time complexity in absolute time unit has the following problems
    1. The time required for an algorithm depends on number of instructions executed, which is a complex polynomial.
    2. The execution time of an instruction depends on computer's power. Since, different computers take different amount of time for the same instruction.
    3. Different types of instructions take different amount of time on same computer.
* Complexity analysis technique abstracts away these machine dependent factors . In this approach, we assume all instruction takes constant amount of time for execution.
* Asymptotic bounds as polynomials are used as a measure of the estimation of the number of instructions to be executed by the algorithm . Three main types of asymptotic order notations are used in practice:


### 🔲 1. Theta Notation ( &Theta; -Notation):
For a given function $\large{\color{Purple}g(n), \Theta(g(n))}$ is defined as

$$\Large{\color{Purple}\Theta(g(n)) = \begin{Bmatrix*}[l]
 f(n):& \textrm{ there exist } c_1 >0, c_2 >0 \textrm{ and } n_0 \in N  \\
& \textrm{ such that } 0\leq c_1 g(n) \leq f(n) \leq c_2 g(n), \textrm{ for all } n \geq n_0 \\
\end{Bmatrix*}}$$
