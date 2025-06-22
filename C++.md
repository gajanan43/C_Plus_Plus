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

Would you like me to explain another example like:

* taking input from user
* doing math (like addition)
* using `if` conditions

Let me know!

