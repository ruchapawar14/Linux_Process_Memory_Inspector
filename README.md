# 🧠 Linux Process Memory Inspector

> A Linux system programming project in C that analyzes the memory layout of a running process using the `/proc` filesystem.

---

## 📌 Project Overview

**Linux Process Memory Inspector** is a Linux-based system utility developed in C that allows users to inspect process information and analyze memory mappings of a running process using its Process ID (PID).

The project reads information from:

- `/proc/<pid>/status`
- `/proc/<pid>/maps`

and displays details about:

- Process state
- Threads
- Memory regions
- Permissions
- Section types

This project demonstrates core concepts of **Linux System Programming, Proc Filesystem Parsing, Process Memory Organization, and Virtual Memory Analysis**.

---

## 🧠 Key Features

### 📄 Process Information Inspection
- Reads process details using `/proc/<pid>/status`
- Displays:
  - Process Name
  - PID
  - Process State
  - Thread Count

### 🗂️ Memory Layout Analysis
- Reads `/proc/<pid>/maps`
- Displays:
  - Start Address
  - End Address
  - Memory Size
  - Permissions
  - Section Type
  - Region Details

### 🧩 Memory Section Classification
- Identifies important memory sections such as:
  - HEAP
  - STACK
  - TEXT
  - DATA
  - VDSO
  - VVAR
  - OTHER

### 🔍 Permission-Based Analysis
- Interprets memory permissions:
  - Read
  - Write
  - Execute

### ⚙️ PID-Based Runtime Analysis
- Dynamically inspects any running process using PID
- Provides real-time process memory analysis

### 🐧 Linux System Programming
- Uses Linux `/proc` filesystem
- Demonstrates low-level process inspection techniques

---

## 🎯 Learning Outcomes

- Practical experience with Linux System Programming
- Understanding Linux `/proc` filesystem
- Process metadata inspection
- Virtual memory layout analysis
- Memory segment classification
- Structured file parsing in C
- Permission interpretation
- File handling using C programming

---

## 🛠️ Technologies Used

- C Programming
- Linux Operating System
- GCC Compiler
- Proc Filesystem (`/proc`)

---

## ▶️ Compilation

```bash
gcc inspector.c -o inspector
```

---

## ▶️ Execution

```bash
./inspector
```

Enter a valid PID when prompted.

---

## 📌 Sample Output

```text
----------------------------------------------------------
----------- Linux Process Memory Inspector ----------------
----------------------------------------------------------

Enter the PID of a process that you want to inspect
1234

Name: bash
Pid: 1234
State: S (sleeping)
Threads: 1

55d8f7f00000 55d8f7f21000 132 r-xp TEXT /usr/bin/bash
7ffd2d0b9000 7ffd2d0da000 132 rw-p STACK [stack]
```

---

## 🚀 Future Enhancements

- Colored terminal output
- Shared library detection
- Export analysis report
- GUI-based interface
- Process listing feature
- Advanced memory statistics

---

## 👩‍💻 Author

### Rucha Hanumant Pawar
