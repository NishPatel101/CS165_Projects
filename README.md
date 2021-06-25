# CS165 Projects
This repository is for my work on the CS165 projects.  
  
## Project 2 - CTF
We exploited vulnerabilities in a toy application and a real-world application to bypass authentications. For the toy application, we modified instructions in the binary to bypass authentication and retrieve a success string (flag). For the real-world application, we similarly modified instructions in the binary to use the program after the trial period ends.  
  
## Project 3 - Buffer Overflow Exploits
We exploited buffer overflow vulnerabilities on a binary in a host server to create different files and a shell with admin priviledges. These attacks took advantage of a faulty use of `strcpy()` to overflow the stack when prompted for user input (login credentials).  

For the first two files, we used the exloit payload to call log_result functions in the binary with our desired inputs (like file names).  

For the third file, we instead invoked a shell to call the desired function.

For creating the shell, we used Return-Oriented-Programming (ROP) chains to bypass data-execution prevention (since we could not execute injected code on the stack). This attack instead used ROP gadgets, calling lines in the binary to execute the series of instructions necessary for the system call `execve()`.  

Each of these approaches are explained in greater detail in their respecive documentations.
