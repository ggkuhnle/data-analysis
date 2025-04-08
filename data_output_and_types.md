
# 🧾 Output and Data Types in Python

This guide introduces how Python handles different types of data and how you can output results clearly and effectively.

---

## 🖨️ Printing and Output

The `print()` function is used to show output:

```python
print("Hello, world!")
```

You can print variables:

```python
name = "Hugo"
print(name)
```

You can also combine text and variables using **f-strings**:

```python
hippo_weight = 1500
print(f"The hippo weighs {hippo_weight} kg")
```

---

## 🧠 What Are Data Types?

A **data type** defines what kind of data you're working with. Python automatically assigns data types when you create a variable.

You can check the type with:

```python
type(x)
```

---

## 🔢 Common Data Types

| Type         | Description                             | Example                        |
|--------------|-----------------------------------------|--------------------------------|
| `int`        | Integer (whole number)                  | `3`, `1500`, `-12`             |
| `float`      | Decimal number                          | `3.14`, `1500.0`               |
| `str`        | String (text)                           | `"hippo"`, `'hello'`           |
| `bool`       | Boolean (True/False)                    | `True`, `False`                |
| `list`       | Ordered collection                      | `[1, 2, 3]`, `["hippo", "dog"]`|
| `dict`       | Dictionary (key–value pairs)            | `{"name": "Fiona", "age": 8}`  |
| `NoneType`   | Represents no value                     | `None`                         |

---

## 🧰 Converting Between Data Types

Sometimes you need to **convert** data to the correct type:

```python
int("5")         # from string to integer
float("3.14")    # from string to float
str(1500)        # from number to string
```

Use with caution: if the conversion doesn't make sense, Python will raise an error.

---

## 🧪 Checking and Comparing Types

```python
x = 3.14
if isinstance(x, float):
    print("x is a float")
```

---

## 🔍 Data Types in `pandas`

When working with tables (`DataFrame`):

```python
df.dtypes           # shows data type of each column
df['col'].astype(str)  # convert column to string
```

---

Understanding data types helps prevent bugs and makes your code clearer and more reliable!
