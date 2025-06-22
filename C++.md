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
