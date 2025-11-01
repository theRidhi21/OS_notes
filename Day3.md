

## 🌟 **Topic 11: System Calls**

### 🧩 What it is:

A **system call** is a **bridge between a program and the operating system**.
When your program wants to do something that requires OS permission — like reading a file, creating a process, or sending data — it uses a **system call**.

Example (in Linux):

```c
read(), write(), open(), close(), fork(), exec(), exit()
```

### ⚙️ Purpose:

* Provides a **safe interface** to access hardware and system resources.
* Keeps user programs separate from kernel (core OS) operations.

### 💼 Corporate World Use:

* Every software — backend service, app, or database — uses system calls in the background.
* Example: When a **Zeta app** reads user data from storage, internally it calls `read()` and `write()` system calls.
* In **cloud or backend engineering**, understanding system calls helps in **performance optimization and debugging**.

---

## 🌟 **Topic 12: Process Concepts**

### 🧩 What it is:

A **process** is a **program in execution**.
It includes the program code, current activity (like register and program counter), and memory.

### ⚙️ Process States:

1. **New** – being created
2. **Ready** – waiting for CPU
3. **Running** – currently executing
4. **Waiting** – waiting for I/O
5. **Terminated** – finished

### 💼 Corporate World Use:

* OS manages multiple processes efficiently — just like companies manage multiple projects at once.
* In **web servers**, each user request is handled by a process or thread.
* Example: When hundreds of users log in to a banking app, each session is a process or lightweight thread.

---

## 🌟 **Topic 13: Process Scheduling**

### 🧩 What it is:

**Scheduling** decides **which process runs next** on the CPU.
It ensures that all processes get fair CPU time and the system remains responsive.

### ⚙️ Types of Schedulers:

1. **Long-term (Job scheduler)** – chooses which programs enter main memory.
2. **Short-term (CPU scheduler)** – selects from ready queue who gets CPU next.
3. **Medium-term** – swaps processes in and out of memory.

### 💼 Corporate World Use:

* This is the logic behind **load balancing** in servers.
* For example, **Zeta or Google Cloud** servers schedule user requests efficiently to avoid lag.
* In operating systems like Linux, scheduling is critical for **performance and responsiveness**.

---

## 🌟 **Topic 14: Operations on Processes**

### 🧩 What it is:

Processes can perform several operations such as:

* **Creation:** A new process is created using `fork()` (in Linux).
* **Execution:** Executes new programs using `exec()`.
* **Termination:** Ends using `exit()`.
* **Communication:** Shares data between processes.

### ⚙️ Parent-Child Relationship:

When a process creates another, it becomes a **parent**, and the new one is a **child process**.

### 💼 Corporate World Use:

* In **web servers**, one main process spawns multiple child processes to handle users.
* Example: Apache web server or Node.js backend spawns worker processes to handle requests.
* In **operating systems**, process creation and management help maintain stability and multitasking.

---

## 🌟 **Topic 15: Cooperating Processes**

### 🧩 What it is:

**Cooperating processes** are those that **share data or resources** with each other to complete a task.

Example: One process produces data; another consumes it — like producer-consumer problem.

### ⚙️ Benefits:

* Information sharing
* Computation speed-up
* Modularity (dividing large tasks)
* Convenience (parallel execution)

### 💼 Corporate World Use:

* This concept is used in **client-server models** and **microservices architecture**.
* Example: In **Zeta**, one service may generate transaction data while another processes and stores it — both cooperate through **Inter-Process Communication (IPC)**.
* In **distributed systems**, cooperation between services ensures **high availability** and **scalability**.

---

## 🌼 **Summary – Today’s Concepts**

| Concept                 | Key Idea                                   | Real-World Example                   |
| :---------------------- | :----------------------------------------- | :----------------------------------- |
| System Calls            | Interface between program & OS             | File access, I/O, process creation   |
| Process Concept         | Program in execution                       | Each user request or app task        |
| Process Scheduling      | Decides which process runs next            | Load balancing in cloud servers      |
| Operations on Processes | Creating, executing, terminating processes | Web servers spawning child processes |
| Cooperating Processes   | Processes sharing data/resources           | Microservices, client-server systems |

---

✨ **In short:**
You’ve now entered the *core* of operating systems — how it handles running programs efficiently.
These are the same ideas used when:

* Multiple users access an app,
* Data moves between services,
* And servers handle thousands of requests simultaneously.

