# updated--cpp-math-class
# clsMath.h - Advanced Mathematical Utility Class for C++

## 🧮 Overview
`clsMath` is a powerful, ⚡lightweight, header-only C++ class that provides an extensive collection of mathematical utilities, number analysis, and helper functions for arithmetic, logic, and numeric conversions.

It’s designed to simplify common math operations such as checking for even/odd numbers, calculating square roots, random numbers, reversing digits, or even converting numbers into English text.

All functions are **static templates**, so you can use them without creating an object — just call them directly from the class.

---

## 🚀 Key Features

### ✅ General Math Operations
- `Sum`, `Subtract`, `Multiplicate`, `Divide`, `Mode2Num`
- `Square`, `Sqrt`, `Half`, `Opposite`, `Swap`
- `Calculate2Num` — performs arithmetic operations based on enum type.

### 🔍 Number Analysis
- `IsPositive`, `IsNegative`, `IsZero`
- `IsOdd`, `IsEven`, `IsPrime`, `IsPerfect`
- `IsPalindrome`, `IsFloat`, `IsLeapYear`
- `FractionPart`, `ReverseNum`, `SumDigits`

### 🧠 Number Conversion & Utilities
- `NumberToText` — converts numbers to readable English words.
- `RandomNumber` — generates a random integer within a given range.
- `Abs`, `Floor`, `Ceil`, `Round` — common rounding and absolute value utilities.

### ⚙️ Additional Helpers
- Enum `enOperatorType` supports:
  - Addition
  - Subtraction
  - Multiplication
  - Division
  - Modulus

All operations are implemented using **C++ templates**, meaning they work seamlessly with `int`, `float`, `double`, `long`, and other numeric types.

---

## 💡 Example Usage

```cpp
#include <iostream>
#include "clsMath.h"
using namespace std;

int main() {
    cout << "Is 2024 a leap year? " << (clsMath::IsLeapYear(2024) ? "Yes" : "No") << endl;
    cout << "Reverse of 1234: " << clsMath::ReverseNum(1234) << endl;
    cout << "Is 17 prime? " << (clsMath::IsPrime(17) ? "Yes" : "No") << endl;
    cout << "Sum of 12 and 8: " << clsMath::Sum(12, 8) << endl;
    cout << "Number to text (123): " << clsMath::NumberToText(123) << endl;
    cout << "Random number (1–10): " << clsMath::RandomNumber(1, 10) << endl;
    return 0;
}
```

---

## 🧪 Testing Guide

You can test individual functions by calling them from `main()` and comparing outputs manually.  
For automated testing, consider using Google Test or Catch2 with simple assertions:

```cpp
#include "clsMath.h"
#include <cassert>

int main()
 {
    assert(clsMath::IsEven(4) == true);
    assert(clsMath::IsOdd(5) == true);
    assert(clsMath::IsPrime(7) == true);
    assert(clsMath::ReverseNum(321) == 123);
    assert(clsMath::Sum(10, 20) == 30);
    cout << "All tests passed!" << endl;
}
```

Run your program:
```
g++ -std=c++17 test_clsMath.cpp -o test && ./test
```

---

## 🧾 Example Output

```
Is 2024 a leap year? Yes
Reverse of 1234: 4321
Is 17 prime? Yes
Sum of 12 and 8: 20
Number to text (123): One Hundred Twenty Three
Random number (1–10): 7
All tests passed!
```

---

## ⚡ Performance & Compatibility
- **Header-only:** No linking needed, just `#include "clsMath.h"`.
- **C++17 and newer** compatible.
- Works across Windows, Linux, and macOS.
- Lightweight, no external dependencies.

---

## 🧱 Structure
```
clsMath.h
└── Contains clsMath class with:
    ├── 40+ static template functions
    ├── enum enOperatorType
    └── Mathematical, logical, and number conversion utilities
```

---

## 🧰 Future Improvements
- Add trigonometric functions (sin, cos, tan).
- Add logarithmic and exponential functions.
- Add fraction simplification and GCD/LCM utilities.

---

## 📜 License
This project is open-source and free to use for educational or commercial purposes.

