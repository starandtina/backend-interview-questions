A curated list of backend interview questions.

# Table of Contents

  1. [General Questions/Ice Breaker](#general)
  1. [Algos, Data Structures, & Computer Science Fundamentals Questions](#algorithms)
  1. [Design Questions](#software-design)
  1. [Backend Linux Questions](#linux)
  1. [Management Questions](#management)

----

## <a name='general'>General/Ice Breaker</a>

* Tell us about your most recent project.
* Do you ever do any coding in your personal time (outside of work)?

## <a name='algorithms'>Algos, Data Structures, & Computer Science Fundamentals</a>

> Algorithms are at the heart of every nontrivial computer application, and algorithmics is a modern and active area of computer science. Every computer scientist and every professional programmer should know about the basic algorithmic toolbox: structures that allow efficient organization and retrieval of data, frequently used algorithms, and basic techniques for modeling, understanding and solving algorithmic problems and our expectation of
event candidates is that they are very strong in this area.

* Implement linux command of tail, and print the last n lines.
* Implement the algorithm judging whether two rectangle has crossed, and compute the crossed area.
* Input one integer from command line, then split it into sum of multiple integers, and also print all possible sequences, once every line. For example, as for 3: the result is 

~~~C
    1 + 1 + 1
    2 + 1
    3
```

* String Matching Algo problem, figuring out whether there is a right bracket matching the left bracket.
* Input one english sentence that is separated by space., and reverse the sequence for the words of sentence, but the character sequence is not changed. For example, "I am a student." -> "student. a am I".
* Input one array with size of N that has different positive integers. As for every element A[i], and we need to get the value which is located between 0 and i-1 and bigger than A[i], also nearest to A[i]. If this element is not found, and just return -1. For example, input: N=4, A[0..3]={7, 5 ,9, 6} output: {-1, -1, 5, 5}, and we need it to be O(n).
* Find a number in a rotated sorted array.
* Find the length of the loop in a linked list.
* Implement an algorithm to print all valid (e.g., properly opened and closed) combinations of n-pairs of parentheses.
* Find the longest common sequence between two strings.
* Topological sort.
* Find a number in a matrix in which each row and column is sorted.
* Use rand5 to implement rand7.
* Explain how a program is loaded into the memory, and how Virtual Memory is layout? where do dynamic libraries and mmap files locates in virtual memory space?
* Using macro 'define' define how many milliseconds for one year.

## <a name='software-design'>Design</a>

> Designing software is an exercise in managing complexity. The complexity exists within the software design itself, within the software organization of the company, and within the industry as a whole. Software design is very similar to systems design. It can span multiple technologies and often involves multiple sub-disciplines. Software specifications tend to be fluid, and change rapidly and often, usually while the design process is still going on. Software development teams also tend to be fluid, likewise often changing in the middle of the design process. In many ways, software bears more resemblance to complex social or organic systems than to hardware. All of this makes software design a difficult and error prone process.  

* Design a `TaskDispatcher` to fullfill the requirements below:

    - Mutiple reader and writer for tasks; 
    - Fetching task definitions from remote, such as Redis Queue; 
    - Task workers are in charge of running tasks concurrently; 
    - Limit the number of maximum specific to the same source of task; 
    - Error handling.

* Design a `BackupTask` for your MSSQL Service Node instance, requirements as below: 

    - Backup MSSQL Server database; 
    - Upload backup files to different servers, such CIFS, S3, vBlob, etc.; 
    - Notify the results to any other components interests at that;
    - Error handling.

* Design a queue using stacks.

## <a name='linux'>Backend Linux</a>

* Explain load_avg/buffer/cache metrics in linux.
* Explain CLOSE_WAIT/TIME_WAIT in tcp connection.
* How to debug a hanging process?
* How to debug iptables rules?
* How to find the remote port is opened?
* How to find how many fds a process has opened?
* How to find last boot log?
* How to combine several commits in local git repo?
* Tell me your git work flow to do a hotfix.
* What's umask?
* Tell me as many ways as you can to copy a file to remote server in bash.
* Do you know the meaning for these commands: ps/sort/awk/join/pwd/iostat/vmstat/top/kill?
* Let’s assume that host is a local machine, and host2 is a remote machine. But as for kinds of reasons, these two computers couldn’t communicate between each other. But, there is another one host named host3 and it could connect to host1 and host2. So how can I let host1 connect to host2?
* Changing filenames in batch using shell scripts. eg: aa-1.1.txt -> aa.txt; ab-1.2.3.4.txt -> ab.txt; aa-bb-cc-1.1.txt -> aa-bb-cc.txt.
* Read a file of text, determine the n most frequently used words, and print out a sorted list of those words along with their frequencies.
* 

## <a name='management'>Management</a>

* How to tackle a task which is difficult to estimate and with high risk?
* How to react to unexpected/frequent requirement changes? Considering PoC phase and production phase.
* How to keep a team stable with limited offer(you can't increase the compensation while the competitors can give more).
