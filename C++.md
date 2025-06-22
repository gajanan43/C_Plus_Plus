# Lec-01
##  1) What is a programming Language & why C++ ?
## What is a **Programming Language**?

A **programming language** is a way for **humans to communicate with computers**.

* It provides a **set of rules** (syntax) and **words** (keywords) to write instructions that a computer can **understand and execute**.
* These instructions tell the computer **what to do**, like calculations, decision making, repeating actions, etc.
* C++ is a general-purpose programming language created by Bjarne Stroustrup in 1979 as an extension of the C programming language. It supports both procedural and object-oriented programming (OOP).


### 🔹 Why **C++**?

C++ is one of the **most powerful and widely used** programming languages. Here's **why it's special**:

#### ✅ 1. **Performance & Speed**

* C++ is close to the hardware (low-level features), so it's **super fast** and used in **gaming, real-time systems, and operating systems**.

#### ✅ 2. **Object-Oriented Programming (OOP)**

* Supports concepts like **classes**, **inheritance**, and **polymorphism**, which help in **organizing and managing large codebases**.

#### ✅ 3. **Standard Template Library (STL)**

* Built-in libraries for **data structures (like vectors, sets, maps)** and **algorithms (like sort, search)** — saves development time.

#### ✅ 4. **Memory Control**

* C++ gives **fine control over memory** using **pointers** and **dynamic memory**, which is useful for system-level programming.

#### ✅ 5. **Foundation Language**

* Many modern languages (like Java, C#, and even parts of Python) are influenced by C++. Learning C++ helps you **understand how computers work internally**.


### 🔹 Where is C++ used?

| Field              | Example                                    |
| ------------------ | ------------------------------------------ |
| System Programming | Operating Systems like Windows/Linux parts |
| Game Development   | Game engines like Unreal Engine            |
| Competitive Coding | Because it's fast and has STL              |
| Embedded Systems   | Programming microcontrollers and hardware  |
| Financial Systems  | High-speed trading software                |

---
## 2) Installation of G++:
##  💻 🔹 For **Windows** (using MinGW)

### ✅ Step 1: Download MinGW

1. Go to the official site: [https://www.mingw-w64.org/](https://www.mingw-w64.org/)
2. Or directly: [MinGW-w64 builds (sourceforge)](https://sourceforge.net/projects/mingw-w64/)

### ✅ Step 2: Install MinGW

* Choose architecture: `x86_64`
* Threads: `posix`
* Exception: `seh`
* Install to a simple path like `C:\mingw-w64\`

### ✅ Step 3: Set Environment Variable

1. Press **Windows + S**, search for **Environment Variables**.
2. Click `Environment Variables > System variables > Path > Edit`.
3. Add:

   ```
   C:\mingw-w64\bin
   ```

   (Use the correct folder path where you installed MinGW.)

### ✅ Step 4: Verify Installation

Open **Command Prompt** and type:

```bash
g++ --version
```

You should see the version info like:

```
g++ (x86_64-posix-seh, built by ...) x.x.x
---

## ✅ How to Compile and Run C++ Code

Create a file `hello.cpp`:

```cpp
#include <iostream>
using namespace std;
int main() {
    cout << "Hello, World!";
    return 0;
}
```

### 🔹 Compile:

```bash
g++ hello.cpp -o hello
```

### 🔹 Run:

```bash
./hello   # On Windows use: hello.exe
```

---
---

# Lec-02
* 1979 -->Bjarne Stroustrup
*  fast Program, more control via system resources + memory management
*  High Performance
*  Updates:
     1) 2011 -->C++11
     2) 2014 -->C++14
     3) 2017 -->C++17

## Basic Structure of Program

### 🔷 Simple C++ Program

```cpp
#include <iostream>
using namespace std;

int main() {
    cout << "Hello, world!" << endl;
    return 0;
}
```

---

### 🔍 Line-by-line and word-by-word Explanation

---

#### 🔹 `#include <iostream>`

* `#include` → A **preprocessor directive**. It tells the compiler to **include** a file before starting the actual compilation.
* `<iostream>` → This is a **header file** that lets you use **input and output**, like `cin` and `cout`.

📌 Think of this line as:
👉 *"Hey compiler, include the file that lets me use `cout` to print and `cin` to take input."*

---

#### 🔹 `using namespace std;`

* `using` → Allows us to **avoid writing `std::`** before things like `cout`, `cin`, etc.
* `namespace` → A **container** for identifiers (names). `std` is the **standard namespace**.
* `std` → Stands for **standard**. It has useful stuff like `cout`, `cin`, `string`, etc.

📌 This line means:
👉 *"I will use standard names directly, no need to write `std::cout`, I can just write `cout`."*

---

#### 🔹 `int main() {`

* `int` → Return type of the function. It means this function will return an **integer value**.
* `main()` → The **starting point** of every C++ program. It’s where the program begins.
* `{` → Start of the **main function’s body** (all code inside this will run).

📌 It means:
👉 *"This is the main function. Start here!"*

---

#### 🔹 `cout << "Hello, world!" << endl;`

* `cout` → Stands for **"character output"**. It prints to the screen.
* `<<` → Called the **insertion operator**, it sends data to `cout`.
* `"Hello, world!"` → A **string literal**, the actual message being printed.
* `endl` → Ends the line and **moves to the next line**. Like pressing "Enter".
* `;` → Ends the statement.

📌 It means:
👉 *"Print ‘Hello, world!’ to the screen and go to a new line."*

---

#### 🔹 `return 0;`

