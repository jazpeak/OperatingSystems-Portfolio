# Operating Systems Portfolio
> A collection of systems engineering projects built to explore the internals of modern Operating Systems.

This repository serves as a centralized index for my Operating Systems projects. My work focuses on bridging the gap between hardware-specific abstractions and user-facing applications. All projects are written primarily in C and Assembly, focusing heavily on memory management, concurrency, and kernel-level resource allocation.

---

## Featured Implementations

### 1. [SimpleOS: MLFQ Scheduler & Custom Shell](https://github.com/jazpeak/egos-mlfq-implementation)
An enhanced version of the EGOS-2000 teaching OS natively running on the RISC-V architecture. 
- **Core Focus**: Kernel space programming, Process Control Blocks (PCBs), Timer Interrupts.
- **Highlights**: Implemented a robust Multi-Level Feedback Queue (MLFQ) preemptive scheduler in the kernel layer to optimize CPU responsiveness, alongside POSIX-like user shell commands (`grep`, `wcl`) built entirely from scratch using raw inode and block reading.

### 2. [SimpleScheduler: Round-Robin Daemon](https://github.com/jazpeak/SimpleScheduler)
A preemptive, daemonized process scheduler built using POSIX timers and IPC.
- **Core Focus**: Context Switching (`SIGSTOP`, `SIGCONT`), Hardware Timers, IPC Pipes.
- **Highlights**: Schedules user-submitted processes across `NCPU` cores using a strict Round-Robin policy. Operates as a background daemon that sleeps natively to conserve CPU cycles, waking only on `SIGALRM` interrupts to context-switch processes.

### 3. [SmartELFLoader: Dynamic Page-Fault Handler](https://github.com/jazpeak/SmartELFLoader)
A custom, lazily-evaluated ELF 32-bit executable loader.
- **Core Focus**: Virtual Memory, `mmap`, Signal Handling (`SIGSEGV`).
- **Highlights**: Implements lazy loading by intentionally forcing and intercepting segmentation faults. Dynamically allocates memory on-demand in 4KB pages and resumes execution, tracking internal fragmentation metrics.

### 4. [SimpleShell: POSIX-Compliant Unix Shell](https://github.com/jazpeak/Simple-Shell-program)
A lightweight interactive Unix shell environment built from scratch.
- **Core Focus**: Process Forking (`fork`, `execvp`), Pipe Redirection (`dup2`).
- **Highlights**: Natively parses and executes arbitrary pipelines of commands, tracking execution duration and process IDs for every pipeline stage, while safely handling terminal interrupts.

### 5. [SimpleMultithreader: C++11 Concurrency Library](https://github.com/jazpeak/SimpleMultithreader)
A lightweight, header-only multithreading library abstracting POSIX threads.
- **Core Focus**: POSIX Threads (`pthread`), C++11 Lambdas, Iteration Chunking.
- **Highlights**: Dynamically distributes arbitrary 1D and 2D iteration workloads across `numThreads` by hooking C++11 lambda functions into bare-metal `pthread_create` calls without thread pools, and features native microsecond execution profiling.

---

## Core Technical Competencies

By completing these projects, I have developed hands-on experience with:
- **Languages**: C, RISC-V Assembly, Bash
- **Concepts**: Preemptive Scheduling, Context Switching, Inter-Process Communication, Memory Paging, File System Architectures.
- **Tools**: GDB, QEMU Emulators, GNU Make, GCC Cross-Compilers.
