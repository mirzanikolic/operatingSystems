# operatingSystems


# CEN 232 - Operating Systems - Project

This project is for implementing C in shell.

## Members
Damir Todic & Mirza Nikolic

## Listing of all files
damirza.c

## Outline of the Assignment
We've put together a basic implementation of all of the tasks that were assigned to us for this project, while attempting to implement each shell command as a separate function. We've been researching functions and commands that other people have used in their own operations throughout the project, and we've come up with conclusions and solutions to our own problems.

## Instructions for compiling
gcc damirza.c -o damirza   
./damirza

## Questions

### Question 1
Action 1: A program wants to read from a disk.

To perform this action, the OS needs to use the kernel mode as the user mode is not at all sufficient. The reason is, the OS cannot read some programs from a disk being in the user mode.  As the disk is hardware, user mode cannot act as a mediator between the processing commands of software and the hardware.  In such times, the program asks the OS to access the hardware (disk) on its behalf and fetch the program as input from it.  To perform this connection between hardware and software, 
the kernel needs to act, which is why the user-mode program is switched into the kernel mode.

Action 2: Reading the current time from the hardware clock.

To perform this action, the OS can just use the user mode This task can be executed in dual modes, i.e.,  in both the user mode and the kernel mode. The reason is - When the kernel boots, the hardware clock is set up in kernel mode. Using this, the system call is set up, 
and from then, we can directly read the current time from user mode (as software). The other options are: if the OS provides memory-mapped registers, then we can access the current time from user mode. As well, we can use the hwclock tool that sets up the system time by hardware clock time so that we can read the current time directly from the user mode.

### Question2

The system call provides the operating system's services to user programs via the Application Program Interface (API).  It acts as a link between a process and the operating system, allowing user-level programs to request operating system services. The only way into the kernel system is through system calls.

#### Types of system calls:
#### Process control: fork(), exit()
#### File manipulation: open(), read(), write()
#### Device manipulation: read(), write(), ioctl()
#### Information maintenance: getpid(), alarm(), sleep()
#### Communication: pipe(), shmget()

## Challenges
We've run into a few syntax issues as a result of the project's complexity. The majority of the problems were typographic in nature (forgeting ;, mispelling variables, etc.). We also had an issue with implicit function declaration, which we solved by declaring the function at the top of the file or adding appropriate imports. Another challenge for us was locating the best possible resources to enable us to carry out all of the tasks that were assigned to us, which we tried to accomplish.

## Sources
We used a variety of resources, the majority of which were just tutorials on YouTube and other websites. Because we are programmers, stackoverflow has always been a good friend of ours, containing many of our unanswered questions.

https://www.youtube.com/watch?v=IOHhUDDZaRk&feature=share&ab_channel=AnuranBarman

https://www.youtube.com/watch?v=cex9XrZCU14&ab_channel=CodeVault

https://www.youtube.com/watch?v=IFEFVXvjiHY&feature=share&ab_channel=NesoAcademy

https://www.youtube.com/watch?v=RpKQO3hgvD4&feature=share

https://stackoverflow.com/

https://brennan.io/2015/01/16/write-a-shell-in-c/

https://www.geeksforgeeks.org/making-linux-shell-c/