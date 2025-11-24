# Advanced Linux Fundamentals and Tools  
A structured, hands-on repository to build complete command-line mastery.  
Every topic is organized into modules, and every command includes:
- a `commands.md` file (concepts, usage, variations)  
- an `outputs.md` file (real command outputs captured from your machine)  

This creates an interactive, practical learning system instead of passive notes.

---

## Repository Purpose

This project is designed to build deep Linux comfort from the ground up.  
Each module focuses on an essential domain: processes, filesystem, permissions, networking, monitoring, Bash scripting, SSH, compression, and distribution-level tools.

The goal is to make you independent, confident, and fluent in real-world Linux workflows:
- debugging slow systems  
- controlling processes  
- navigating complex directory structures  
- inspecting ports and open files  
- managing permissions  
- writing automation scripts  
- interacting with servers and SSH environments  
- working with both macOS (BSD utilities) and Linux (GNU utilities)  

---

## Repository Structure

```
Advanced-linux-fundamentals-and-tools/
 ├── processes/
 │     ├── ps/
 │     │     ├── commands.md
 │     │     └── outputs.md
 │     ├── top/
 │     ├── htop/
 │     ├── pstree/
 │     ├── pgrep/
 │     ├── pkill/
 │     ├── kill/
 │     ├── lsof/
 │     ├── netstat-ss/
 │     └── nice-renice/
 │
 ├── filesystem/
 ├── networking/
 ├── permissions/
 ├── monitoring/
 ├── bash/
 ├── ssh/
 ├── compression/
 ├── distro/
 └── README.md
```

Each subfolder will eventually contain its own set of tools with clear, practical breakdowns.

---

## Module 1: Processes (Current Module)

This module focuses on understanding and controlling processes on macOS and Linux.

Included tools:
- `ps`  
- `top`  
- `htop`  
- `pstree`  
- `pgrep`  
- `pkill`  
- `kill`  
- `lsof`  
- `netstat` / `ss`  
- `nice` / `renice`  

Every folder contains:
- `commands.md` → theory, command variations, flags, and explaining when to use what  
- `outputs.md` → real examples pasted from the user's own terminal  

This dual-file structure makes learning active instead of passive.

---

## Future Modules

### Module 2 — Filesystem & Navigation  
Commands like `ls`, `tree`, `find`, `du`, `df`, `stat`, `rm`, `cp`, `mv`.

### Module 3 — Permissions & Ownership  
Understanding `chmod`, `chown`, octal permissions, symbolic modes, sticky bits.

### Module 4 — Networking Essentials  
`curl`, `ping`, `wget`, `ifconfig/ip`, `dig`, `traceroute`, and port inspection.

### Module 5 — Monitoring & Logs  
`dmesg`, `vmstat`, `iostat`, `journalctl`, `/var/log`.

### Module 6 — Bash Scripting  
Variables, loops, conditions, functions, automation patterns.

### Module 7 — Advanced System Tools  
`grep`, `sed`, `awk`, `rsync`, `jq`, `xargs`, and more.

### Module 8 — Package Management  
`apt`, `yum`, `brew`, `snap`.

---

## Mini-Projects

After completing all modules, the repository will include two hands-on Linux mini-projects:

### 1. System Doctor  
A script that generates a full system health report using all process, monitoring, and networking tools.

### 2. Server Debugger Toolkit  
A set of short utilities for inspecting ports, processes, logs, permissions, and file usage.

---

## Philosophy

This repository is built on:
- command fluency  
- real-world practice  
- clean organization  
- reproducibility  
- long-term engineering growth  

Every command is tested, documented, and explained in plain English.  
Every output is real and captured manually for maximum learning impact.

---

## Author  
**Parth Ashtikar**  
This repo is part of a long-term learning arc toward full Linux mastery, high-level engineering workflows, and research-oriented automation.

