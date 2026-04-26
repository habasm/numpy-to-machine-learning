````md
# 🚀 NumPy Performance Tips

This guide helps you write **fast, efficient, and scalable NumPy code** — essential for machine learning and data processing.

---

## ⚡ 1. Use Vectorization (Avoid Loops)

❌ Slow:
```python
result = []
for x in arr:
    result.append(x * 2)
````

✅ Fast:

```python
result = arr * 2
```

👉 Why:

* NumPy runs in optimized C under the hood
* Loops in Python are slow

---

## 📦 2. Use Built-in Functions

❌ Manual:

```python
total = 0
for x in arr:
    total += x
```

✅ Optimized:

```python
total = np.sum(arr)
```

👉 Built-ins are heavily optimized

---

## 🧠 3. Choose the Right Data Type

```python
arr = np.array([1, 2, 3], dtype=np.float32)
```

👉 Why:

* float32 uses less memory than float64
* Important for large datasets / ML

---

## 📐 4. Avoid Unnecessary Copies

❌ Creates copy:

```python
b = a.copy()
```

✅ Use views when possible:

```python
b = a[:]
```

👉 Copies waste memory and time

---

## 🔄 5. Preallocate Arrays

❌ Inefficient:

```python
arr = []
for i in range(1000):
    arr.append(i)
```

✅ Efficient:

```python
arr = np.zeros(1000)
```

---

## ⚙️ 6. Use Broadcasting

```python
arr = np.array([1, 2, 3])
result = arr + 5
```

👉 No loops, faster execution

---

## 📊 7. Use Efficient Linear Algebra

```python
np.dot(a, b)
np.matmul(A, B)
```

👉 These are optimized with BLAS libraries

---

## 🔍 8. Profile Your Code

```python
import time

start = time.time()
# your code
end = time.time()

print(end - start)
```

👉 Measure performance — don’t guess

---

## 🧠 9. Use NumPy Instead of Python Lists

❌ Python list:

```python
a = [1, 2, 3]
```

✅ NumPy array:

```python
a = np.array([1, 2, 3])
```

👉 Arrays are:

* faster
* memory efficient
* vectorized

---

## 🔥 10. Avoid Python Functions Inside Loops

❌ Slow:

```python
for x in arr:
    np.sqrt(x)
```

✅ Fast:

```python
np.sqrt(arr)
```

---

## 🧩 Summary

| Technique     | Benefit         |
| ------------- | --------------- |
| Vectorization | Speed ⚡         |
| Broadcasting  | Simplicity 🧠   |
| Built-ins     | Optimization 🚀 |
| Preallocation | Memory 💾       |

---

## 🎯 Golden Rule

> "If you're writing a loop in NumPy, you're probably doing it wrong."

````