* `return` → Sends a value **back to the system**.
* `0` → Means the program ended **successfully**.
* `;` → Ends the statement.

📌 It means:
👉 *"I'm done. Everything went okay."*

---

#### 🔹 `}`

* This closes the **main function**.

---

### ✅ Output

```
Hello, world!
```

---
---

# Lec-03

## Variables & Comments:
1)Variables:
👉 Variables are like boxes that store data (like numbers, words, etc.)

2)Comments:
👉 Comments are notes for the programmer. The compiler ignores them.

---
---

# Lec-04

## Variable Scope & Data Type:

Great! Let's learn about **Variable Scope** and **Data Types** in C++ with easy explanations and examples. 🧠✨

---

## 🔶 PART 1: **Variable Scope in C++**

### 📌 What is Scope?

**Scope** means **where a variable can be used (seen/accessible)** in your program.

---

### ✅ Types of Scope:

| Scope Type       | Meaning                                                                                  |
| ---------------- | ---------------------------------------------------------------------------------------- |
| **Global Scope** | Variable is declared **outside** all functions — can be used **anywhere**.               |
| **Local Scope**  | Variable is declared **inside** a function or block — used **only there**.               |
| **Block Scope**  | Inside `{}` brackets like in loops or `if` statements — used only **inside that block**. |

---

### 🔷 Example:

```cpp
#include <iostream>
using namespace std;

int globalVar = 100;  // 🌍 Global Scope

int main() {
    int localVar = 50;  // 📌 Local to main()

    if (true) {
        int blockVar = 20;  // 🔒 Block Scope
        cout << "Inside block: " << blockVar << endl;
    }

    // cout << blockVar << endl; ❌ Error! blockVar is not visible here

    cout << "Global: " << globalVar << endl;
    cout << "Local: " << localVar << endl;

    return 0;
}
```

---

### 🔍 Output:

```
Inside block: 20
Global: 100
Local: 50
```

---

## 🔶 PART 2: **Data Types in C++**

### 📌 What is a Data Type?

* A **data type** tells the compiler **what kind of data** a variable will store.
* Data types in C++ are categorized in three groups:
1) Built-in:
   * int
   * float
   * char
   * double
   * bool
2) User-defined :
   * struct
   * union
   * enum
3) Derived:
   * array
   * function
   * pointer


---
---

# Lec-05

## Basic input/Output:

* C++ comes with libraries which helps us in performing input/output.
* In C++ sequence of bytes corresponding to input and output are commonly known as streams.

1) Input Stream: Direction of flow of bytes takes place from input device(for ex Keyboard) to the main memory.

2) Output Stream: Direction of flow of bytes takes place from main memory to the output device (for example Display)

---
---

# Lec-06

## Header files & Operators:

### 📘 Header Files:

* **Pre-written code**
* Start with `#include`
* Examples: `<iostream>`, `<cmath>`, `<string>`, etc.

### 🔢 Operators:

* Perform operations like math, logic, comparison
* Common types: Arithmetic, Assignment, Comparison, Logical

---
---

# Lec-07

## Reference Variables & Typecasting:

## 🔷 1. **Reference Variables in C++**

A **reference variable** is another **name (alias)** for an existing variable.
It **refers to the same memory location**, not a copy.

---

### 🔷 Syntax:

```cpp
datatype &ref = original;
```

---

### ✅ Example:

```cpp
#include <iostream>
using namespace std;

int main() {
    int x = 10;
    int &y = x;  // y is a reference to x

    cout << "x = " << x << ", y = " << y << endl;

    y = 20;  // changing y will also change x
    cout << "x = " << x << ", y = " << y << endl;

    return 0;
}
```

---

### 🧾 Output:

```
x = 10, y = 10
x = 20, y = 20
```

### 🧠 Key Points:

* `&y` means `y` is a **reference** to `x`.
* Changing `y` also changes `x` (because they point to the **same memory**).

---

## 🔷 2. **Typecasting in C++**

### 📌 What is Typecasting?

**Typecasting** means **converting one data type into another**.

---

### 🔷 Two Types:

| Type         | Syntax                           | Example                    |
| ------------ | -------------------------------- | -------------------------- |
| **Implicit** | Automatic conversion by compiler | `int x = 5.7;` (becomes 5) |
| **Explicit** | Done manually by programmer      | `float(x)`, `(int)y`       |

---

### ✅ Example 1: Implicit Typecasting

```cpp
#include <iostream>
using namespace std;

int main() {
    float f = 5.7;
    int x = f; // float to int automatically (implicit)

    cout << "x = " << x << endl;  // Output: x = 5

    return 0;
}
```

---

### ✅ Example 2: Explicit Typecasting

```cpp
#include <iostream>
using namespace std;

int main() {
    int a = 10, b = 3;

    float result = (float)a / b; // casting a to float
    cout << "Result = " << result << endl;  // Output: 3.3333

    return 0;
}
```

---

### 🧠 Key Points:

| Cast Type  | What it does                            | Example               |
| ---------- | --------------------------------------- | --------------------- |
| `(int)`    | Converts to integer                     | `(int)3.9` → `3`      |
| `(float)`  | Converts to float                       | `(float)3/2` → `1.5`  |
| `(double)` | Converts to double (more precise float) | `(double)5/2` → `2.5` |

---

## ✅ Summary Table:

| Concept       | Meaning                            | Example        |
| ------------- | ---------------------------------- | -------------- |
| Reference Var | Another name for the same variable | `int &y = x;`  |
| Typecasting   | Converting one type to another     | `(float)a / b` |

---
---
