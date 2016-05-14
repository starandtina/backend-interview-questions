A curated list of backend interview questions.

# Table of Contents

  1. [General Questions/Ice Breaker](#general)
  1. [Management Questions](#management)
  1. [Algos, Data Structures, & Computer Science Fundamentals Questions](#algorithms)
  1. [Design Questions](#design)
  1. [Backend Linux Questions](#linux)
  1. [Management Questions](#management)

----


## <a name='general'>General/Ice Breaker</a>

>You're looking for passion and enthusiasm when a candidate discusses their previous projects and any projects they're working on in their spare time. If they get excited talking about these things, they show the kind of passion for software development that is a good indicator of whether they're capable of meeting the your bar.
Once you've calmed a nervous candidate's nerves or determined level of passion/enthusiasm, move on to the next set of questions. Try to spend a maximum of 5 minutes on this section.

* Tell us about your most recent project.
* Do you ever do any coding in your personal time (outside of work)?
* Do you have a account on Github?
  * If so, what are some examples of repos you follow?
* Tell us what critical problems you have to handle in your latest projects?
* Why did you get into development?
* How many technical books did you read in the past year?
* What was your favorite technical book in the past year? What did you learn from it?
* What websites do you read regularly, related to development?
* Do you maintain any open-source projects?
* Do you code in your spare-time?
* Do you love programming, or do you do it for the money?
* Have you accomplished anything important in your career yet? Do you want to?
* What would make you feel that you have done something important?
* What's your favorite programming language? Why?
* If you could add one feature to your favorite language, what would it be? Why?
* If you could remove one feature from it, what would it be? Why?

## <a name='management'>Management</a>

* How to tackle a story/task which is difficult to estimate and with high risk?

>
  - Investigate as early as possible
  - Assign senior staffs on the problem
  - More frequent update and more communication
  - Report higher level supervisors to be aware of the situation

* How to react to unexpected/frequent requirement changes, considering PoC phase and production phase.

>
  - For PoC:
    - communicate with team members to let them know things are changing.
    - Proving the solution is more important than perfect design/implementation. For requirement changes, argue for the reason. If it is business reason, mostly we should follow. If it is technical reason, we should discuss first and then make decision.
  - For production:
    - Setup a process first. A requirement change should result in following reactions after replan (re-estimation):
         - If it is not so urgent, keep working, change the future plan
         - If it is urgent, either request resource (considering the
ramp-up cost) or cut features
         - If not possible, suggest delay the release date

* How to keep a team stable with limited offer. (How's about if you can't increase the compensation while the competitors can give more)

>Basically, setup a good working environment all the time, making team members work happily, and with good development direction and opportunity. If things really happens, resort to higher-level manager and HR to find out a solution.

## <a name='algorithms'>Algos, Data Structures, & Computer Science Fundamentals</a>

> Algorithms are at the heart of every nontrivial computer application, and algorithmics is a modern and active area of computer science. Every computer scientist and every professional programmer should know about the basic algorithmic toolbox: structures that allow efficient organization and retrieval of data, frequently used algorithms, and basic techniques for modeling, understanding and solving algorithmic problems and our expectation of
event candidates is that they are very strong in this area.

* Implement linux command of tail, and print the last n lines.
* Sorting 5GB file, considering memory problem, also using your favorite language writing the Merge sort algo.
* Implement the algorithm judging whether two rectangle has crossed, and compute the crossed area.
* Input one integer from command line, then split it into sum of multiple integers, and also print all possible sequences, once every line. For example, as for 3: the result is 

  ~~~C++
  1 + 1 + 1
  2 + 1
  3
  ~~~

* String Matching Algo problem, figuring out whether there is a right bracket matching the left bracket. It should satisfies space complexity of O(n), but O(1) is better.
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
* What is the difference between a process and a thread?
* What is a critical section?
* What is a race condition?
* Define how many milliseconds in one year using `define`.
* Define `max` function using `define`.
* Why we always need to wrap up muliple statment block with `do{while(0);}` when using `define`?
* Describe the role of `static`, `const`, `volatile`, `typeof`.
* Implement a `trim_string` function for removing the whitespace from the beginning and end of a string.
* Implement a Class which can't be inherited by other Classes with `C++`.
* List the methods for IPC with brief explanations.
* Write a function or macro: `LENGTH_OF` in order to get the length of array.

  ~~~C++
  int  array1[100];
  byte array2[300];
  LENGTH_OF(array1) returns 100
  LENGTH_OF(array2) returns 300
  ~~~


## <a name='design'>Design</a>

> Designing software is an exercise in managing complexity. The complexity exists within the software design itself, within the software organization of the company, and within the industry as a whole. Software design is very similar to systems design. It can span multiple technologies and often involves multiple sub-disciplines. Software specifications tend to be fluid, and change rapidly and often, usually while the design process is still going on. Software development teams also tend to be fluid, likewise often changing in the middle of the design process. In many ways, software bears more resemblance to complex social or organic systems than to hardware. All of this makes software design a difficult and error prone process.  

* Design a queue using stacks.

* Implement an in­-memory job queue. (Thanks @easeway)

  Description:

  Jobs are created by users, so each job is associated with a certain user id. The execution time of a job varies. It is possible a job takes hours up­ to days. There's a fixed number of job consumers and each of them pops a job from the queue and executes it.

  In such a system like above, a common problem is if a user creates too many jobs and each takes quite long time to execute, he may exhausts all the job consumers and other users can't get their jobs run.

  To improve the quality of service, only one job from the same user can be executed at the same time, and no more than `M` jobs can be queued for the same user (all up­coming jobs will be rejected).
  The order of jobs pushed by the same user must be preserved.

  In general, it should has requimrents as below but not limted to:

  * Mutiple reader and writer for tasks
  * Fetching task definitions from remote, such as Redis Queue
  * Task workers are in charge of running tasks concurrently
  * Limit the number of maximum specific to the same source of task
  * Error handling
  * ...

  The queue must provide the following interface (pseudo code)

  ~~~C++
  class Job {
    public string UserId;
    public virtual void Run(); 
  }

  class FairQueue {
    public const int M=5;

    // when there's some jobs in queue, pop one,and returns.
    // block when queue is empty.
    public Job Dequeue();

    // enqueue a job.
    // If the pending limit exceeds M, returns false.
    // otherwise return true after job is enqueued.
    public bool Enqueue(Job);
  }
  ~~~

  Questions:

  * Design the queue, considering multi­thread environment.
  * Write code for implementation.

* Design a `BackupTask` for the MSSQL Service instance, requirements as below: 

  * Backup MSSQL Server database, including different strategies, such as full backup, differential backup and log backup
  * Upload backup files to different devices, such CIFS, S3, vBlob, etc.
  * Notify the results to any other components interested at that
  * Schedule backup tasks, such as once every day or once every hour, etc.
  * Error handling
  * ...

* A service exposes simple RESTful APIs for reading and updating objects:(Thanks @easeway)

  ~~~JavaScript
  GET http://hostname/api/v1/object/ID
  PUT http://hostname/api/v1/object/ID(with data encoded as JSON in payload)
  ~~~

  As a client, it uses library which provides 4 functions wrapping the above APIs:

  ~~~C++
  object get_object(id)
  update_object(object)
  ~~~

  When a client application wants to perform an atomic update of the object, the logic is like:

  ~~~C++
  object calc_and_update(id){
    obj=get_object(id) 
    calculate(obj) // update attributes according to current values 
    update_object(obj)
    return obj;
  }
  ~~~

  The problem with above logic is: 

  * when there's multiple clients working concurrently
  * the above logic is not atomic

  Questions:

  * Please analyze the inconsistency scenarios
  * How to solve the problem

* Design the algorithm judging whether two rectangle has crossed and also calculate the crossed area if it exists.

  ~~~C++
  struct Rect {
    int x, y; // left-upper coordinators
    int w, h; // width and height 
  };
  ~~~

  Implement the function:
  ~~~C++
  bool rectOverlap(constRect &r1, const Rect &r2, Rect& overlap);
  ~~~

  If there's an overlapping, fill overlap with the overlapped area then return true, otherwise, leave overlap untouched then return false.


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
* Let's assume that host is a local machine, and host2 is a remote machine. But as for kinds of reasons, these two computers couldn't communicate between each other. But, there is another one host named host3 and it could connect to host1 and host2. So how can I let host1 connect to host2?
* Changing filenames in batch using shell scripts. eg: aa-1.1.txt -> aa.txt; ab-1.2.3.4.txt -> ab.txt; aa-bb-cc-1.1.txt -> aa-bb-cc.txt.
* Read a file of text, determine the n most frequently used words, and print out a sorted list of those words along with their frequencies.


## <a name='management'>Management</a>

* How to tackle a task which is difficult to estimate and with high risk?
* How to react to unexpected/frequent requirement changes? Considering PoC phase and production phase.
* How to keep a team stable with limited offer(you can't increase the compensation while the competitors can give more).
