A curated list of frontend interview questions.

# Table of Contents

  1. [General Questions](#general)
  1. [Algos, Data Structures, & Computer Science Fundamentals Questions](#algorithms)
  1. [Design Questions](#shell)
  1. [Problem Solving Questions](#problem-solving)
  1. [Management Questions](#management)

----

## <a name='algorithms'>General</a>

* Tell us about your most recent project.
* Do you ever do any coding in your personal time (outside of work)?

## <a name='algorithms'>Algorithms</a>

Algorithms are at the heart of every nontrivial computer application, and algorithmics is a modern and active area of computer science. Every computer scientist and every professional programmer should know about the basic algorithmic toolbox: structures that allow efficient organization and retrieval of data, frequently used algorithms, and basic techniques for modeling, understanding and solving algorithmic problems and our expectation of
event candidates is that they are very strong in this area.


* Implement linux command of tail, and print the last n lines.
* Implement the algorithm judging whether two rectangle has crossed, and compute the crossed area.
* Input one integer from command line, then split it into sum of muliple integers, and also print all possible sequences, once every line. For example, as for 3: the result is 

    1 + 1 + 1
    2 + 1
    3

* Design queue using stacks.
* String Matching Algo problem, figuring out whether there is a right bracket matching the left bracket.
* Input one english sentence that is separated by space., and reverse the sequence for the words of sentence, but the character sequence is not changed. For example, "I am a student." -> "student. a am I".
* Input one array with size of N that has different positive integers. As for every element A[i], and we need to get the value which is located between 0 and i-1 and bigger than A[i], also nearest to A[i]. If this element is not found, and just return -1. For example, input: N=4, A[0..3]={7, 5 ,9, 6} output: {-1, -1, 5, 5}, and we need it to be O(n).
* Find a number in a rotated sorted array.
* Find the length of the loop in a linked list.
* Implement an algorithm to print all valid (e.g., properly opened and closed) combinations of n-pairs of parentheses.
* Find the longest common sequence between two strings.
* Topological sort.
* Find a number in a matrix in which each row and column is sorted ○ Use rand5 to implement rand7.
* Explain how a program is loaded into the memory, and how Virtual Memory is layout? where do dynamic libraries and mmap files locates in virtual memory space?
* Using macro 'define' define how many milliseconds for one year.

## <a name='design'>Design</a>

*　Design a `TaskDispatcher` to fullfill the requirements below:

  1. Mutiple reader and writer for tasks; 
  1. Fetching task definitions from remote, such as Redis Queue; 
  1. Task workers are in charge of running tasks concurrently; 
  1. Limit the number of maximum specific to the same source of task; 
  1. Error handling.

* Design a `BackupTask` for your MSSQL Service Node instance, requirements as below: 
  
    1. Backup MSSQL Server database; 
    1. Upload backup files to different servers, such CIFS, S3, vBlob, etc.; 
    1. Notify the results to any other components interests at that;
    1. Error handling.

## <a name='design'>Problem Solving</a>

## <a name='management'>Management</a>

* How to tackle a task which is difficult to estimate and with high risk?
* How to react to unexpected/frequent requirement changes? Considering PoC phase and production phase.
* How to keep a team stable with limited offer (you can't increase the compensation while the competitors can give more)