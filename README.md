# Operating-system-assignment
CPU Scheduling | Longest Remaining Time First (LRTF) algorithm

Use case of LRTF

Three Students (a, b, c) are arriving in the Mess at the same time. The Id numbers of these Students are 2132, 2102, 2453 and the food taken time from the mess table is 2, 4 and 8 minutes. If the two students have same remaining time so it is broken by giving priority to the Students with the lowest id number. Consider the Longest Remaining Time First (LRTF) Scheduling Algorithm and calculate the average turnaround time and waiting time.


Algorithm


Step-1: Create a structure of process containing all necessary fields like AT (Arrival Time), BT (Burst Time), CT (Completion Time), TAT (Turn Around Time), WT (Waiting Time).
Step-2: Sort according to the AT;
Step-3: Find the process having Largest Burst Time and execute for each single unit. Increase the total time by 1 and reduce the Burst Time of that process with 1.
Step-4: When any process has 0 BT left, then update the CT (Completion Time of that process CT will be Total Time at that time).
Step-5: After calculating the CT for each process, find TAT and WT.


Purpose


This is a pre-emptive version of Longest Job First (LJF) scheduling algorithm. In this scheduling algorithm, we find the process with maximum remaining time and then process it. We check for the maximum remaining time after some interval of time (say 1 unit each) to check if another process having more Burst Time arrived up to that time.


Procedure


Step-1: First, sort the processes in increasing order of their Arrival Time.
Step-2: Choose the process having least arrival time but with most Burst Time. Then process it for 1 unit. Check if any other process arrives up to that time of execution or not.


General Terms


Arrival Time:Time at which the process arrives in the ready queue.
Completion Time:Time at which process completes its execution.
Burst Time:Time required by a process for CPU execution.
Turn Around Time:Time Difference between completion time and arrival time.
Waiting Time: Time Difference between turnaround time and burst time.


Formulas


Turn Around Time (TAT) = (Completion Time) - (Arrival Time)
Waiting Time (WT) = (Turn Around Time) - (Burst Time) 
Step-3: Repeat the above both steps until execute all the processes. Example: Consider the following table of arrival time and burst time for four processes P1, P2, P3 and P4.
