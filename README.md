# Tiny Unix Shell (tsh)

A Unix-style command shell implemented in C with full job control, I/O redirection, and pipeline support using POSIX system calls.

## Overview

This project implements a functional Unix shell that can execute programs in the foreground and background, manage job states, handle signals correctly, and support file redirection and pipelines.

It demonstrates core operating systems concepts including process creation, signal handling, file descriptors, and inter-process communication.

---

## Features

### Job Control
- Foreground and background execution
- Built-in commands:
  - `jobs` – list running and stopped jobs
  - `fg` – resume job in foreground
  - `bg` – resume job in background
  - `quit` – exit shell
- Supports job states:
  - Foreground
  - Background
  - Stopped

### Signal Handling
Correct handling of:

- SIGINT (Ctrl+C)
- SIGTSTP (Ctrl+Z)
- SIGCHLD (child termination)

Prevents zombie processes and race conditions.

---

### I/O Redirection

Supports:
# Tiny Unix Shell (tsh)

A Unix-style command shell implemented in C with full job control, I/O redirection, and pipeline support using POSIX system calls.

## Overview

This project implements a functional Unix shell that can execute programs in the foreground and background, manage job states, handle signals correctly, and support file redirection and pipelines.

It demonstrates core operating systems concepts including process creation, signal handling, file descriptors, and inter-process communication.

---

## Features

### Job Control
- Foreground and background execution
- Built-in commands:
  - `jobs` – list running and stopped jobs
  - `fg` – resume job in foreground
  - `bg` – resume job in background
  - `quit` – exit shell
- Supports job states:
  - Foreground
  - Background
  - Stopped

### Signal Handling
Correct handling of:

- SIGINT (Ctrl+C)
- SIGTSTP (Ctrl+Z)
- SIGCHLD (child termination)

Prevents zombie processes and race conditions.

---

### I/O Redirection

Supports:
command < input.txt
command > output.txt
command >> output.txt
command 2> error.txt

---

### Pipelines

Supports multiple commands connected via pipes:
/bin/ls | /usr/bin/grep txt | /usr/bin/wc -l

---

## Concepts Demonstrated

- fork()
- execve()
- waitpid()
- signal handling
- process groups
- pipes
- dup2()
- file descriptors
- race condition prevention using sigprocmask()

---

## Build
gcc tsh.c -o tsh

---

## Run
./tsh


Example:
tsh> /bin/sleep 30 &
tsh> jobs
tsh> fg %1

---

## File Structure
tsh.c
README.md

---

## Educational Purpose

This project was built to understand low-level Unix process management and shell internals.

---

## Author

Tamanna Chandak
