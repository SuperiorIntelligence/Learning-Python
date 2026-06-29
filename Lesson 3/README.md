# 🐍 Python Programming — Session 03
## Operators, Conditions & Strings

> **Making decisions in code** — this is where your programs stop being a simple list of instructions and start having a *brain*.

---

## 🗺️ What You'll Learn

By the end of this session, you'll be able to write programs that respond to different inputs, evaluate complex conditions, and work confidently with text. Here's the roadmap:

| # | Topic | The Big Idea |
|---|-------|-------------|
| 1 | ⚡ Arithmetic Operators | All math ops in Python, plus the ones you didn't know you needed |
| 2 | 🔗 Logical Operators | `and`, `or`, `not` — and why order matters |
| 3 | 🔀 if / elif / else | Teaching your program to make choices |
| 4 | 🪆 Nested Conditions | Decisions inside decisions |
| 5 | 🗃️ Variable Types (Deep Dive) | What `int`, `float`, `str`, and `bool` really are |
| 6 | 🧵 String Methods | The most useful built-in tools for working with text |

---

## ⚡ Part 1 — Arithmetic Operators

You already know `+`, `-`, `*`, `/`. This part fills in the rest:

- **Floor division `//`** — divides and rounds *down*, always. So `10 // 3 = 3`, and `-10 // 3 = -4` (not -3 — it rounds toward negative infinity).
- **Modulo `%`** — gives you the *remainder*. Classic use: `number % 2 == 0` tells you if a number is even.
- **Exponentiation `**`** — `2 ** 10 = 1024`. Bonus: `144 ** 0.5` gives you the square root.
- **Augmented assignment** — `score += 10` is just shorthand for `score = score + 10`.

You'll also nail down **operator precedence** — the rules that decide which operation runs first in a complex expression. The short version: `**` before `* / // %` before `+ -` before comparisons before `not` before `and` before `or`. When in doubt, use parentheses.

---

## 🔗 Part 2 — Logical Operators & Precedence

A review of `and`, `or`, `not` from Session 2, but this time with a focus on how they interact with arithmetic and comparison operators in a *single expression*:

```python
age >= 18 and score + 5 >= 60
```

Python evaluates this step by step: arithmetic first → comparisons next → logical last. Understanding this flow lets you write clean, bug-free conditions without needing extra parentheses everywhere.

---

## 🔀 Part 3 — if / elif / else

This is the heart of the session. You'll learn how to give your program multiple possible paths:

```python
if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 60:
    grade = "C"
else:
    grade = "F"
```

One important gotcha: **order matters**. Python stops at the *first* condition that is `True` and skips the rest. So you should always place your most specific (highest threshold) conditions first — a common beginner mistake is putting them in the wrong order and wondering why the logic breaks.

---

## 🪆 Part 4 — Nested Conditions

Sometimes a second check only makes sense *after* a first check passes. That's nesting:

```python
if age >= 18:
    if has_id:
        print("You may enter ✅")
    else:
        print("Please show your ID 🪪")
else:
    print("You are too young ❌")
```

You'll also learn when *not* to nest — if all conditions are independent, a flat `and` is almost always cleaner and easier to read.

---

## 🗃️ Part 5 — Variable Types, Deep Dive

You've used `int`, `float`, `str`, and `bool`. Now you'll understand their quirks:

- `int`: supports `1_000_000` notation for readability. Dividing two ints with `/` always returns a `float`.
- `float`: watch out for `0.1 + 0.2 ≠ 0.3` — floating-point precision is a real thing. Use `round()` when displaying results.
- `str`: single quotes, double quotes, or triple quotes — all valid. Strings support `+` for joining and `*` for repetition.
- `bool`: `True` and `False` are actually integers (`True == 1`, `False == 0`). An empty string `""` is *falsy*, which means you can use `if name:` instead of `if name != "":`.

---

## 🧵 Part 6 — String Methods

Strings come packed with built-in methods. You'll work through the most-used ones:

| Method | What it does |
|--------|-------------|
| `.upper()` / `.lower()` | Change case — great for case-insensitive comparisons |
| `.strip()` | Remove leading/trailing whitespace — always use this on user input |
| `.find(sub)` | Returns index of first match, or `-1` if not found |
| `.count(sub)` | How many times a substring appears |
| `.replace(a, b)` | Replace all occurrences of `a` with `b` |
| `.split(sep)` | Break a string into a list |
| `.startswith()` / `.endswith()` | Quick `True`/`False` checks |

You'll also cover **string slicing** — extracting any part of a string with `text[start:end:step]`, including tricks like `text[::-1]` to reverse a string.

---

## 🏋️ In-Class Exercises

Four hands-on exercises that use *only* what you've learned in Sessions 1–3:

1. **Smart Score Grader** — Take a student's name and score, validate the input, and print a grade with a personalized message.
2. **Operator Precedence Explorer** — Predict the output of expressions *before* running them, then verify your answers.
3. **Name Analyzer** — Take a full name and extract stats: case variants, character counts, first/last name split, vowel check.
4. **Trip Cost Calculator** — Calculate fuel cost for a road trip, split it per passenger, and classify the result as cheap / moderate / expensive.

---

## ✅ What You'll Have After This Session

- You can write programs that respond differently to different inputs
- You understand why expression order matters — and how to control it
- You can cleanly manipulate and analyze text using string methods
- You're ready for the next step: **loops** (`for` and `while`)

---

> 💡 **Note:** All examples and exercises in this session intentionally use only concepts from Sessions 1–3. Nothing from future sessions is introduced.
