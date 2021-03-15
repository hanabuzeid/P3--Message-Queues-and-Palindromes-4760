Readme for the programs coordinator and palin.

This application inputs a list of words (one word per line) and determines whether the words are palindromes or not. It then writes the palindromes to one file, palin.out, and the non-palindromes to another file, nopalin.out.   It accomplishes this with multiprocessing (by launching palin as a child process multiple times) and System V message queues.  

If the process takes 25 seconds or more, it and all of its child processes are terminated.  You can also terminate prematurely by pressing ^C.   You can also stop the process prematurely by limiting the number of processes that can run, i.e. using the -c command line option.

To compile this application, you will need the Makefile, coordinator.c and palin.c in the same directory.   The Makefile will require the -pthread library.  

Here is how to run the application. 

coordinator -h
coordinator [-h] [-c i] [-m j] datafile

-h   		Describes how the project should be run and then terminate.
-c i 		Indicate how many child processes i should be launched in total.
-m j		Indicate the maximum number of children j allowed to exist in the system at the same time. 
datafile	Input file containing the palindromes and non-palindromes, one per line