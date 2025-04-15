# 🎬 Movie Rating Histogram  
*A MapReduce job to count movie ratings using Python*

![Python](https://img.shields.io/badge/Python-3.x-blue) 
![mrjob](https://img.shields.io/badge/Library-mrjob-green) 
![MapReduce](https://img.shields.io/badge/Pattern-MapReduce-orange)

---

## 📦 Overview

A lightweight MapReduce implementation that analyzes movie rating frequency from tab-separated data. Built for scalability — works locally or on Hadoop clusters.

---

## ⚡ Quick Start

### ✅ Prerequisites

Install the `mrjob` library:

bash
pip install mrjob
```
### ▶️ How It Works

| Component | Action              | Example                                   |
|-----------|---------------------|-------------------------------------------|
| Mapper    | Emits `(movieID, 1)`| `"u1 m10 4.5 12345"` → `("m10", 1)`        |
| Reducer   | Sums the counts     | `("m10", [1, 1])` → `("m10", 2)`           |

📊 Sample Output

"10"    29  

"20"    15

userID    movieID    rating    timestamp

```
