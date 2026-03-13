## Multitasking

- CPU -> core -> program -> process -> thread.

- Multitasking.

![alt text](image.png)

- eg: we are browsing the internet while listening to music and downloading a file.

- multitasking utilizes the capabilities of a CPU and its cores. when an OS performs multitasking, it can assign different tasks to different cores. This is more efficient than assigning all tasks to single core.

## Multithreading

- It refers to the ability to execute multiple threads within a single process concurrently.
- eg: web browser can use multithreading by having separate threads for rendering the page, running JS, and managing user inputs. This makes the browser more responsive and efficient.

- Multithreading enhances the efficiently of multitasking by breaking down individual tasks into smaller subtasks or threads. These threads can be processed simultaneously, making better use of the CPU's capabilites.


## Diff

- Multitasking operates at the level of processes, which are the operating system's primary units of execution.

- Multitasking allows us to run multiple applications simultaneously, improving productivity and system utilization.

- Multithreading operates at the level of threads, which are smaller units within a process.

- Multithreading allows a single application to perform multiple tasks at the same time, improving application performance and responsiveness.

- eg: the office manager (OS) assigns different employess( processes) to work on different projects( applications) simultaneously. Each employee works on a different project independently.
Now within a single project( application), a team( process) of employess( threads) works on different parts of project at the same time, collaborating and sharing resources.

- In a single-core system: Both threads and processes are managed by the OS scheduler through time slicing and context switching to create the illusion of simultanaeous execution.

- In a multi-core system: Both threads and processes can run in true parallel on different cores, with the OS scheduler distributing tasks across the cores to optimize performance.



## Time-slicing

- It divides the CPU time into smaller intervals called time slices or quanta.
- Function: the OS scheduler allocates these time slices to different processes and threads, ensuring each gets a fair share of CPU time.

## Context-switching

- It is the process of saving the state of a currently running process or thread and loading the state of a next one to be executed.
- Function: when a process or thread's time slice expires, the OS scheduler performs a context switch  to move the CPU's focus to another process or thread.


## how JVM handles Multithreading?

- Java provides robust support for multithreading allowing developers to create applications that can perform multiple tasks simultaneously, improving performance and responsiveness.

- In Java, java.lang.package supports the Multithreading

- In single-core env, Java's multithreading is managed by the JVM and the OS, which switch between threads to give the illusion of concurrency

- In multi-core env, it can take full advantage of the available cores. The JVM can distribute threads across multiple cores allowing true parallel execution of threads.


- As soon as the Java program starts, one thread start running which is main thread. This thread is responsible for executing the main method of program.




