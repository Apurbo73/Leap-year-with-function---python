Leap year with function-- python

Absolutely. Let's understand it **step by step**.

### The code

```python
def is_leap(year):
    if year % 400 == 0:
        return True
    elif year % 100 == 0:
        return False
    elif year % 4 == 0:
        return True
    else:
        return False


year = int(input("Enter a year: "))
print(is_leap(year))
```

### 1. Create the function

```python
def is_leap(year):
```

`def` is used to create a **function**.

Here, the function is named `is_leap` and it takes one value called `year`.

For example:

```python
is_leap(2024)
```

Here, `2024` is passed into `year`.

---

### 2. Check if the year is divisible by 400

```python
if year % 400 == 0:
    return True
```

`%` is the **modulus operator**. It gives us the remainder after division.

For example:

```python
2024 % 400
```

gives `24`, so 2024 is **not** divisible by 400.

But:

```python
2000 % 400
```

gives `0`.

So 2000 is divisible by 400, and we return:

```python
True
```

---

### 3. Check if the year is divisible by 100

```python
elif year % 100 == 0:
    return False
```

`elif` means **"else if"**.

This checks years such as `1900`.

```python
1900 % 100 == 0
```

This is `True`, so we return:

```python
False
```

Why? Because years divisible by 100 are normally **not** leap years.

---

### 4. Check if the year is divisible by 4

```python
elif year % 4 == 0:
    return True
```

If the year isn't divisible by 400 or 100, we check whether it's divisible by 4.

For example:

```python
2024 % 4 == 0
```

This is `True`, so:

```python
return True
```

Therefore, 2024 is a leap year.

---

### 5. If none of the conditions are true

```python
else:
    return False
```

If the year isn't divisible by 400, 100, or 4, it's not a leap year.

For example:

```python
1990
```

`1990 % 4` is not `0`, so the function returns:

```python
False
```

---

### 6. Take input from the user

```python
year = int(input("Enter a year: "))
```

`input()` gets information from the user.

For example, the user enters:

```text
2024
```

But `input()` normally gives us a **string**.

So:

```python
int()
```

converts `"2024"` into the integer `2024`.

Then we store it in the variable:

```python
year
```

---

### 7. Call the function and print the result

```python
print(is_leap(year))
```

Suppose the user entered:

```text
2024
```

Then Python effectively does:

```python
is_leap(2024)
```

The function checks the rules and returns:

```python
True
```

Then `print()` displays:

```text
True
```

### The logic in simple terms

Think of it like this:

```text
Is year divisible by 400?
       ↓
      YES → True
       ↓ NO
Is year divisible by 100?
       ↓
      YES → False
       ↓ NO
Is year divisible by 4?
       ↓
      YES → True
       ↓ NO
     False
```

So:

| Year | Result  | Reason                        |
| ---- | ------- | ----------------------------- |
| 2024 | `True`  | Divisible by 4                |
| 1900 | `False` | Divisible by 100, but not 400 |
| 2000 | `True`  | Divisible by 400              |
| 1990 | `False` | Not divisible by 4            |
