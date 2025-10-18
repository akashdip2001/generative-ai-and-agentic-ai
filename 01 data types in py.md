# 🧠 1. Python Built-in Data Types (Overview)

```mermaid
graph TD
    A["Python Data Types"] --> B["Text Type"]
    A --> C["Numeric Types"]
    A --> D["Sequence Types"]
    A --> E["Mapping Type"]
    A --> F["Set Types"]
    A --> G["Boolean Type"]
    A --> H["Binary Types"]
    A --> I["None Type"]

    B --> B1["str"]
    C --> C1["int"]
    C --> C2["float"]
    C --> C3["complex"]
    D --> D1["list"]
    D --> D2["tuple"]
    D --> D3["range"]
    E --> E1["dict"]
    F --> F1["set"]
    F --> F2["frozenset"]
    G --> G1["bool"]
    H --> H1["bytes"]
    H --> H2["bytearray"]
    H --> H3["memoryview"]
    I --> I1["NoneType"]
```

## 🧠 Python Data Types Overview

### **1. Standard Classification**

| Category       | Data Types                         |
| -------------- | ---------------------------------- |
| Text Type      | `str`                              |
| Numeric Types  | `int`, `float`, `complex`          |
| Sequence Types | `list`, `tuple`, `range`           |
| Mapping Type   | `dict`                             |
| Set Types      | `set`, `frozenset`                 |
| Boolean Type   | `bool`                             |
| Binary Types   | `bytes`, `bytearray`, `memoryview` |
| None Type      | `NoneType` (`None`)                |

---

## 🧩 **1. Text Type: String (`str`)**

**Immutable**

### Example

```python
name = "Aromatic and Bold"
```

### Operations

* Indexing → `name[0]  # 'A'`
* Slicing → `name[0:3]  # 'Aro'`
* Concatenation → `name + " Coffee"`
* Methods → `.upper()`, `.split()`, `.replace()`

### Diagram

```
String
 ├── core
 ├── indexing
 ├── slicing
 └── encoding-decoding
```

🧱 Immutable → once created, can’t change individual characters.

```mermaid
graph TD
    A["String (Immutable)"] --> B["Core"]
    A --> C["Indexing"]
    A --> D["Slicing"]
    A --> E["Encoding / Decoding"]

    F["Example: 'Aromatic and Bold'"] --> G["Index 0: 'A'"]
    F --> H["Index 1: 'r'"]
```

---

## 🔢 **2. Numeric Types**

### (a) **int**

Whole numbers (no decimals)

```python
x = 10
y = -3
```

### (b) **float**

Decimal or floating-point numbers

```python
pi = 3.14159
```

### (c) **complex**

Numbers with real and imaginary parts

```python
z = 2 + 3j
```

### Diagram

```
Numeric
 ├── int
 ├── float
 └── complex
```

```mermaid
graph TD
    A["Numeric Types"] --> B["int"]
    A --> C["float"]
    A --> D["complex"]

    B --> B1["Example: x = 10"]
    C --> C1["Example: pi = 3.14"]
    D --> D1["Example: z = 2 + 3j"]
```

---

---

## 📜 **3. Sequence Types**

```mermaid
graph TD
    A["Sequence Types"] --> B["list (Mutable)"]
    A --> C["tuple (Immutable)"]
    A --> D["range (Immutable)"]

    B --> B1["Example: ['apple', 'banana', 'cherry']"]
    B --> B2["Methods: append(), remove(), sort()"]
    C --> C1["Example: (10, 20, 30)"]
    C --> C2["Immutable, supports indexing/slicing"]
    D --> D1["Example: range(5) => 0,1,2,3,4"]
```

### (a) **List**

**Mutable**

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("mango")
```

* Indexing / slicing supported
* Can change, add, remove elements

**Diagram**

```
List
 ├── append()
 ├── remove()
 ├── slicing
 └── iteration
```

---

### (b) **Tuple**

**Immutable**

```python
coords = (10, 20, 30)
```

* Similar to list but can’t modify values.

**Diagram**

```
Tuple
 ├── indexing
 ├── slicing
 └── immutable
