# 📄 `common_mistakes.md`

```md
# ⚠️ Common NumPy Mistakes (and How to Avoid Them)

These are mistakes beginners (and even intermediate learners) make — fixing them will level you up fast.

---

## ❌ 1. Using Python Loops Instead of Vectorization

```python
# WRONG
for x in arr:
    print(x * 2)
````

```python
# RIGHT
print(arr * 2)
```

---

## ❌ 2. Confusing Shape and Dimension

```python
arr.shape   # (rows, cols)
arr.ndim    # number of dimensions
```

👉 Many bugs come from misunderstanding shapes

---

## ❌ 3. Wrong Broadcasting Assumptions

```python
a = np.array([[1,2,3]])
b = np.array([1,2])

a + b  # ❌ ERROR
```

👉 Shapes must align properly

---

## ❌ 4. Modifying Copies Instead of Original

```python
b = a.copy()
b[0] = 100
```

👉 `a` is unchanged

---

## ❌ 5. Forgetting Axis Parameter

```python
np.sum(arr)        # total
np.sum(arr, axis=0)  # column-wise
np.sum(arr, axis=1)  # row-wise
```

👉 Missing axis = wrong results

---

## ❌ 6. Using List Instead of NumPy Array

```python
a = [1,2,3]
a * 2   # [1,2,3,1,2,3]
```

```python
a = np.array([1,2,3])
a * 2   # [2,4,6]
```

---

## ❌ 7. Ignoring Data Types

```python
arr = np.array([1,2,3])
```

👉 Default might not be optimal

---

## ❌ 8. Not Setting Random Seed

```python
np.random.rand(3)
```

👉 Results change every run

✅ Fix:

```python
np.random.seed(42)
```

---

## ❌ 9. Inefficient Memory Usage

```python
large = np.zeros((10000, 10000))
```

👉 Can crash your system

---

## ❌ 10. Misunderstanding `=` vs Copy

```python
b = a
b[0] = 10
```

👉 This changes `a` too!

---

## 🧠 Debug Tip

Always check:

```python
print(arr.shape)
print(arr.dtype)
```

---

## 🔥 Pro Insight

> "Most NumPy bugs are not logic errors — they are shape errors."

---

## 🎯 Final Advice

* Think in **arrays, not loops**
* Always check **shape**
* Use **vectorization first**

---

## 🚀 You're Ready If You Can:

* Replace loops with NumPy
* Fix shape mismatches
* Use broadcasting correctly

```