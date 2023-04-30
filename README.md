Download Link: https://assignmentchef.com/product/solved-mie562-assignment2-mip-modeling
<br>
We have done our best to answer all questions in this document. Please read it carefully. If you have a question that is not covered here, please post it to piazza.

<h1>1             Problem Definition Details</h1>

You can find definitions of the job shop scheduling problem and the disjunctive MILP model in the course slides and/or textbook. In this section, we provide details on how we represent the problem instances and the conventions used.

<strong>The instance file format is identical to that used for Coding Assignment #1.</strong>

Refer to the Coding Assignment #1 for the details.

The instances that are part of the solution to Coding Assignment #1 (see Quercus) are all valid instances for this assignment – however, the solutions to those instances for Coding Assignment #1 are not necessarily correct solutions to this assignment.<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a> These are not the test instances that will be used on MarkUs so it is recommended that you also develop your own instances to fully test your code.

<h1>2             Coding and Marking Details</h1>

You may re-use code <strong>that you wrote for Coding Assignment #1 </strong>for this assignment. In particular, because the instance format is the same, the code for reading in the instances can be taken from your existing code.

We will use the automated marking system called MarkUs to mark your code (see “Marking Scheme” below). MarkUs is running Python 3.8.3 and your code needs to work with this version of Python.<a href="#_ftn2" name="_ftnref2"><sup>[2]</sup></a>

In this section, we provide the coding requirements and other necessary information for using the MarkUs grading system.

<h2>2.1           Function Definition</h2>

You must submit a Python file called coding2.py that contains (perhaps among other functions) a function with the following signature:

run disjunctive(instance), where instance is a string of the filename of the instance (e.g., “ft06.txt”).

The function should read in the problem instance (assume it is in the same folder as the coding2.py file), create a MILP model, send the model to Gurobi to find a solution, and interpret the results from Gurobi.

The function should return a tuple containing (this is the same format as the solution in Coding Assignment #1):

<ul>

 <li>the makespan: integer</li>

 <li>a schedule: a dictionary with keys corresponding to the job number and values being a list of start times for that job’s operations following that job’s operation order.</li>

</ul>

MarkUs will call your function and parse the return value to compare it against the correct answer. It is important that you follow the above instructions exactly.

<h2>2.2           Using the Gurobi Library and Python Interface</h2>

Gurobi and its Python interface are available on the ECF system that you all have remote access to. You can also download the library for academic use.

For all details about installing and examples files of using the interface, please see the Quercus announcement titled “Heads Up: Software to Use for Coding Assignment #2”.

<h2>2.3           Restrictions on the Code You Write</h2>

<strong>PLEASE READ CAREFULLY! A NUMBER OF PEOPLE GOT VERY LOW</strong>

<strong>MARKS ON CODING ASSIGNMENT #1 BECAUSE THEY DID NOT ADHERE TO THE RESTRICTIONS!</strong>

There are the following restrictions on the code that you may write (in addition to the usual requirements of academic integrity):

<ul>

 <li>Do not put any input or print statements in your code. If you have them in your code for testing purposes, they should be commented out in your final submission.</li>

 <li>Do not put any commands outside a function (unless they are within a if name == ‘‘ main ’’ block). They will cause your code to crash when run by MarkUs (and you will fail all the automated tests).</li>

 <li>Do not import any modules except gurobipy. This is for two reasons: first, external modules will really not help you much and, second, your code will crash when run by MarkUs if you do so. If you have a good argument as to why you should be allowed to use a particular external module that does not defeat the purpose of this assignment, I am willing to listen to it. Please email Prof. Beck.</li>

 <li>Do not include the following line in your code: #!/usr/bin/env python. The MarkUs system does not have the Python implementation that we are using in the same place and the line will make make your code crash. This line is unnecessary in your Python if you run from an IDE or if you run from the command line (e.g., python coding2.py).</li>

</ul>

<h2>2.4           Marking Scheme</h2>

The marks for this assignment will be distributed as follows:

<ul>

 <li>7 marks from MarkUs. MarkUs will call your run disjunctive function with seven different problem instances. If your code returns the correct answer for an instance, you will get 1 mark. If it doesn’t return the correct answer, you will get 0 marks for that instance.</li>

 <li>3 marks from code review. Your code will be manually reviewed (i.e., by a human) and awarded a mark out of 3 based on the following scale:

  <ol>

   <li>no code submitted or the code submitted doesn’t even try to solve the problem;</li>

   <li>code submitted but horrible;</li>

   <li>code is pretty good but a few ugly/painful parts;</li>

   <li>good code.</li>

  </ol></li>

</ul>

Once marks are released, you will have one week to submit a remark request to Prof Beck. Such a request must specify the reason you believe that your code has been marked incorrectly. (E.g., “The correct answer to test #3 is X. The output of my code in MarkUs is X but I received 0 marks for that instance.”).

<a href="#_ftnref1" name="_ftn1">[1]</a> It is left as an exercise to understand why this is true.

<a href="#_ftnref2" name="_ftn2">[2]</a> Generally, as long as you are using Python 3.5 or greater, you should not have a problem.