```

---

### (c) **Range**

Used with loops, generates sequences

```python
r = range(5)  # 0,1,2,3,4
```

---

## 🧭 **4. Mapping Type: Dictionary (`dict`)**

```mermaid
graph TD
    A["Dictionary (Mutable)"] --> B["Keys"]
    A --> C["Values"]
    A --> D["Items"]
    A --> E["Methods: update(), pop(), clear()"]

    F["Example: {'name': 'Alex', 'age': 21}"] --> G["student['name'] = 'Alex'"]
```

**Mutable**, key–value pairs

```python
student = {"name": "Alex", "age": 21, "grade": "A"}
print(student["name"])  # Alex
```

**Diagram**

```
Dictionary
 ├── keys()
 ├── values()
 ├── items()
 └── update(), pop()
```

---

## 🧮 **5. Set Types**

```mermaid
graph TD
    A["Set Types"] --> B["set (Mutable)"]
    A --> C["frozenset (Immutable)"]

    B --> B1["Unique Elements"]
    B --> B2["Supports Union, Intersection, Difference"]
    C --> C1["Immutable and Unordered"]

    D["Example: {'red', 'green', 'blue'}"]
```

### (a) **set**

**Mutable**, unordered unique elements

```python
colors = {"red", "green", "blue"}
```

Operations: union, intersection, difference.

### (b) **frozenset**

**Immutable version of set**

```python
fset = frozenset(["a", "b", "c"])
```

---

## ⚙️ **6. Boolean Type (`bool`)**

```mermaid
graph TD
    A["Boolean Type"] --> B["True"]
    A --> C["False"]
    D["Example: 5 > 2 → True"]
```

```python
is_active = True
print(5 > 2)  # True
```

**Diagram**

```
Boolean
 ├── True
 └── False
```

---

## 🧵 **7. Binary Types**

```mermaid
graph TD
    A["Binary Types"] --> B["bytes (Immutable)"]
    A --> C["bytearray (Mutable)"]
    A --> D["memoryview (Mutable)"]

    B --> B1["Example: b'hello'"]
    C --> C1["Example: bytearray(5)"]
    D --> D1["Example: memoryview(b'hello')"]
```

| Type       | Mutable | Example                |
| ---------- | ------- | ---------------------- |
| bytes      | ❌       | `b"hello"`             |
| bytearray  | ✅       | `bytearray(5)`         |
| memoryview | ✅       | `memoryview(b"hello")` |

Used for low-level data manipulation, e.g. file I/O or networking.

---

## 🕳 **8. None Type**

```mermaid
graph TD
    A["NoneType"] --> B["Represents no value"]
    B --> C["Example: x = None"]
```

Represents **absence of value**

```python
x = None
```

**Diagram**

```
NoneType
 └── represents no value
```

---

## 🔒 **Mutability Summary**

| Type       | Mutable | Example            |
| ---------- | ------- | ------------------ |
| int        | ❌       | 10                 |
| float      | ❌       | 10.5               |
| complex    | ❌       | 2+3j               |
| str        | ❌       | "hello"            |
| tuple      | ❌       | (1,2,3)            |
| list       | ✅       | [1,2,3]            |
| dict       | ✅       | {"a":1}            |
| set        | ✅       | {"a","b"}          |
| frozenset  | ❌       | frozenset({1,2,3}) |
| bool       | ❌       | True               |
| bytes      | ❌       | b"abc"             |
| bytearray  | ✅       | bytearray(3)       |
| memoryview | ✅       | memoryview(b"abc") |
| NoneType   | ❌       | None               |

```mermaid
graph LR
    A["Immutable"] --> A1["int"]
    A --> A2["float"]
    A --> A3["complex"]
    A --> A4["str"]
    A --> A5["tuple"]
    A --> A6["frozenset"]
    A --> A7["bytes"]
    A --> A8["bool"]
    A --> A9["NoneType"]

    B["Mutable"] --> B1["list"]
    B --> B2["dict"]
    B --> B3["set"]
    B --> B4["bytearray"]
    B --> B5["memoryview"]
```

---
