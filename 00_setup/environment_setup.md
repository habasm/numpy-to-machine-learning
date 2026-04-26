
# Environment Setup

## 1. Create Virtual Environment

```bash
python -m venv venv
````

## 2. Activate Environment

### Windows

```bash
venv\Scripts\activate
```

### Mac/Linux

```bash
source venv/bin/activate
```

## 3. Install Requirements

```bash
pip install -r requirements.txt
```

## 4. Launch Jupyter

```bash
jupyter notebook
```

## 📓 `how_to_run.ipynb`

### Structure (VERY IMPORTANT — reuse this pattern everywhere)

Each notebook should follow this flow:

---

### 🧱 1. Title + Goal

```python
# How to Run This Course

"""
Goal:
- Learn how to execute notebooks
- Understand workflow
"""
````

---
### ⚙️ 2. Imports

```python
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
```

---

### 🧪 3. Test Code

```python
arr = np.array([1, 2, 3])
print("Array:", arr)
print("Mean:", arr.mean())
```

---

### 📊 4. Visualization Example

```python
plt.plot(arr)
plt.title("Simple Plot")
plt.show()
```
