---
title: "Operating system from scratch"
layout: post
date: 2020-5-16 22:10
tag: academic
image: https://sergiokopplin.github.io/indigo/assets/images/jekyll-logo-light-solid.png
headerImage: true
projects: true
hidden: true # don't count this post in blog pagination
description: ""
category: project
author: qinxinWang
externalLink: false
---
Supervised by Prof. Ahmed Gheith, UT Austin

**[Code](https://github.com/qinzzz/BobOS)**

I built basic components of an operating system based on skeleton code provided by CS439 at UT Austin.   
My work includes implementing heap memory allocation, preemptive multi-threading, synchronization primitives, file system, virtual memory, system calls, etc. 

---

## Critical senction
Bootstrap kernel and critical section. 

## Heap memory allocation
Implement malloc(), free(), new, delete. Tested with space and time efficiency.  
Use a double linked list to trace all free blocks and add header & footer for every memory block.

## Cooperative multi-threading
A thread calls yield() to switch to another thread. Threads wait in the ready queue until some other threads give up their task and yield.

## Preemptive multi-threading. 
APIT generates an interrupte every 1ms and calls yield() to switch the threads.
Sycronization primitives. Implement semaphore and use it for barrier, bounded buffer, etc.

![buffer](../assets/posts/bounded_buffer.png)  
*Illustration of bounded buffer. Credit to Karl Marklund*

## File system
An ext2-like file system. Mount a FS from a disk or initialize on a device. You can read, write, find files and create hard links.

## Virtual memory
Enable virtual memory. Allow each process to have its private, lazily-mapped virtual address space. 
Handle the page fault exception and map virtual address space to physical address space.

![vspace](../assets/posts/vspace.gif)  
*Credit to Garrett Gu*

## System calls
Go to the User Mode. Implement the system call handler in kernel.

Workflow:  
Init -> kernelMain -> user program -> sys.S -> sysHandler -> sys.S -> user 

## Advanced system calls
Implement system calls including read, write, sem, fork, execl, wait, etc.
Use process table to manage resources(file, semaphore, process) created by system calls. 
- fork() syscall creates a copy of the current process (as child process)
- exec() replaces the current process with a different one and run some program




