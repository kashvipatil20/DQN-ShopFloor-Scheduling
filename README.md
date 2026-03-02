# 🚀 DQN-Based Dynamic Job Shop Scheduling System

## 📌 Project Overview

This project implements a **Deep Q-Network (DQN)** based reinforcement learning solution to solve a **Dynamic Job Shop Scheduling Problem (JSSP)** under realistic industrial constraints.

Unlike traditional static scheduling systems, this model handles real-world manufacturing complexities such as:

- Multi-operation jobs (OP10, OP20, OP30, etc.)
- Multiple routing options per operation (Option 1, 2, 3)
- Machine breakdowns (planned & unexpected)
- Operator availability constraints
- Fixture constraints
- Raw material constraints
- Batch-based order processing
- Due date penalties
- Dynamic rescheduling

The objective is to **minimize makespan, tardiness, and idle time penalties** while learning an adaptive scheduling policy.

---

## 🎯 Problem Statement

In real-world manufacturing systems, job shop scheduling becomes highly complex due to:

- Competing resource constraints
- Dynamic failures
- Multiple routing alternatives
- Strict customer deadlines
- Variable batch sizes

Traditional heuristic methods (e.g., Nearest Due Date) often fail to adapt dynamically.

This project models the shop floor as a **custom reinforcement learning environment**, where a DQN agent learns an optimal scheduling strategy through interaction and reward feedback.

---

## 🧠 Methodology

### 1️⃣ Custom Shop Floor Environment

A custom OpenAI Gym–style environment was designed to simulate:

- Multiple jobs with sequential operations
- Option-based routing (different machines for same operation)
- Machine and operator availability tracking
- Planned maintenance and random breakdown simulation
- Batch splitting logic
- Time-based event progression (smart WAIT handling)
- Due date and penalty calculation

The state representation includes:

- Machine availability status
- Operator status
- Remaining operations
- Due dates
- Current simulation time
- Batch details

---

### 2️⃣ Deep Q-Network (DQN) Agent

The reinforcement learning setup includes:

- Fully connected neural network (PyTorch)
- Experience Replay Buffer
- Epsilon-Greedy exploration
- Target Q-value updates
- Reward shaping

Reward components:

- ✔ Priority reward  
- ✔ Tardiness penalty  
- ✔ Idle machine penalty  
- ✔ Makespan penalty  
- ✔ Escalating WAIT penalty  

---

### 3️⃣ Scheduling Strategy Comparison

The learned policy can be compared against:

- Nearest Due Date (NDD) heuristic
- Static scheduling baseline

This allows evaluation of RL performance improvements over traditional methods.

---

## 📊 Key Features

✔ Dynamic job shop simulation  
✔ Multi-option routing support  
✔ Batch-based process time scaling  
✔ Machine & operator failure simulation  
✔ Due date penalty modeling  
✔ Smart time advancement during WAIT  
✔ Human-readable Gantt chart visualization  
✔ Excel-based shop floor input handling  

---

## 🛠 Technology Stack

- Python
- PyTorch
- Pandas
- NumPy
- Matplotlib
- OpenAI Gym (Custom Environment)

---

## 📈 Results

The DQN agent learns to:

- Reduce total tardiness
- Reduce makespan
- Improve resource utilization
- Adapt to machine/operator failures

Compared to static heuristics, the RL-based system demonstrates improved adaptability in dynamic environments.

## 👩‍💻 Author

**Kashvi Patil**  
GitHub: https://github.com/kashvipatil20  

---

## ⭐ If You Found This Interesting

Feel free to fork the repository or connect for collaboration.

