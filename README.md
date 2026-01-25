# Thread-Pool-Task-Scheduler



A high-performance multithreaded task scheduler written in modern C++ (C++17) for Linux, using a fixed thread pool, RAII-based resource management, and safe concurrency primitives to execute tasks efficiently under load.











So in this task is important to check 



* Jobs (Functions that we want to run
* Workers will be threads
* We will have a waiting line (Queue , Fifo?)

WE WILL NOT

* Create a new thread for every job
* Run jobs immediately on the main thread.

We will

* Start N worker threads at once.
* They are currently waiting, idle.
* Submit a job -> Goes to Queue
* Worker gets it, takes the job and runs it



worker is waiting = elegible 



running a task = busy









mainthread LOCKS queue, pushes job 

