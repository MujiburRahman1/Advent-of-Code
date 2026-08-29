# 🎄 Advent of Code 2025 — Day 11: *Reactor*  
Tracing every possible data path through a tangled network of devices.  

---

## 📌 Challenge Summary
You're given a directed graph of devices where data flows **forward only**.  
Your mission: analyze how many unique ways data can travel between key devices inside a reactor system.

---

### **Part 1**
You're positioned at device **`you`** and must determine how many unique paths eventually reach the main output **`out`**.

Your goal:  
Count *all* possible directed paths from **you → out**.
---

### **Part 2**
The Elves discovered the faulty path must include **both** critical devices:  
- `dac` (digital-to-analog converter)  
- `fft` (Fourier transform unit)

Your goal:  
Count all paths from **svr → out** that *must pass through* **both `dac` and `fft`**, in *any* order.

---

## 🧪 Sample Example & Outputs

For the provided sample networks, valid paths include all direct graph-traversal routes that follow outbound connections only.

### **Example Results**
The sample diagrams show multiple paths between source and output, but only a subset satisfy the Part 2 condition of visiting both required nodes.

### **Example Sums**
- **Part 1 Sample Sum:** `5`  
- **Part 2 Sample Sum:** `2`  

---

## 🧠 Solution Outline

### ⚡ Strategy (Optimized for speed)
- Represent the device map as an adjacency list for **O(1)** traversal.  
- Use **DFS + memoization** to avoid recomputing paths in overlapping subgraphs.  
- For Part 2, track a compact **bitmask state** to mark whether `dac` and `fft` have been visited.  
- Time efficiency: **O(V + E)** for both parts.  
- Produces fast results even for large reactor networks.

---

## 🏁 Results (Based on My Actual Input)

| Part | Answer |
|------|--------|
| **1** | **696** |
| **2** | **473741288064360** |

---
