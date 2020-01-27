# ScedulingSimulator

Simulates a fixed priority rate-monotonic scheduling algorithm. Randomly generates tasks and deadlines. This program aims to show 
how the fixed priority rate monotonic algorithm and the Deadline Driven algorithm look when used as outlined in the paper
Scheduling Algorithms for Multipogramming in a Hard-Real-Time Environment by Liu and Layland . In the paper, it is outlined that
the fixed priority algorithm can only consistantly achieve a processor utilization that is the below the average of the runtimes
and the request periods. For more information, see section 5 on acievable processor utilization. The fixed priority algorithm 
works by completing the shortest task first, then moving on to the next. If a shorter period ends before the current task is
completed (meaning a task higher on the Gantt diagram arrives before the current task is completed, in the Gantt diagrams showed),
the shorter period has a higher priority and therefore would preempt (or interrupt) the current task. In the dynamic algorithm,
the tasks are scheduled on-the-fly based on which deadline is closest. At each time interval, there are two choices: either work
on the current task or move on to another. For this algorithm, it will only move to another task when it's finished with the
current task or a task arrives who has an earlier deadline. The priorities, therefore, must be determined on each time interval.
While this algorithm is more complicated, it has a guaranteed processor utilization of up to 100%, meaning that as long as the
processor utilization is under 100%, the dynamic scheduling algorithm is feasible.

-John DeHart
