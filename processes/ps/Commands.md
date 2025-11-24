# ps Command Handbook  
(A complete guide to all ps variants for macOS and Linux)

The `ps` command (process status) is one of the most fundamental tools for inspecting running processes.  
This document covers all major variants and usage patterns of `ps` in both macOS (BSD ps) and Linux (GNU ps).  
Real terminal outputs are stored separately in `outputs.md`.

---

## 1. Basic ps

### Example 1 — Processes in the current terminal
**Command:**
```
ps
```
(See `outputs.md` for sample output.)

### Example 2 — Processes belonging to your user
**Command:**
```
ps -u $USER
```

### Example 3 — Full-format output
**Command:**
```
ps -f
```

---

## 2. ps aux — Full system process list

`ps aux` displays every process running on the system, including daemons, user programs, background tasks, and system services.  
A daemon is a background service process that runs continuously and handles system-level tasks without direct user control.

### Example — First few processes
**Command:**
```
ps aux | head
```
(Sample output located in `outputs.md`.)

### Filtering a specific process
```
ps aux | grep python
```

### Differences (Linux vs macOS)
- Linux supports the `--sort` flag  
- macOS does not; sorting requires the external `sort` command  

---

## 3. Sorting Processes by CPU and Memory

### macOS (BSD ps)

Sort by CPU:
```
ps aux | sort -nr -k 3 | head
```

Sort by memory:
```
ps aux | sort -nr -k 4 | head
```

### Linux (GNU ps)

Sort by CPU:
```
ps aux --sort=-%cpu | head
```

Sort by memory:
```
ps aux --sort=-%mem | head
```

---

## 4. Filtering with ps + grep

Find Chrome processes:
```
ps aux | grep Chrome
```

Find processes using port 8080:
```
ps aux | grep 8080
```

Exclude grep itself:
```
ps aux | grep python | grep -v grep
```

---

## 5. Custom Output (ps -o)

Show PID, PPID, and command:
```
ps -o pid,ppid,command
```

Show CPU, memory, and command:
```
ps -o %cpu,%mem,command
```

---

## 6. Inspecting Specific PIDs

Single PID:
```
ps -p <PID> -o pid,ppid,%cpu,%mem,command
```

Multiple PIDs:
```
ps -p 100,200,300
```

---

## 7. Viewing Processes of Another User

```
ps -u root
```

---

## 8. Counting Processes

Total processes running:
```
ps aux | wc -l
```

Processes owned by the current user:
```
ps -u $USER | wc -l
```

---

## 9. Process Tree View

macOS:
```
brew install pstree
pstree
```

Linux:
```
ps auxf
```

---

## 10. STAT Column Meanings

Common process states:

- R = Running  
- S = Sleeping  
- D = Uninterruptible sleep  
- T = Stopped  
- Z = Zombie  
- Ss = System daemon  
- R+ = Running in the current terminal  

---

## 11. TTY Column Meaning

- `??` = no terminal (this is typical for daemons and background services)  
- `ttys000` = a terminal session  
- `console` = system login console  

---

## Real-World Use Cases

- Identifying CPU-heavy or memory-intensive processes  
- Killing or restarting stuck programs  
- Investigating daemons and background services  
- Tracing parent/child relationships between processes  
- Debugging slow or unresponsive systems  
- Finding command lines for long-running jobs  
- Filtering processes by application or keyword  

---

## Additional ps Variants (coming later)

This folder will eventually include detailed sub-guides such as:

- ps aux deep dive  
- Sorting processes  
- ps with grep  
- ps process trees  
- ps vs top  
- ps differences: macOS vs Linux  

---
