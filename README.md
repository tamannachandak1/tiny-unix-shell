# Tiny Unix Shell (C, Linux)

A Unix-style shell implemented in C supporting job control and signal handling.

## Features

- Foreground and background job execution
- Job control (fg, bg, jobs)
- Signal handling (SIGINT, SIGTSTP, SIGCHLD)
- Process group management
- Built using POSIX APIs

## Concepts demonstrated

- fork / exec
- waitpid
- signals
- process lifecycle
- race condition prevention

## How to compile

```bash
gcc tsh.c -o tsh
./tsh
