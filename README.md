# 🚚 Vehicle Routing Problem (VRP) using Genetic Algorithm

## 📌 Project Overview
This project implements a **Genetic Algorithm (GA) for solving the Vehicle Routing Problem (VRP)**. The goal is to optimize delivery routes for multiple vehicles while minimizing the total travel distance and balancing the workload among vehicles.

## 🔍 Problem Statement
Given:
- A **depot (central location)** where all vehicles start and end their journey.
- A set of **randomly generated delivery locations**.
- A fixed number of **vehicles** to complete the deliveries.

The objective is to **minimize the total distance traveled** and **ensure a balanced distribution of workload** across all vehicles.

## 📂 Dataset Information
- The delivery locations are **randomly generated within a 100x100 grid**.
- Each vehicle must start and end at the **depot (fixed at (50, 50))**.
- The number of vehicles is **configurable** (default: **3 vehicles**).

## 🛠️ Solution Approach
✔️ **Genetic Algorithm (GA)** for route optimization  
✔️ **K-Means clustering** to group locations (if needed)  
✔️ **Multi-Objective Optimization** for balancing workload  
✔️ **Matplotlib visualization** for route plotting  

## 🤖 Genetic Algorithm Setup
### **1️⃣ Representation of Individuals**
- Each individual represents a **permutation** of delivery locations.
- The list of locations is **divided among vehicles** to form separate routes.

### **2️⃣ Fitness Function**
- **Objective 1**: Minimize **total route distance**.
- **Objective 2**: Minimize **imbalance** (standard deviation of route distances among vehicles).

### **3️⃣ Evolutionary Operators**
- **Selection**: Tournament Selection (chooses the best individuals from a random subset).
- **Crossover**: Partially Matched Crossover (PMX) for preserving valid permutations.
- **Mutation**: Shuffle Mutation (randomly swaps two locations with a 5% probability).

## 📌 How to Run the Project
1. **Clone the repository**
   ```bash
   git clone https://github.com/Deepakjd-dev/VRP.git
   
   cd VRP
   ```
2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the Python script**
   ```bash
   python VRP.py
   ```
4. **Output**:
   - **Plots the optimized vehicle routes** 📍
   - **Displays genetic algorithm performance over generations** 📈
   - **Shows the best fitness values (shortest & balanced route)** 🏆

## 📊 Results & Insights
| Model Configuration | Avg. Route Distance | Balance Penalty |
|---------------------|---------------------|-----------------|
| Initial Random Routes | 333.56 | 1.15 |
| Optimized (Genetic Algorithm) | **203.89** | **2.49** |

📌 The optimized routes **reduce travel distance by ~39%** while maintaining a **balanced workload among vehicles**.

## 🚀 Future Enhancements
🔹 Implement **real-world datasets** for delivery optimization  
🔹 Introduce **time windows** and traffic conditions  
🔹 Deploy as a **web application** for interactive route planning  

## 🏆 Contributors
👨‍💻 **Your Name** – [GitHub Profile](https://github.com/Vasanthrk29)

## 📜 License
This project is licensed under the **MIT License**. Feel free to use and modify!
