## 📄 README.md

```markdown
# Deadlocks Demonstration (C / POSIX Threads)

## 📌 Overview
This project demonstrates how **deadlocks occur in multithreaded programs** using POSIX threads (`pthread`) in C.

A deadlock happens when two or more threads wait indefinitely for resources held by each other, causing the program to stop making progress.

This project is intended for:
- Operating Systems learning
- Concurrency concepts practice
- Multithreading demonstrations
- Systems programming education

---

## 🧠 Deadlock Concept

A deadlock occurs when four conditions exist simultaneously:

1. **Mutual Exclusion** – Resources cannot be shared.
2. **Hold and Wait** – Threads hold one resource while waiting for another.
3. **No Preemption** – Resources cannot be forcibly taken.
4. **Circular Wait** – Threads wait in a circular chain.

---

## 🧵 How This Demo Works

The program creates two threads:

- Thread 1 locks `lock1`, then waits for `lock2`
- Thread 2 locks `lock2`, then waits for `lock1`

This creates a circular dependency, causing the program to freeze (deadlock).

Example Output:
```

Thread 1: locked lock1
Thread 2: locked lock2
Thread 1: waiting for lock2
Thread 2: waiting for lock1

````

At this point, the program will stop progressing.

---

## 🛠 Requirements

- Linux / WSL (Recommended)
- GCC Compiler
- POSIX Thread Library

Install dependencies (Ubuntu / WSL):
```bash
sudo apt update
sudo apt install build-essential
````

---

## ▶️ Compile and Run

Compile:

```bash
gcc deadlock.c -o deadlock -lpthread
```

Run:

```bash
./deadlock
```

---

## 📂 Project Structure

```
Deadlocks/
│
├── deadlock.c
├── README.md
└── LICENSE
```

---

## 🎯 Learning Goals

This project helps demonstrate:

* Thread synchronization
* Mutex locking
* Race conditions
* Deadlock creation
* Concurrency debugging basics

---

## ⚠️ Note

This code intentionally creates a deadlock for educational purposes.
Do **not** use this pattern in production systems.

---

## 📚 Technologies Used

* C Programming Language
* POSIX Threads (pthread)
* GCC Compiler
* Linux / WSL Environment

---

## 👤 Author

**Dixon Codes**

---

## 📜 License

This project is licensed under the MIT License.

```
