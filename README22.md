# Home Work 4 - Job Scheduler

## Description

The main aim of the homework four is to impelment a simple job scheduler.

This job scheduler will only implement only the given number of programs at a time and remaining are all in waiting untill preprogram completed.

Threads, job scheduler, pid, queue, read-keywords, processing, background, C laungage, command line arguments. 

### Prerequisites

Requirements for the software and other tools to build, test and push
- [Sample 1]GCC compiler
- [Sample 2]C language

## To Build the file

To compile the files 
    $ gcc Hw4.c -o Hw4 -lpthread

## Running the tests


And to run the output file, Run the command lines as

    $./Hw4<integer input>
        here <integer input> is the number of simultaneous programs you want to run at a time upto 8.

    The program will now move to the scheduler with the given parameters and the following commands are used to run the required programs.

    Enter Command> submit <command argument> <input> (input if necessary)
    Enter Command> showjobs
    Enter Command> submithistory

If there is a need to terminate the program then use either 'CNTL+c' or 'CNTL+\' to terminate the pprogram.

### Sample Tests

Samples of the program on the provided commands
Enter command> submit sleep 45
job 0 added to the queue
Enter command> submit sleep 55
job 1 added to the queue
Enter command> submit sleep 10
job 2 added to the queue
Enter command> submit sleep 56
job 3 added to the queue
Enter command> showjobs
jobid   command         status
0       sleep 45      working
1       sleep 55      working
2       sleep 10      waiting
3       sleep 56      waiting
Enter command> showjobs
jobid   command         status
0       sleep 45      working
1       sleep 55      working
2       sleep 10      waiting
3       sleep 56      waiting
Enter command> showjobs
jobid   command         status
1       sleep 55      working
2       sleep 10      working
3       sleep 56      waiting
Enter command> showjobs
jobid   command         status
2       sleep 10      working
3       sleep 56      working
Enter command> showjobs
jobid   command         status
3       sleep 56      working
Enter command> submithistory
jobid   command         starttime                       endtime                         status
0       sleep 45      Fri Nov 16 10:15:22 2022        Fri Nov 16 10:16:12 2022        success
1       sleep 55      Fri Nov 16 10:15:29 2022        Fri Nov 16 10:16:19 2022        success
2       sleep 10      Fri Nov 16 10:16:13 2022        Fri Nov 16 10:16:28 2022        success
Enter command> submithistory
jobid   command         starttime                       endtime                         status
0       sleep 45      Fri Nov 18 10:15:22 2022        Fri Nov 18 10:16:12 2022        success
1       sleep 55      Fri Nov 18 10:15:29 2022        Fri Nov 18 10:16:19 2022        success
2       sleep 10      Fri Nov 18 10:16:13 2022        Fri Nov 18 10:16:28 2022        success
3       sleep 56      Fri Nov 18 10:16:19 2022        Fri Nov 18 10:17:04 2022        success
Enter command>


## Authors

  - **Sai Gowtham Yeluri** - *CS 532* -
  [GitHub](https://github.com/syeluri99)
  - **Bhuvanesh Alla** - *CS 532* - 
  [GitHub](https://github.com/BhuvaneshAlla)