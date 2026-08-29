# 🎄 Advent of Code 2025 — Day 1: *Secret Entrance* 🔐


## 📘 Challenge Summary
The elves set up a giant circular lock with **100 positions (0–99)**.  
You begin at **position 50** and follow a sequence of rotations like `L68`, `R23`, etc.

### **Part 1 – Count zeroes at the *end* of rotations**
Every time a rotation finishes *exactly* at position `0`, increment the password.

<img width="1404" height="639" alt="Screenshot 2025-12-01 215012" src="https://github.com/user-attachments/assets/b9bd17ba-76fb-4ba0-ac2b-540f18aa54a1" />


### **Part 2 – Count *every* time the dial hits 0**
A rotation may pass through `0` many times.  
Example: Starting at 50 → `R1000` hits `0` **10 times**.

<img width="1403" height="678" alt="Screenshot 2025-12-01 234915" src="https://github.com/user-attachments/assets/be4a4c41-1289-4c3b-b8ea-8ab8170ddeff" />


Your task: Using the rotation list, compute the final password.

---

## 🧪 Example

Start: 50

L68 → hits 0 once  
L30  
R48 → ends at 0  
L5  
R60 → hits 0 once  
L55 → ends at 0  
L1  
L99 → ends at 0  
R14  
L82 → hits 0 once

**Part 1 Output:** 3  
**Part 2 Output:** 6

---

## 🛠️ Solution Outline
- Treat the dial as infinite rotation in both directions  
- Count each pass over `0` (including landing exactly on it)  
- Use modular arithmetic for end positions  
- Use absolute movement to compute the number of zero-crossings efficiently

---

## 📄 Final Answers (My Input)
| Part | Answer |
|------|--------|
| **1** | **1139** |
| **2** | **6684** |

---
