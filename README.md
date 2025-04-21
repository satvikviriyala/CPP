# C++
## Course Overview

**Course Title:** Comprehensive Course On C++
**Instructor:** Pankaj Sharma
**Platform:** Unacademy
**Target Audience:** GATE - CSIT, DSAI & Interview Preparation
**Language:** Hinglish (Content presented here in English)

**Course Description (from slides):** This course covers C++, a leading programming language used in game development, virtual reality, real-time simulation, and high-frequency trading, emphasizing efficiency and speed. The course includes concepts, problem-solving, and potentially covers the Standard Template Library (STL).

---

### Lecture 1: Introduction - Part I (May 10, 2024)

**Topics Covered:**
*   Course structure and schedule overview.
*   History of C and C++.
*   Procedural vs. Object-Oriented Programming (OOP).
*   Introduction to Objects and Classes.

**Detailed Notes:**

1.  **Course Logistics:**
    *   The course seems structured over several weeks (approx. 10 weeks mentioned).
    *   Classes might run Monday to Friday or potentially daily.
    *   Different types of sessions mentioned: Plus classes, Special classes, YouTube (YT) sessions.
    *   Focus on C++ fundamentals, potentially leading into Data Structures and Algorithms (DSA) and problem-solving relevant for GATE and interviews.

2.  **History & Evolution:**
    *   **C Language:** Developed in 1972 by Dennis Ritchie at AT&T Bell Labs. Primarily used for developing the UNIX OS. Known for being efficient, powerful, and popular ("King" of programming languages for system tasks). It's a *procedural* language.
    *   **Object-Oriented Concepts:** Emerged with languages like SIMULA 1 and SIMULA 67 (considered the first OOPLs), but they weren't widely adopted or seen as efficient/powerful as C for many tasks.
    *   **Limitations of C for Large Projects:** Procedural programming (like in C) becomes difficult to manage for large/complex software due to:
        *   Lack of data security/hiding.
        *   Poor code reusability.
        *   Maintenance challenges.
        *   Inter-relatedness of functions making changes risky.
    *   **C++ Origin:** Developed by Bjarne Stroustrup at AT&T Bell Labs, starting around 1979, initially called "C with Classes". Officially named C++ in 1983.
    *   **Goal of C++:** To combine the efficiency and low-level capabilities of C with the organizational and design benefits of OOP (inspired by SIMULA).
    *   **"C with Classes":** C++ is fundamentally a superset of C, meaning most valid C code is also valid C++ code. It adds Object-Oriented features on top of C.
    *   **C++ Standards:** C++ has evolved with various standard updates (C++98, C++03, C++11, C++14, C++17, C++20, etc.).

3.  **Programming Paradigms:**
    *   **Procedural Oriented Programming (POP):** Focuses on functions (procedures) and the sequence of steps to solve a problem. Data and functions are often separate. Suitable for small to medium projects. (Example: C).
    *   **Object-Oriented Programming (OOP):** Focuses on "objects" which bundle data (attributes/properties) and methods (functions/behaviors) that operate on that data. Emphasizes concepts like encapsulation, abstraction, inheritance, and polymorphism. Better suited for large, complex projects, promoting modularity, reusability, and maintainability. (Examples: C++, Java, Python).
    *   **C++ as a Hybrid:** C++ supports both procedural and object-oriented programming paradigms.

4.  **Objects and Classes (Introduction):**
    *   **Real-world Analogy:** Think of entities like "Teacher", "Student", "Patient", "Bank Account".
    *   **Properties/Attributes:** Characteristics of an entity (e.g., Teacher: Name, Age, Qualification, Experience; Patient: Name, Age, Blood Group, BP). These correspond to *data members* or *member variables* in a class.
    *   **Methods/Actions/Behaviors:** Things an entity can do or have done to it (e.g., Teacher: Teach(); Patient: Diagnose(); Bank Account: Deposit(), Withdraw()). These correspond to *member functions* in a class.
    *   **Class:** A blueprint, template, or design for creating objects. It defines the common properties and methods for a type of object. (e.g., The design for a "Hero Honda xyz" bike).
    *   **Object:** An instance of a class. A concrete entity created based on the class blueprint. Objects have state (values of their properties) and behavior (defined by class methods). (e.g., A specific "Hero Honda xyz" bike produced from the design). Many objects can be created from a single class.

**Code Snippets:** (Illustrative C vs C++ basic program structure)

*   **C Example (Procedural):**
    ```c
    #include <stdio.h> // Header for standard input/output functions

    int main() {
        int n, ans;

        printf("Enter a number: "); // Output function
        scanf("%d", &n); // Input function

        ans = n * n; // Calculation

        printf("The square of %d is %d\n", n, ans); // Output result

        return 0;
    }
    ```
*   **C++ Equivalent (Showing OOP elements later):**
    ```cpp
    #include <iostream> // Header for C++ input/output stream objects

    // using namespace std; // Tells the compiler to use names from the standard namespace (like cout, cin)

    int main() {
        int n, ans;

        std::cout << "Enter a number: "; // Output object (insertion operator <<)
        std::cin >> n; // Input object (extraction operator >>)

        ans = n * n; // Calculation

        // Chained output using insertion operator
        std::cout << "The square of " << n << " is " << ans << std::endl; // endl inserts newline and flushes buffer

        // getch(); // Might be used in some environments (like Turbo C++) to pause console, requires <conio.h> - generally not standard C++
        return 0;
    }
    ```
    *Note: The slide mentioned potential errors if `<conio.h>` isn't included or if `using namespace std;` is omitted. Standard C++ prefers using `std::` prefix.*

---

### Lecture 2: Introduction - Part II (May 13, 2024)

**Topics Covered:**
*   Object-Oriented Concepts: Properties and Methods.
*   C vs C++: `printf`/`scanf` vs `cout`/`cin`.
*   Operators: Insertion (`<<`) and Extraction (`>>`).

**Detailed Notes:**

1.  **Objects & Classes (Continued):**
    *   Focus on identifying relevant properties and methods for a given entity (e.g., Teacher, Patient, Bank Account).
    *   Properties represent the *state* of an object.
    *   Methods represent the *behavior* or actions related to the object.
    *   In C++, objects encapsulate both state (variables) and behavior (functions).
    *   Example: `Ram.playing()` - `Ram` is the object, `playing()` is the method (behavior). `Ram.height` - `Ram` is the object, `height` is the property (state).

2.  **C vs C++ Input/Output:**
    *   **C:** Uses functions like `printf()` (output) and `scanf()` (input). These are part of the standard C library (`stdio.h`). They are procedural. `printf` uses format specifiers (`%d`, `%f`, `%s`, etc.). `scanf` requires addresses (`&variable`).
    *   **C++:** Uses stream objects `cout` (console output) and `cin` (console input) defined in `<iostream>`. These are objects of predefined classes (`ostream`, `istream`).
    *   **Insertion Operator (`<<`):** Used with `cout` to "insert" data into the output stream. It's an operator overloaded for various data types. `cout << "Welcome";`
    *   **Extraction Operator (`>>`):** Used with `cin` to "extract" data from the input stream into a variable. It's overloaded for various data types. `cin >> n;`
    *   **Advantages of `cout`/`cin`:** Type-safe (no format specifiers needed), extensible (can be overloaded for user-defined types), often more convenient syntax (chaining).
    *   **Namespace `std`:** `cout`, `cin`, `endl`, etc., are part of the standard namespace (`std`). Need to use `std::cout` or include `using namespace std;`.
    *   **Header Files:** C++ typically uses `<iostream>` for I/O. C headers like `<stdio.h>` can also be used (often as `<cstdio>` in C++).

3.  **Operators as Part of Class Interface:**
    *   In OOP, operators like `<<` and `>>` can be thought of as actions performed *by* or *on* objects. `cout << data` means the `cout` object is performing the insertion action with `data`. `cin >> variable` means the `cin` object is performing extraction into `variable`. This relates to operator overloading.

**Code Snippets:**

*   **Comparing Output:**
    ```c
    // C
    printf("The square of %d is %d\n", n, ans);

    // C++
    std::cout << "The square of " << n << " is " << ans << std::endl;
    ```
*   **Comparing Input:**
    ```c
    // C (single int)
    scanf("%d", &n);
    // C (two ints)
    scanf("%d %d", &a, &b);

    // C++ (single int)
    std::cin >> n;
    // C++ (two ints - chaining)
    std::cin >> a >> b;
    ```

---

### Lecture 3: Inline Function (May 14, 2024)

**Topics Covered:**
*   Function call overhead.
*   Inline functions: concept, syntax, purpose.
*   Compiler's role.
*   Advantages and disadvantages.

**Detailed Notes:**

1.  **Functions: Advantages & Disadvantages:**
    *   **Advantages:** Code reusability, easier readability/modification, memory saving (code defined once, called multiple times).
    *   **Disadvantage:** Function call overhead. Each time a function is called:
        *   Current state needs to be saved.
        *   Control needs to be transferred to the function's code.
        *   Arguments may need to be pushed onto the stack.
        *   Return value handling.
        *   Control transfer back.
        *   Restoring state.
        *   This takes a small amount of execution time.

2.  **Inline Functions:**
    *   **Concept:** A mechanism to reduce function call overhead, primarily for small, frequently called functions.
    *   **Mechanism:** Instead of transferring control, the compiler *replaces* the function call site with the actual code (body) of the function.
    *   **Syntax:** Use the `inline` keyword before the function's return type in its definition.
        ```cpp
        inline int square(int a) {
            return a * a;
        }
        ```
    *   **Request, Not Command:** `inline` is a *request* or suggestion to the compiler. The compiler may choose to ignore it based on certain conditions or its own optimization strategies.
    *   **When Compiler Might Ignore `inline`:**
        *   Function is too large.
        *   Function contains loops (e.g., `for`, `while`).
        *   Function contains `static` variables.
        *   Function is recursive.
        *   Function contains `switch` or `goto`.
        *   Address of the function is taken.

3.  **Trade-offs:**
    *   **Advantage:** Can lead to faster execution by eliminating call overhead.
    *   **Disadvantage:** Can increase the size of the compiled executable (code bloat) if the function body is large or called very many times, potentially leading to *slower* execution due to increased cache misses.

4.  **Programmer vs. Compiler:**
    *   The programmer *requests* inlining.
    *   The compiler *decides* whether to actually inline the function based on its analysis and optimization settings.

**Code Snippet:**

```cpp
#include <iostream>

// Requesting the compiler to inline this function
inline int square(int a) {
    // Simple function, good candidate for inlining
    return a * a;
}

int main() {
    int n, ans;
    std::cout << "Enter a number: ";
    std::cin >> n;

    // At compile time, this call might be replaced by: ans = n * n;
    ans = square(n);

    std::cout << "The square is " << ans << std::endl;
    return 0;
}
```

---

### Lecture 4: Default Arguments (May 15, 2024)

**Topics Covered:**
*   Concept of default arguments.
*   Syntax and rules.
*   Use cases.

**Detailed Notes:**

1.  **Problem:** Sometimes a function requires arguments, but in many common cases, those arguments might have typical or default values. Requiring the caller to always provide them can be tedious.
    *   Example: An `Add` function taking 3 arguments. What if the caller often only wants to add 2 numbers (assuming the third is 0)?

2.  **Default Arguments:**
    *   **Concept:** Allows assigning default values to function parameters in the function *declaration* (prototype) or *definition*. If a call omits an argument for which a default exists, the compiler automatically uses the default value.
    *   **Syntax:**
        ```cpp
        // In declaration (prototype) - Preferred location
        int Add(int a, int b, int c = 0);

        // Or in definition (if no separate declaration)
        // int Add(int a, int b, int c = 0) { ... }
        ```
    *   **Rule 1: Right-Aligned:** Default arguments *must* be the trailing (rightmost) parameters. You cannot have a default parameter followed by a non-default parameter.
        ```cpp
        // VALID:
        int func(int a, int b = 10, int c = 20);
        // INVALID:
        // int func(int a = 5, int b, int c = 20); // Error!
        // int func(int a, int b = 10, int c);     // Error!
        ```
    *   **Rule 2: Declaration or Definition:** Defaults should be specified in the function declaration (prototype) if one exists and is visible to the caller. If specified in both, they must match. If only a definition exists, specify them there. It's generally best practice to put them in the declaration (often in a header file).

3.  **Calling Functions with Default Arguments:**
    *   When calling, arguments are matched from left to right.
    *   You can omit trailing arguments for which defaults exist.
    *   ```cpp
        int Add(int a, int b = 0, int c = 0);
        // ...
        Add(10, 20, 30); // a=10, b=20, c=30
        Add(10, 20);     // a=10, b=20, c=0 (default used)
        Add(10);         // a=10, b=0,  c=0 (defaults used)
        // Add();        // Error! 'a' has no default
        ```

**Code Snippet:**

```cpp
#include <iostream>

// Function declaration with default arguments
int Add(int a, int b, int c = 0, int d = 0); // c and d have default values

int main() {
    std::cout << "Adding 2 numbers (10, 20): " << Add(10, 20) << std::endl; // Uses defaults for c, d
    std::cout << "Adding 3 numbers (10, 20, 30): " << Add(10, 20, 30) << std::endl; // Uses default for d
    std::cout << "Adding 4 numbers (10, 20, 30, 40): " << Add(10, 20, 30, 40) << std::endl; // No defaults used

    return 0;
}

// Function definition
int Add(int a, int b, int c, int d) {
    return a + b + c + d;
}
```

---

### Lecture 5: Reference Variable (May 16, 2024)

**Topics Covered:**
*   Review Call by Value, Call by Address (Pointers).
*   Introduction to Reference Variables in C++.
*   Syntax, properties, and initialization.
*   Use in Call by Reference.
*   Comparison with pointers.

**Detailed Notes:**

1.  **Parameter Passing in C:**
    *   **Call by Value:** A copy of the actual argument's value is passed to the function's formal parameter. Changes to the formal parameter inside the function *do not* affect the original actual argument. (Default mechanism for simple types).
    *   **Call by Address (using Pointers):** The address of the actual argument is passed. The formal parameter is a pointer. Changes made by dereferencing the pointer inside the function *do* affect the original actual argument.

2.  **C++ Parameter Passing:** Supports Call by Value, Call by Address, and adds **Call by Reference**.

3.  **Reference Variables:**
    *   **Concept:** A reference is an *alias* or an alternative name for an *already existing* variable. It doesn't create a new variable in memory; it just provides another way to access the original variable's memory location.
    *   **Syntax:** `dataType& referenceName = existingVariable;`
        ```cpp
        int x = 20;
        int& y = x; // y is now a reference (alias) for x.
        ```
    *   **Key Properties:**
        1.  **Must be Initialized:** A reference must be initialized when it is declared, and it must be initialized with an existing variable. `int& ref; // Error!` `int& ref = 10; // Error (usually, unless const ref)`
        2.  **Cannot be Re-seated:** Once initialized to refer to a variable, it cannot be changed to refer to a different variable later. `int z = 30; y = z; // This assigns the *value* of z (30) to x (via y), it does NOT make y refer to z.`
        3.  **Cannot be NULL:** References must refer to a valid memory location.
        4.  **No Separate Storage (Typically):** References usually don't occupy their own memory storage; they directly use the storage of the variable they refer to. (Implementation detail, but conceptually true).
        5.  **Initializer Type:** The initializer must generally be an l-value (something with an address) of the same type (or implicitly convertible). `int& ref = x + 1; // Error!` `double d = 9.8; int& ref = d; // Error!`

4.  **Call by Reference:**
    *   Uses reference variables as formal parameters in a function.
    *   Syntax: `void func(int& param) { ... }`
    *   Mechanism: When called (`func(myVar);`), the formal parameter (`param`) becomes an alias for the actual argument (`myVar`).
    *   Effect: Changes made to the reference parameter inside the function *directly affect* the original argument passed during the call.
    *   Advantage over pointers: Safer (cannot be NULL, cannot be re-seated accidentally) and often cleaner syntax (no need for `*` or `&` during access inside the function or during the call).

5.  **References vs. Pointers:**
    *   **Initialization:** References *must* be initialized; pointers *can* be uninitialized or NULL.
    *   **Re-seating:** References *cannot* be changed to refer elsewhere; pointers *can* be made to point to different locations.
    *   **NULL:** References *cannot* be NULL; pointers *can* be NULL.
    *   **Syntax:** References use `&` in declaration, access like normal variables; Pointers use `*` in declaration, require `*` for dereferencing, `->` for member access.
    *   **Use Case:** References are often preferred for function parameters (Call by Reference) and return types when aliasing is needed and NULL is not a valid state. Pointers are necessary when NULL is possible, re-seating is needed, or for pointer arithmetic (e.g., iterating through C-style arrays).

**Code Snippet:**

```cpp
#include <iostream>

// Function demonstrating Call by Reference
void modifyValue(int& ref) {
    std::cout << "Inside modifyValue, received value: " << ref << std::endl;
    ref = ref + 100; // Modifies the original variable
    std::cout << "Inside modifyValue, changed value to: " << ref << std::endl;
}

int main() {
    int x = 10;
    int& y = x; // y is an alias for x

    std::cout << "x = " << x << ", y = " << y << std::endl; // Output: 10, 10

    y = 25; // Modifying y also modifies x
    std::cout << "After y = 25:" << std::endl;
    std::cout << "x = " << x << ", y = " << y << std::endl; // Output: 25, 25

    std::cout << "Calling modifyValue with x..." << std::endl;
    modifyValue(x); // Pass x to the function expecting a reference
    std::cout << "After modifyValue:" << std::endl;
    std::cout << "x = " << x << ", y = " << y << std::endl; // Output: 125, 125

    // int& z; // Error: References must be initialized
    // int& w = 50; // Error: Initializer must be an l-value (variable)

    return 0;
}
```

---

### Lecture 6 & 7: Function Overloading - Part I & II (May 17 & 20, 2024)

**Topics Covered:**
*   Concept and purpose of function overloading.
*   Rules for overloading (signature differences).
*   Return type irrelevance.
*   Overload resolution process (Exact Match, Promotion, Conversion).
*   Ambiguity errors.

**Detailed Notes:**

1.  **Concept:** Function overloading allows defining multiple functions within the same scope that share the *same name* but have different *parameter lists* (signatures).
2.  **Purpose:** To use a single, intuitive function name for operations that are conceptually similar but work on different types or numbers of arguments. Improves code readability and usability.
    *   Example: `FindMax` for two integers vs. three integers. `Area` for a rectangle (length, width) vs. a square (side).
3.  **Rules for Overloading:**
    *   Functions must have the same name.
    *   Functions must be in the same scope.
    *   Functions must differ in their *parameter list* (signature) in at least one of the following ways:
        *   **Number of parameters:** `int Add(int a, int b)` vs `int Add(int a, int b, int c)`
        *   **Type of parameters:** `int Add(int a, int b)` vs `double Add(double a, double b)`
        *   **Sequence of parameter types:** `void func(int a, double b)` vs `void func(double a, int b)`
    *   **Return Type is NOT Considered:** You cannot overload functions based *only* on a different return type if their name and parameter lists are identical.
        ```cpp
        // INVALID Overloading:
        // int Add(int a, int b);
        // double Add(int a, int b); // Error! Same signature.
        ```

4.  **Function Signature:** The combination of the function name and its parameter list (number, types, and order of parameters). The signature must be unique for overloaded functions within the same scope.

5.  **Overload Resolution:** The process by which the compiler determines which specific overloaded function to call based on the arguments provided in the function call. This happens at compile time. The compiler tries to find the "best match" using the following sequence:
    1.  **Exact Match:** Find a function whose parameter types exactly match the argument types (after trivial conversions like array-to-pointer or function-to-pointer, and adding/removing `const`).
    2.  **Match with Promotion:** If no exact match, look for a match achievable through *integral promotions* (e.g., `char`, `short` promoted to `int`; `float` promoted to `double`).
    3.  **Match with Standard Conversion:** If still no match, look for a match achievable through *standard conversions* (e.g., `int` to `double`, `double` to `int`, numeric to `bool`, pointer conversions).
    4.  **Match with User-Defined Conversion:** (More advanced) Look for matches using user-defined conversion operators or converting constructors.
    5.  **Match with Ellipsis (`...`):** Match a function taking variable arguments.

6.  **Ambiguity:** If the compiler finds *more than one* equally good match at the best level found (e.g., two different standard conversions are possible, but no promotions or exact matches), it results in an *ambiguity error* during compilation. The programmer must resolve the ambiguity, perhaps by explicitly casting the arguments or defining a more specific overload.

**Code Snippet:**

```cpp
#include <iostream>
#include <string>

// Overloaded functions for Add
int Add(int a, int b) {
    std::cout << "-> Called Add(int, int)" << std::endl;
    return a + b;
}

double Add(double a, double b) {
    std::cout << "-> Called Add(double, double)" << std::endl;
    return a + b;
}

int Add(int a, int b, int c) {
    std::cout << "-> Called Add(int, int, int)" << std::endl;
    return a + b + c;
}

// Example for overload resolution steps
void printType(int x) {
    std::cout << "-> Called printType(int): " << x << std::endl;
}

void printType(double x) {
    std::cout << "-> Called printType(double): " << x << std::endl;
}

// void printType(float x) { // Adding this might cause ambiguity with char -> int vs char -> float -> double
//     std::cout << "-> Called printType(float): " << x << std::endl;
// }


int main() {
    // Basic overloading
    std::cout << "Add(5, 6) = " << Add(5, 6) << std::endl;
    std::cout << "Add(3.2, 4.5) = " << Add(3.2, 4.5) << std::endl;
    std::cout << "Add(1, 2, 3) = " << Add(1, 2, 3) << std::endl;

    std::cout << "\nOverload Resolution Examples:" << std::endl;
    int i = 10;
    char c = 'A'; // ASCII value is 65
    float f = 5.5f;

    printType(i); // Exact match with printType(int)
    printType(c); // No exact match. Promotion: char -> int. Calls printType(int)
    printType(f); // No exact match. Promotion: float -> double. Calls printType(double)

    // Ambiguity Example (if printType(float) was also defined)
    // printType(c); // Might be ambiguous: char->int vs char->float? Compiler dependent, often promotes to int.

    // Ambiguity Example 2
    // void ambig(long l);
    // void ambig(double d);
    // ambig(10); // Error! Ambiguous: int -> long vs int -> double

    return 0;
}
```

---

### Lecture 8, 9, 10: Structure and Class - Part I, II, III (May 21, 22, 23, 2024)

**Topics Covered:**
*   Structures in C vs C++.
*   Classes: definition, objects, members.
*   Access Specifiers: `public`, `private`, `protected`.
*   Encapsulation, Data Hiding, Abstraction.
*   Static members (variables and functions).

**Detailed Notes:**

1.  **Structures (Recap & C++ Enhancements):**
    *   **C `struct`:** Groups related data items (members). Members are `public` by default (no concept of access specifiers). Cannot contain member functions directly. `struct` keyword is mandatory when declaring variables (`struct Student s;`). No static members allowed.
    *   **C++ `struct`:** Can contain both data members and member functions. Members are `public` by default. Supports access specifiers (`private`, `protected`). `struct` keyword is optional when declaring variables (`Student s;`). Can have static members. Essentially like a class where the default access is `public`.

2.  **Classes:**
    *   **Concept:** The fundamental building block of OOP in C++. A user-defined data type that acts as a blueprint for creating objects.
    *   **Syntax:**
        ```cpp
        class ClassName {
        private: // Optional: default for class
            // Private members (data/functions)
        protected: // Optional
            // Protected members (data/functions)
        public: // Optional
            // Public members (data/functions) - Interface
        }; // Semicolon is mandatory
        ```
    *   **Members:** Variables (data members) and functions (member functions) declared inside a class.
    *   **Objects:** Instances of a class. Created like variables: `ClassName objectName;`.

3.  **Access Specifiers:** Control the visibility and accessibility of class members.
    *   **`public`:** Members are accessible from anywhere (inside the class, by derived classes, and outside the class through an object). Defines the class's public interface.
    *   **`private`:** Members are accessible *only* from within the class itself (by its own member functions or friend functions). Not accessible by derived classes or outside the class. (Default for `class`). Enforces data hiding.
    *   **`protected`:** Members are accessible from within the class itself and by its derived classes. Not accessible from outside the class through an object. Used in inheritance.

4.  **OOP Principles:**
    *   **Encapsulation:** Bundling data and the methods that operate on that data within a single unit (the class). C++ achieves this through classes and structs.
    *   **Data Hiding:** Restricting direct access to the internal data members of an object. Achieved using `private` (and `protected`) access specifiers. Protects the object's internal state from accidental or malicious modification.
    *   **Abstraction:** Hiding the complex implementation details and exposing only the necessary functionalities (the public interface) to the outside world. Users interact with the object through its public methods without needing to know how they are implemented internally.

5.  **Static Members:** Members that belong to the class itself, rather than to individual objects.
    *   **Static Member Variables:**
        *   Shared by all objects of the class. Only one copy exists.
        *   Declared inside the class with the `static` keyword.
        *   Must be *defined* (and optionally initialized) *outside* the class definition, usually in the .cpp file. Syntax: `dataType ClassName::staticVarName = initialValue;`
        *   Can be accessed using the class name and scope resolution operator (`ClassName::staticVarName`) even if no objects exist, or via an object (`objectName.staticVarName` - less common/clear).
        *   Useful for data common to all instances (e.g., a counter for the number of objects created).
        *   Memory is allocated only once.
    *   **Static Member Functions:**
        *   Declared inside the class with the `static` keyword.
        *   Belong to the class, not a specific object.
        *   Can be called using the class name (`ClassName::staticFuncName()`) or via an object (`objectName.staticFuncName()`).
        *   Do *not* receive an implicit `this` pointer because they aren't associated with a specific object.
        *   Can *only* directly access other *static* members (variables or functions) of the class. They cannot directly access non-static (instance) members.
        *   Useful for utility functions related to the class but not dependent on a specific object's state.

**Code Snippet:**

```cpp
#include <iostream>
#include <string>

class Product {
private: // Data hiding: accessible only within the class
    std::string name;
    double price;
    static int objectCount; // Static variable declaration (shared by all objects)

public: // Public interface: accessible from outside
    // Constructor to initialize product
    Product(std::string n = "Default", double p = 0.0) : name(n), price(p) {
        std::cout << "Product '" << name << "' created." << std::endl;
        objectCount++; // Increment shared count when an object is created
    }

    // Destructor
    ~Product() {
        std::cout << "Product '" << name << "' destroyed." << std::endl;
        objectCount--; // Decrement shared count
    }

    // Public member function to display product details (accesses private data)
    void display() {
        std::cout << "Name: " << name << ", Price: $" << price << std::endl;
    }

    // Public static member function (can be called without an object)
    static int getObjectCount() {
        // Cannot access 'name' or 'price' directly here (they are non-static)
        // Can access static members like objectCount
        return objectCount;
    }

    // Example function trying to access private static member (would need to be static or friend)
    // void accessStaticDirectly() { std::cout << objectCount; } // OK

}; // Don't forget the semicolon!

// Static member variable definition and initialization (outside the class)
int Product::objectCount = 0;

int main() {
    std::cout << "Initial object count: " << Product::getObjectCount() << std::endl; // Access static func via class

    Product p1("Laptop", 1200.50);
    Product p2("Mouse", 25.00);
    Product p3; // Uses default constructor values

    std::cout << "\nCurrent object count: " << Product::getObjectCount() << std::endl;
    // std::cout << p1.objectCount << std::endl; // Can also access via object, but less clear

    p1.display();
    p2.display();
    p3.display();

    // p1.price = 1000; // Error! price is private
    // std::cout << p1.name; // Error! name is private

    std::cout << "\nExiting main..." << std::endl;
    // Destructors will be called automatically for p1, p2, p3 here
    // Final object count will be printed by destructors implicitly

    return 0;
}
```

---

### Lecture 11 & 12: Constructor & Destructor - Part I & II (May 27 & 28, 2024)

**Topics Covered:**
*   Constructors: purpose, rules, types (Default, Parameterized, Copy).
*   Constructor overloading.
*   Compiler-generated constructors.
*   Destructors: purpose, rules, automatic invocation.

**Detailed Notes:**

1.  **Constructor:**
    *   **Purpose:** To initialize the state (data members) of an object when it is created. Ensures objects start in a valid state.
    *   **Characteristics:**
        *   Special member function.
        *   Same name as the class.
        *   No return type (not even `void`).
        *   Automatically invoked when an object is instantiated.
        *   Can be overloaded.
        *   Is an instance member function (cannot be `static`).
        *   Handles the initialization problem (prevents objects having garbage values initially).

2.  **Types of Constructors:**
    *   **Default Constructor:** Takes no arguments.
        ```cpp
        class Complex {
        public:
            Complex() { // Default Constructor
                real = 0; img = 0;
                std::cout << "Default Ctor called" << std::endl;
            }
        private:
            int real, img;
        };
        Complex c1; // Invokes default constructor
        ```
    *   **Parameterized Constructor:** Takes arguments to initialize data members.
        ```cpp
        class Complex {
        public:
            Complex(int r, int i) { // Parameterized Constructor
                real = r; img = i;
                std::cout << "Param Ctor called" << std::endl;
            }
        private:
            int real, img;
        };
        Complex c2(10, 20); // Invokes parameterized constructor
        ```
    *   **Copy Constructor:** Initializes an object using another object of the same class. Takes a single argument: a reference (usually `const`) to an object of the same class.
        ```cpp
        class Complex {
        public:
            // User-defined Copy Constructor
            Complex(const Complex& other) {
                real = other.real;
                img = other.img;
                std::cout << "Copy Ctor called" << std::endl;
            }
             // Need other constructors too...
            Complex(int r=0, int i=0) : real(r), img(i) {} // Default/Param combined
        private:
            int real, img;
        };
        Complex c3(3, 4);
        Complex c4 = c3; // Invokes copy constructor (Initialization)
        Complex c5(c3);  // Invokes copy constructor (Initialization)
        // Note: Complex c6; c6 = c3; // This uses the assignment operator, NOT copy ctor.
        ```
        *   **Why `const` reference?** `const` prevents the copy constructor from modifying the source object. Reference (`&`) avoids making a copy of the argument, which would require calling the copy constructor again, leading to infinite recursion.

3.  **Compiler-Generated (Implicit) Constructors:**
    *   **Default Constructor:** The compiler provides a public, empty default constructor *only if* the programmer does *not* define *any* constructors for the class. If you define *any* constructor (e.g., parameterized), the compiler will *not* generate the default one.
    *   **Copy Constructor:** The compiler provides a public copy constructor *if* the programmer does not define one. This implicit copy constructor performs a *member-wise copy* (shallow copy) of the data members. This is often sufficient, but can be problematic if the class manages dynamic memory (requires a deep copy).

4.  **Destructor:**
    *   **Purpose:** To clean up resources allocated by an object before it is destroyed (goes out of scope or is explicitly deleted). Common use: deallocating dynamic memory allocated in the constructor.
    *   **Characteristics:**
        *   Special member function.
        *   Same name as the class, preceded by a tilde (`~`). Example: `~Complex()`.
        *   No return type.
        *   Takes no arguments (cannot be overloaded).
        *   Automatically invoked when an object's lifetime ends.
        *   Is an instance member function (cannot be `static`).
    *   **Compiler-Generated Destructor:** If the programmer doesn't provide one, the compiler generates a public, empty destructor.

**Code Snippet (Illustrating Constructors & Destructor):**

```cpp
#include <iostream>

class Example {
private:
    int id;
    int* data; // Pointer for dynamic allocation

public:
    // Default Constructor
    Example() : id(0), data(nullptr) { // Use initializer list
        std::cout << "Default Constructor called (ID: " << id << ")" << std::endl;
    }

    // Parameterized Constructor
    Example(int i, int val) : id(i) { // Use initializer list
        data = new int(val); // Allocate memory
        std::cout << "Parameterized Constructor called (ID: " << id << ", Data: " << *data << ")" << std::endl;
    }

    // Copy Constructor (Deep Copy needed due to raw pointer 'data')
    Example(const Example& other) : id(other.id) {
        if (other.data) {
            data = new int(*other.data); // Allocate new memory and copy value
            std::cout << "Copy Constructor called (ID: " << id << ", Copied Data: " << *data << ")" << std::endl;
        } else {
            data = nullptr;
            std::cout << "Copy Constructor called (ID: " << id << ", Source data was null)" << std::endl;
        }
    }

    // Destructor
    ~Example() {
        std::cout << "Destructor called (ID: " << id << ")";
        if (data) {
            std::cout << " Deleting data: " << *data;
            delete data; // Deallocate memory
            data = nullptr; // Good practice
        }
        std::cout << std::endl;
    }

    void display() {
         std::cout << "ID: " << id;
         if(data) std::cout << ", Data: " << *data;
         else std::cout << ", Data: null";
         std::cout << std::endl;
    }
};

int main() {
    std::cout << "--- Creating e1 (Param Ctor) ---" << std::endl;
    Example e1(1, 100);
    e1.display();

    std::cout << "\n--- Creating e2 from e1 (Copy Ctor) ---" << std::endl;
    Example e2 = e1; // Invokes Copy Constructor
    e2.display();

    std::cout << "\n--- Creating e3 (Default Ctor) ---" << std::endl;
    Example e3;
    e3.display();

    std::cout << "\n--- Exiting main (Destructors called in reverse order: e3, e2, e1) ---" << std::endl;
    return 0;
}
```

---

### Lecture 13: Pointers (May 29, 2024)

**Topics Covered:**
*   Review of C pointers.
*   Pointers to objects.
*   Arrow operator (`->`).
*   Dynamic memory allocation (`new`, `delete`).
*   `this` pointer.

**Detailed Notes:**

1.  **Pointers (Review):** A variable that stores the memory address of another variable. Declared using `*`. Accessed using `*` (dereference) and `&` (address-of).
2.  **Pointers to Objects:** You can have pointers that store the memory address of an object.
    ```cpp
    ClassName* ptr; // Declares a pointer to an object of type ClassName
    ClassName obj;
    ptr = &obj;    // ptr now holds the address of obj
    ```
3.  **Accessing Members via Pointers:**
    *   Use the arrow operator (`->`): `ptr->memberName`
    *   Equivalent to dereferencing the pointer first and then using the dot operator: `(*ptr).memberName`
    *   The arrow operator is generally preferred for readability.

4.  **Dynamic Memory Allocation in C++:** Used to allocate memory on the heap at runtime.
    *   **`new` Operator:** Allocates memory and returns a pointer to the allocated space. It also calls the appropriate constructor for objects.
        *   Single object: `ClassName* ptr = new ClassName(constructor_args);`
        *   Array of objects: `ClassName* ptrArr = new ClassName[size];` (Calls default constructor for each element).
        *   Primitive type: `int* intPtr = new int(10);`
        *   Array of primitive: `int* intArr = new int[size];`
    *   **`delete` Operator:** Deallocates memory previously allocated with `new`. Calls the destructor for objects before deallocating.
        *   Single object: `delete ptr;`
        *   Array of objects/primitives: `delete[] ptrArr;` (Using `[]` is crucial for arrays to ensure all destructors are called and memory is correctly freed).
    *   **Comparison with C (`malloc`/`free`):**
        *   `new`/`delete` are operators, `malloc`/`free` are functions.
        *   `new`/`delete` are type-safe (no casting needed).
        *   `new`/`delete` automatically call constructors/destructors. `malloc`/`free` do not.
        *   Generally prefer `new`/`delete` in C++.

5.  **`this` Pointer:**
    *   **Concept:** An implicit pointer available *inside every non-static member function* of a class.
    *   **Value:** It holds the memory address of the *object* on which the member function was invoked (the "calling object").
    *   **Type:** `ClassName* const` (a constant pointer to an object of the class type).
    *   **Purpose:**
        *   Disambiguate between member variables and local variables/parameters with the same name: `this->memberName = memberName;`
        *   Return a reference or pointer to the current object from a member function: `return *this;` (often used for operator overloading to enable cascading).
        *   Explicitly pass the current object's address to another function.

**Code Snippet:**

```cpp
#include <iostream>
#include <string>

class Item {
private:
    std::string name;
    int value;
public:
    Item(std::string n = "None", int v = 0) : name(n), value(v) {
        std::cout << "Item '" << name << "' constructed." << std::endl;
    }
    ~Item() {
        std::cout << "Item '" << name << "' destructed." << std::endl;
    }
    void display() {
        std::cout << "Item: " << name << ", Value: " << value << std::endl;
    }
    // Function returning reference to the object for chaining
    Item& setValue(int newValue) {
        this->value = newValue; // Using 'this' to access member
        return *this; // Return reference to the current object
    }
};

int main() {
    // Pointer to object
    Item* itemPtr;
    Item item1("Gadget", 50);

    itemPtr = &item1;

    std::cout << "\nAccessing via pointer:" << std::endl;
    itemPtr->display(); // Access member using ->
    (*itemPtr).display(); // Equivalent access using * and .

    // Dynamic Allocation
    std::cout << "\nDynamic Allocation:" << std::endl;
    Item* dynamicItem = new Item("Widget", 100); // Allocate on heap, calls constructor
    if (!dynamicItem) {
        std::cerr << "Memory allocation failed!" << std::endl;
        return 1;
    }
    dynamicItem->display();

    // Using 'this' for chaining
    std::cout << "\nUsing 'this' for chaining:" << std::endl;
    dynamicItem->setValue(150).display(); // setValue returns *this, then display() is called

    // Dynamic Array Allocation
    int size = 3;
    Item* itemArray = new Item[size]; // Allocates array, calls default constructor 3 times

    std::cout << "\nDisplaying dynamic array items:" << std::endl;
    for(int i = 0; i < size; ++i) {
        itemArray[i].setValue(i * 10).display();
    }

    // Deallocation
    std::cout << "\nDeallocating memory:" << std::endl;
    delete dynamicItem; // Deallocate single object, calls destructor
    delete[] itemArray; // Deallocate array, calls destructor for each element

    std::cout << "\nExiting main (item1 destructor called automatically)..." << std::endl;
    return 0;
}
```

---

### Lecture 14, 15, 16: Operator Overloading - Part I, II, III (May 30, 31 & Jun 4, 2024)

**Topics Covered:**
*   Concept and purpose.
*   Syntax using `operator` keyword.
*   Overloading as member functions vs. non-member (friend) functions.
*   Rules and limitations.
*   Overloading binary operators (e.g., `+`).
*   Overloading unary operators (e.g., `++`, `-`).
*   Overloading stream operators (`<<`, `>>`).
*   Cascading operators.
*   `this` pointer in operator overloading.

**Detailed Notes:**

1.  **Concept:** Extending the functionality of existing C++ operators to work with user-defined types (classes/structs).
2.  **Purpose:** To make operations on objects more intuitive and resemble operations on built-in types, improving code readability and expressiveness (syntactic sugar). Example: `Complex c3 = c1 + c2;` is more natural than `Complex c3 = c1.add(c2);`.
3.  **Syntax:** Define a special function named `operator<op>` where `<op>` is the operator symbol (e.g., `operator+`, `operator==`, `operator<<`, `operator++`).
4.  **Implementation Methods:**
    *   **Member Function:**
        *   Declared inside the class.
        *   The left operand is implicitly the calling object (`this`).
        *   Binary operators take *one* explicit parameter (the right operand).
        *   Unary operators take *no* explicit parameters.
        *   Example: `Complex Complex::operator+(const Complex& other) const;`
    *   **Non-Member Function (often `friend`):**
        *   Declared outside the class (often declared as `friend` inside the class if private/protected access is needed).
        *   Binary operators take *two* parameters (left and right operands).
        *   Unary operators take *one* parameter.
        *   Necessary when the left operand is not an object of the class (e.g., `cout << obj;` - `cout` is not a `Complex` object) or for symmetric conversions.
        *   Example: `friend std::ostream& operator<<(std::ostream& os, const Complex& c);`

5.  **Rules & Limitations:**
    *   Cannot overload: `.` (member access), `.*` (member pointer access), `::` (scope resolution), `?:` (ternary), `sizeof`.
    *   Cannot change operator precedence, arity (number of operands), or associativity.
    *   At least one operand must be of a user-defined type (cannot overload `int + int`).
    *   Cannot invent new operators.

6.  **Overloading Common Operators:**
    *   **Binary Arithmetic (`+`, `-`, `*`, `/`):** Often implemented as member functions or non-member friends. Usually return a new object representing the result.
    *   **Stream Insertion (`<<`):** Must be a non-member function (usually `friend`). Takes `std::ostream&` as the first parameter and `const ClassName&` as the second. Returns `std::ostream&` to allow chaining.
    *   **Stream Extraction (`>>`):** Must be a non-member function (usually `friend`). Takes `std::istream&` as the first parameter and `ClassName&` (non-const) as the second. Returns `std::istream&` for chaining.
    *   **Comparison (`==`, `!=`, `<`, etc.):** Can be member or non-member. Return `bool`.
    *   **Assignment (`=`):** Special case. Compiler provides a default member-wise assignment operator. Should be overloaded (as a member function) if deep copy is needed (Rule of Three/Five). Returns `ClassName&` (`*this`).
    *   **Increment/Decrement (`++`, `--`):**
        *   **Prefix (`++obj`):** Overloaded as member with no parameters (`operator++()`) or non-member with one parameter (`operator++(ClassName&)`). Should modify the object and return a reference to the modified object (`*this` for member).
        *   **Postfix (`obj++`):** Overloaded as member with a dummy `int` parameter (`operator++(int)`) or non-member with two parameters (`operator++(ClassName&, int)`). Should typically store the original state, modify the object, and return the *original* state (by value).

7.  **Cascading:** Achieved by returning a reference (usually `*this` for members modifying the object, or the stream object for `<<`/`>>`). Allows expressions like `c1 = c2 = c3;` or `cout << c1 << c2;`.

**Code Snippet (Adding Operators to Complex Class):**

```cpp
#include <iostream>

class Complex {
private:
    double real;
    double imag;

public:
    // Constructor
    Complex(double r = 0.0, double i = 0.0) : real(r), imag(i) {}

    // --- Member Operator Overloading ---

    // Overload + as a member function
    Complex operator+(const Complex& other) const {
        Complex result;
        result.real = this->real + other.real;
        result.imag = this->imag + other.imag;
        return result; // Return new object by value
    }

    // Overload == as a member function
    bool operator==(const Complex& other) const {
        return (this->real == other.real) && (this->imag == other.imag);
    }

    // Overload prefix ++ as a member function
    Complex& operator++() {
        this->real++; // Modify the object
        this->imag++;
        return *this; // Return reference to modified object for cascading
    }

    // Overload postfix ++ as a member function
    Complex operator++(int) { // Dummy int parameter indicates postfix
        Complex temp = *this; // Store original state
        ++(*this);            // Use prefix ++ to modify the object
        return temp;          // Return the original state by value
    }


    // --- Friend Operator Overloading (for I/O) ---
    // Friend declaration for stream insertion operator <<
    friend std::ostream& operator<<(std::ostream& os, const Complex& c);

    // Friend declaration for stream extraction operator >>
    friend std::istream& operator>>(std::istream& is, Complex& c);

    // Simple display function (alternative to <<)
    void display() const {
         std::cout << real << " + " << imag << "i";
    }
};

// --- Friend Function Definitions ---

// Definition of overloaded stream insertion operator <<
std::ostream& operator<<(std::ostream& os, const Complex& c) {
    os << c.real << " + " << c.imag << "i"; // Can access private members because it's a friend
    return os; // Return ostream reference for cascading
}

// Definition of overloaded stream extraction operator >>
std::istream& operator>>(std::istream& is, Complex& c) {
    std::cout << "Enter real part: ";
    is >> c.real; // Can access private members
    std::cout << "Enter imaginary part: ";
    is >> c.imag;
    return is; // Return istream reference for cascading
}


int main() {
    Complex c1(2.0, 3.0);
    Complex c2(1.0, 5.0);
    Complex c3, c4;

    std::cout << "c1 = " << c1 << std::endl; // Uses overloaded <<
    std::cout << "c2 = " << c2 << std::endl;

    c3 = c1 + c2; // Uses overloaded +
    std::cout << "c3 (c1 + c2) = " << c3 << std::endl;

    if (c1 == c2) { // Uses overloaded ==
        std::cout << "c1 and c2 are equal." << std::endl;
    } else {
        std::cout << "c1 and c2 are NOT equal." << std::endl;
    }

    std::cout << "\nPrefix Increment:" << std::endl;
    std::cout << "Original c1: " << c1 << std::endl;
    c4 = ++c1; // Uses prefix ++
    std::cout << "After ++c1, c1 = " << c1 << std::endl;
    std::cout << "Value assigned to c4 = " << c4 << std::endl;

    std::cout << "\nPostfix Increment:" << std::endl;
    std::cout << "Original c2: " << c2 << std::endl;
    c4 = c2++; // Uses postfix ++
    std::cout << "After c2++, c2 = " << c2 << std::endl;
    std::cout << "Value assigned to c4 = " << c4 << std::endl; // Should be the value *before* increment

    // Complex c5;
    // std::cout << "\nEnter details for c5:" << std::endl;
    // std::cin >> c5; // Uses overloaded >>
    // std::cout << "You entered c5 = " << c5 << std::endl;

    return 0;
}
```

---

### Lecture 17: Friend Function (Jun 5, 2024)

**Topics Covered:**
*   Concept of friend functions.
*   Syntax for declaring friends.
*   Purpose and use cases (operator overloading, multi-class operations).
*   Friend classes.

**Detailed Notes:**

1.  **Concept:** A `friend` function of a class is a non-member function that is granted special permission to access the `private` and `protected` members of that class.
2.  **Why Needed?** Encapsulation restricts access to private/protected members from outside the class. However, sometimes it's necessary or more convenient for a non-member function to access these members.
3.  **Syntax:**
    *   **Declaration:** The function is declared inside the class definition, prefixed with the `friend` keyword.
        ```cpp
        class MyClass {
        private:
            int secret;
        public:
            MyClass(int s = 0) : secret(s) {}
            // Friend function declaration
            friend void showSecret(const MyClass& obj);

            // Friend declaration for operator overloading
            friend std::ostream& operator<<(std::ostream& os, const MyClass& obj);
        };
        ```
    *   **Definition:** The function is defined outside the class like a normal non-member function (without the `friend` keyword and without `ClassName::`).
        ```cpp
        // Friend function definition
        void showSecret(const MyClass& obj) {
            // Can access private member 'secret' because it's a friend
            std::cout << "The secret is: " << obj.secret << std::endl;
        }

        std::ostream& operator<<(std::ostream& os, const MyClass& obj) {
            os << "MyClass secret: " << obj.secret; // Access private member
            return os;
        }
        ```
4.  **Key Properties:**
    *   It's *not* a member function of the class (it's not called using `object.friendFunc()`, and it doesn't receive a `this` pointer implicitly).
    *   It can access all members (`public`, `protected`, `private`) of the class for which it is declared a friend.
    *   Friendship is *granted* by the class, not taken by the function.
    *   Friendship is *not* symmetric (if A is a friend of B, B is not automatically a friend of A).
    *   Friendship is *not* transitive (if A is a friend of B, and B is a friend of C, A is not automatically a friend of C).
    *   Friendship is *not* inherited (friends of a base class are not automatically friends of a derived class).

5.  **Use Cases:**
    *   **Operator Overloading:** Especially for binary operators where the left operand is not an object of the class (like `<<`, `>>`) or when symmetric behavior is desired (e.g., `Complex + int` and `int + Complex`).
    *   **Functions Operating on Multiple Classes:** A function might need to access private members of two different classes simultaneously. It can be declared as a friend in both classes.
    *   Factory functions or helper functions that are closely related to a class but don't logically belong as members.

6.  **Friend Classes:** An entire class can be declared as a friend of another class. This grants all member functions of the friend class access to the private and protected members of the class granting friendship.
    ```cpp
    class B; // Forward declaration

    class A {
    private:
        int dataA;
        friend class B; // Class B is a friend of A
    };

    class B {
    public:
        void processA(A& objA) {
            objA.dataA = 10; // OK: B is a friend of A
        }
    };
    ```

7.  **Caution:** Friend functions/classes break strict encapsulation. Use them judiciously when necessary for design clarity or functionality that cannot be easily achieved otherwise.

**Code Snippet:** (Using the Complex class example from previous lecture, where `<<` and `>>` were friends)

```cpp
#include <iostream>

class Complex {
private:
    double real;
    double imag;

public:
    Complex(double r = 0.0, double i = 0.0) : real(r), imag(i) {}

    // Friend declarations (granting access)
    friend std::ostream& operator<<(std::ostream& os, const Complex& c);
    friend Complex addReal(double r_val, const Complex& c); // Another friend example
};

// Friend function definitions (non-members)
std::ostream& operator<<(std::ostream& os, const Complex& c) {
    // Accessing private members directly because it's a friend
    os << c.real << " + " << c.imag << "i";
    return os;
}

Complex addReal(double r_val, const Complex& c) {
    // Accessing private members directly
    return Complex(r_val + c.real, c.imag);
}

int main() {
    Complex c1(5.0, 6.0);

    std::cout << "c1 = " << c1 << std::endl; // Uses friend operator<<

    Complex c2 = addReal(10.0, c1); // Uses friend function addReal
    std::cout << "c2 (10.0 + c1) = " << c2 << std::endl;

    return 0;
}
```

---

### Lecture 18-25: Inheritance - Part I-VIII (Jun 6 - Jun 15, 2024)

**Topics Covered:**
*   Concept: IS-A relationship, reusability, extensibility.
*   Syntax, base/derived classes.
*   Access Specifiers in Inheritance (`public`, `protected`, `private`).
*   Accessibility rules summary.
*   Constructor/Destructor call order.
*   Calling base class constructors (initializer list).
*   Function Overriding vs. Hiding.
*   Types of Inheritance (Single, Multiple, Multilevel, Hierarchical, Hybrid).
*   Multiple Inheritance issues (Ambiguity, Diamond Problem).
*   Virtual Inheritance.
*   Early vs. Late Binding (Static vs. Dynamic Polymorphism).

**Detailed Notes:**

1.  **Concept:** Inheritance is a fundamental OOP mechanism allowing a new class (derived class) to acquire the properties (data members) and behaviors (member functions) of an existing class (base class).
    *   **IS-A Relationship:** Public inheritance models an "IS-A" relationship (e.g., a `Manager` IS-A type of `Employee`).
    *   **Benefits:**
        *   **Code Reusability:** Avoids duplicating code from the base class.
        *   **Extensibility:** Easily add new features in the derived class without modifying the base class.
        *   **Maintainability:** Changes in the base class are reflected in derived classes.
        *   **Polymorphism:** Enables treating objects of derived classes as objects of the base class (covered later).

2.  **Syntax:**
    ```cpp
    class Base { ... };
    class Derived : accessMode Base { ... };
    // accessMode can be public, protected, or private
    ```

3.  **Access Control & Inheritance:** The `accessMode` determines the accessibility of *inherited* members within the derived class and further down the hierarchy.
    *   **`public` Inheritance:** (Most common, models IS-A)
        *   Base `public` members become `public` in Derived.
        *   Base `protected` members become `protected` in Derived.
        *   Base `private` members are *inherited* but *inaccessible* directly by Derived.
    *   **`protected` Inheritance:**
        *   Base `public` members become `protected` in Derived.
        *   Base `protected` members become `protected` in Derived.
        *   Base `private` members are inherited but inaccessible.
    *   **`private` Inheritance:** (Models "implemented-in-terms-of")
        *   Base `public` members become `private` in Derived.
        *   Base `protected` members become `private` in Derived.
        *   Base `private` members are inherited but inaccessible.
    *   **Summary:** A derived class can access its own members and the `public` and `protected` members of its base class (depending on the inheritance mode). It *cannot* directly access `private` members of the base class.

4.  **Constructor & Destructor Order:**
    *   **Construction:** When a derived object is created, the base class constructor is called *first*, followed by the derived class constructor.
    *   **Destruction:** When a derived object is destroyed, the derived class destructor is called *first*, followed by the base class destructor.

5.  **Calling Base Class Constructors:**
    *   If the base class has a default (no-argument) constructor, it's called automatically.
    *   If you need to call a specific *parameterized* base class constructor, or if the base class *only* has parameterized constructors, you *must* call it explicitly using the *member initializer list* in the derived constructor's definition.
    ```cpp
    class Base {
    public:
        Base(int b_val) { /* ... */ }
    };
    class Derived : public Base {
    public:
        // Must call Base constructor in initializer list
        Derived(int d_val, int b_val) : Base(b_val) { /* ... */ }
    };
    ```

6.  **Function Overriding vs. Hiding:**
    *   **Overriding:** A derived class provides its own implementation for a member function that already exists in the base class *with the exact same signature* (name, parameters, const-ness). Used for polymorphism with `virtual` functions.
    *   **Hiding (Name Hiding):** If a derived class defines a member function with the *same name* as a base class function but a *different signature*, it *hides* all base class functions with that name. Base class versions are no longer directly accessible via the derived object unless explicitly qualified (`derivedObj.Base::func()`) or brought into scope (`using Base::func;`).

7.  **Types of Inheritance:**
    *   **Single:** Derived class inherits from one base class.
    *   **Multilevel:** Derived class inherits from a base class, which itself is derived from another class (A -> B -> C).
    *   **Multiple:** Derived class inherits from two or more base classes (A -> C, B -> C).
    *   **Hierarchical:** Multiple derived classes inherit from a single base class (A -> B, A -> C).
    *   **Hybrid:** Combination of two or more types (e.g., multilevel and multiple), often leading to the Diamond Problem.

8.  **Diamond Problem (Multiple Inheritance Ambiguity):**
    *   Occurs when a class D inherits from two classes B and C, and both B and C inherit from a common base class A.
    *   Problem: D gets two copies of the members from A (one via B, one via C). Calls to A's members via a D object become ambiguous.
    *   **Solution: Virtual Inheritance.** Declare the inheritance from A as `virtual` in the intermediate classes (B and C).
    ```cpp
    class A { ... };
    class B : virtual public A { ... }; // Virtual inheritance
    class C : virtual public A { ... }; // Virtual inheritance
    class D : public B, public C { ... }; // D gets only ONE copy of A's members
    ```

9.  **Binding (Polymorphism Context):**
    *   **Early (Static) Binding:** The function call address is determined at compile time. This is the default for non-virtual functions. The function called depends on the *static type* of the pointer or reference used to make the call.
    *   **Late (Dynamic) Binding:** The function call address is determined at run time based on the *actual type* of the object being pointed/referred to. Requires:
        *   Base class pointer or reference.
        *   Pointer/reference pointing to a derived class object.
        *   The function being called must be declared `virtual` in the base class.

**Code Snippet (Illustrating Inheritance, Overriding, Virtual):**

```cpp
#include <iostream>
#include <string>

// Base Class
class Employee {
protected: // Accessible by derived classes
    std::string name;
    int id;
public:
    Employee(std::string n = "Unknown", int i = 0) : name(n), id(i) {}

    // Virtual function for dynamic binding (polymorphism)
    virtual void displayDetails() const {
        std::cout << "ID: " << id << ", Name: " << name;
    }

    // Base class destructor should be virtual if using polymorphism with pointers
    virtual ~Employee() {
        std::cout << "~Employee Destructor for " << name << std::endl;
    }
};

// Derived Class
class Manager : public Employee { // Public Inheritance (IS-A)
private:
    std::string department;
public:
    // Call base constructor using initializer list
    Manager(std::string n, int i, std::string dept) : Employee(n, i), department(dept) {}

    // Override the virtual function from the base class
    void displayDetails() const override { // 'override' keyword is optional but recommended
        Employee::displayDetails(); // Call base version first (optional)
        std::cout << ", Department: " << department; // Add derived class info
    }

     ~Manager() {
        std::cout << "~Manager Destructor for " << name << std::endl;
    }
};

// Another Derived Class
class Engineer : public Employee {
private:
    std::string specialty;
public:
    Engineer(std::string n, int i, std::string spec) : Employee(n, i), specialty(spec) {}

    void displayDetails() const override {
        Employee::displayDetails();
        std::cout << ", Specialty: " << specialty;
    }

     ~Engineer() {
        std::cout << "~Engineer Destructor for " << name << std::endl;
    }
};

// Function demonstrating polymorphism
void showEmployeeInfo(const Employee& emp) { // Takes Base class reference
    emp.displayDetails(); // Calls the correct version (Base or Derived) due to virtual
    std::cout << std::endl;
}

int main() {
    Employee emp1("Alice", 101);
    Manager mgr1("Bob", 201, "Sales");
    Engineer eng1("Charlie", 301, "Software");

    std::cout << "--- Direct Calls ---" << std::endl;
    emp1.displayDetails(); std::cout << std::endl;
    mgr1.displayDetails(); std::cout << std::endl;
    eng1.displayDetails(); std::cout << std::endl;

    std::cout << "\n--- Polymorphic Calls via Reference ---" << std::endl;
    showEmployeeInfo(emp1); // Calls Employee::displayDetails
    showEmployeeInfo(mgr1); // Calls Manager::displayDetails
    showEmployeeInfo(eng1); // Calls Engineer::displayDetails

    std::cout << "\n--- Polymorphic Calls via Pointer ---" << std::endl;
    Employee* empPtr;

    empPtr = &mgr1;
    empPtr->displayDetails(); std::cout << std::endl; // Calls Manager::displayDetails

    empPtr = &eng1;
    empPtr->displayDetails(); std::cout << std::endl; // Calls Engineer::displayDetails

    std::cout << "\n--- Dynamic Allocation & Deletion ---" << std::endl;
    Employee* empPtrDynamic = new Manager("David", 401, "Marketing");
    empPtrDynamic->displayDetails(); std::cout << std::endl;
    delete empPtrDynamic; // Calls ~Manager then ~Employee because base destructor is virtual

    std::cout << "\n--- Exiting main (Destructors for emp1, mgr1, eng1) ---" << std::endl;
    return 0;
}
```

---

### Lecture 26, 27: Late Binding / Run Time Polymorphism / Virtual Functions (Jun 19 & 20, 2024)

**Topics Covered:**
*   Early Binding vs. Late Binding recap.
*   Achieving Late Binding using `virtual` functions.
*   vtable and vptr mechanism (conceptual).
*   Runtime Polymorphism.

**Detailed Notes:**

1.  **Binding Recap:**
    *   **Early (Static) Binding:** Function call resolved at compile time based on the *static type* of the pointer/reference. Default for non-virtual functions. Example: If `Employee* ptr = &mgr1;`, a call to a non-virtual `ptr->someFunc()` would always call `Employee::someFunc()`.
    *   **Late (Dynamic) Binding:** Function call resolved at run time based on the *actual type* of the object being pointed/referred to. Requires `virtual` functions. Example: If `Employee* ptr = &mgr1;` and `displayDetails()` is virtual, `ptr->displayDetails()` calls `Manager::displayDetails()` at runtime.

2.  **`virtual` Keyword:**
    *   Placed before the function declaration in the *base class*.
    *   Signals to the compiler that this function might be overridden in derived classes and that calls via base pointers/references should use late binding.
    *   Once a function is declared `virtual` in the base class, it remains virtual in all derived classes, even if the `virtual` keyword isn't repeated (though repeating it or using `override` is good practice).

3.  **Runtime Polymorphism:** "Many forms" at runtime. The ability of code (like `showEmployeeInfo` function or `empPtr->displayDetails()` call) to behave differently depending on the actual type of the object being processed at runtime. This is a cornerstone of OOP, enabled by inheritance and virtual functions.

4.  **vtable and vptr (Conceptual Mechanism):**
    *   **vtable (Virtual Table):** When a class declares or inherits at least one virtual function, the compiler typically creates a static array called the vtable for that class. This table contains pointers to the correct versions of the virtual functions for that specific class (including overridden ones).
    *   **vptr (Virtual Pointer):** Each *object* of a class with a vtable contains a hidden pointer member, the vptr, which points to the vtable for its class. This vptr is initialized by the constructor.
    *   **Call Process:** When a virtual function is called via a base class pointer/reference (`ptr->virtualFunc()`), the runtime system:
        1.  Uses the object's vptr to find the correct vtable (e.g., the Manager's vtable if `ptr` points to a `Manager` object).
        2.  Looks up the address of `virtualFunc` within that vtable.
        3.  Calls the function at that address.
    *   This lookup mechanism allows the correct derived class function to be called even though the call is made through a base class pointer.

5.  **Virtual Destructors:** If a class is intended to be used as a base class in polymorphic scenarios (i.e., you might `delete` a derived object through a base class pointer), the base class destructor *must* be declared `virtual`.
    *   **Why?** If the base destructor is *not* virtual, `delete basePtr;` (where `basePtr` points to a derived object) will only call the base class destructor (early binding), leading to resource leaks if the derived class destructor had cleanup work to do.
    *   Declaring the base destructor `virtual` ensures late binding is used for destruction, so the derived destructor is called first, followed by the base destructor, ensuring proper cleanup.

**Code Snippet:** (See the code for Lecture 18-25, which already demonstrates virtual functions, overriding, polymorphism, and virtual destructors).

---

### Lecture 28: Generic Programming / Abstract Class (Jun 21, 2024)

*(Note: Slide title mismatch - focusing on Abstract Class content shown)*

**Topics Covered:**
*   Pure Virtual Functions.
*   Abstract Classes: definition, properties, purpose.
*   Forcing implementation in derived classes.

**Detailed Notes:**

1.  **Problem:** Sometimes a base class represents a concept so general that it doesn't make sense to provide a default implementation for certain functions. We want to define an *interface* that derived classes *must* implement.
    *   Example: A `Shape` class. What does `draw()` mean for a generic shape? It only makes sense for specific shapes like `Circle` or `Rectangle`.

2.  **Pure Virtual Function:**
    *   A virtual function declared in the base class that has no implementation provided in the base class itself.
    *   **Syntax:** Append `= 0;` to the virtual function declaration.
        ```cpp
        class Shape {
        public:
            // Pure virtual function (defines an interface)
            virtual void draw() const = 0;
            virtual ~Shape() {} // Virtual destructor is still important!
        };
        ```
    *   The `= 0` signifies that the derived classes are responsible for providing the implementation.

3.  **Abstract Class:**
    *   A class that contains one or more pure virtual functions.
    *   **Key Property:** You *cannot* create objects (instances) of an abstract class directly.
        ```cpp
        Shape s; // Error! Cannot instantiate abstract class Shape
        Shape* ptr; // OK: Can have pointers/references to abstract class
        ```
    *   **Purpose:**
        *   To serve as a base class for inheritance.
        *   To define a common interface that all derived classes must adhere to.
        *   To enforce implementation of certain functionalities in derived classes.
        *   Used extensively for polymorphism.

4.  **Concrete Class:**
    *   A non-abstract class (a class for which objects can be created).
    *   A derived class inheriting from an abstract base class becomes concrete *only if* it provides implementations (overrides) for *all* the pure virtual functions inherited from the base class.
    *   If a derived class does not override all inherited pure virtual functions, it also becomes an abstract class.

**Code Snippet:**

```cpp
#include <iostream>
#include <vector>

// Abstract Base Class (Interface)
class Shape {
public:
    // Pure virtual function - makes Shape abstract
    virtual void draw() const = 0;

    // Virtual destructor is crucial for base classes with virtual functions
    virtual ~Shape() {
        std::cout << "~Shape destructor" << std::endl;
    }
};

// Concrete Derived Class 1
class Circle : public Shape {
private:
    double radius;
public:
    Circle(double r) : radius(r) {}

    // Provide implementation for the pure virtual function
    void draw() const override {
        std::cout << "Drawing Circle with radius " << radius << std::endl;
    }

    ~Circle() {
        std::cout << "~Circle destructor" << std::endl;
    }
};

// Concrete Derived Class 2
class Rectangle : public Shape {
private:
    double width, height;
public:
    Rectangle(double w, double h) : width(w), height(h) {}

    // Provide implementation for the pure virtual function
    void draw() const override {
        std::cout << "Drawing Rectangle with width " << width << " and height " << height << std::endl;
    }
     ~Rectangle() {
        std::cout << "~Rectangle destructor" << std::endl;
    }
};

// class Square : public Shape { // This would also be abstract if draw() wasn't implemented
// private: double side;
// public: Square(double s) : side(s) {}
// // Missing: void draw() const override { ... }
// };

int main() {
    // Shape s; // Error! Cannot create object of abstract class Shape
    // Square sq(5); // Error! Square is abstract because it didn't implement draw()

    Circle c(10.0);
    Rectangle r(5.0, 8.0);

    // Polymorphism using pointers to abstract base class
    std::vector<Shape*> shapes;
    shapes.push_back(&c);
    shapes.push_back(&r);
    shapes.push_back(new Circle(7.5)); // Dynamically allocated
    shapes.push_back(new Rectangle(3, 4)); // Dynamically allocated

    std::cout << "--- Drawing all shapes ---" << std::endl;
    for (const Shape* shapePtr : shapes) {
        shapePtr->draw(); // Calls the correct derived class version
    }

    std::cout << "\n--- Cleaning up dynamic shapes ---" << std::endl;
    // Clean up dynamically allocated memory
    delete shapes[2]; // Calls ~Circle then ~Shape
    delete shapes[3]; // Calls ~Rectangle then ~Shape

    std::cout << "\n--- Exiting main (Destructors for c, r) ---" << std::endl;
    return 0;
}
```

---

### Lecture 29: Revising All Concepts (Jun 22, 2024)

**Topics Covered:**
*   A summary and review of all major C++ concepts covered in the previous lectures.

**Detailed Notes:**

*   **C++ Fundamentals:** Superset of C, hybrid (procedural + OOP), basic syntax, I/O (`cout`, `cin`, `<<`, `>>`), namespaces (`std`).
*   **Functions:** Call overhead, inline functions (optimization request), default arguments (right-aligned rule).
*   **Memory:** Static vs. Dynamic allocation (`new`, `delete`, `delete[]`).
*   **References:** Aliases (`&`), initialization rule, non-null, non-reseatable, Call by Reference.
*   **OOP Core Concepts:**
    *   **Encapsulation:** Bundling data and methods (classes, structs).
    *   **Data Hiding:** Protecting internal state (`private`, `protected`).
    *   **Abstraction:** Hiding implementation details (public interface).
    *   **Classes:** Blueprints (members: data/functions, static/instance).
    *   **Objects:** Instances of classes.
    *   **Access Specifiers:** `public`, `private`, `protected`.
*   **Class Members:**
    *   Instance variables/methods (object-specific).
    *   Static variables/methods (class-specific, shared).
*   **Special Member Functions:**
    *   **Constructors:** Initialization (Default, Parameterized, Copy), overloading rules, compiler-generated versions.
    *   **Destructors:** Cleanup (`~ClassName()`), automatic invocation, virtual destructors.
*   **`this` Pointer:** Implicit pointer to the calling object in non-static methods.
*   **Operator Overloading:** Extending operators for user-defined types (`operator+`, `operator<<`, etc.), member vs. non-member (friend) implementation, rules, cascading.
*   **Friend Functions/Classes:** Granting non-member access to private/protected members.
*   **Inheritance:** Code reuse, IS-A relationship (`:` syntax), access modes (`public`, `protected`, `private`), constructor/destructor order, calling base constructors, types (single, multi-level, multiple, hierarchical, hybrid).
*   **Polymorphism:**
    *   **Compile-time (Static):** Function overloading, operator overloading.
    *   **Run-time (Dynamic):** Inheritance + Virtual Functions.
*   **Advanced Inheritance:** Function overriding vs. hiding, Diamond Problem, Virtual Inheritance (`virtual` base class).
*   **Virtual Functions:** `virtual` keyword, late binding, vtable/vptr mechanism, pure virtual functions (`= 0`), abstract classes (interfaces, cannot be instantiated).

*(No new code for this lecture)*

---

### Lecture 30: Templates (Jun 26, 2024)

**Topics Covered:**
*   Generic Programming concept.
*   Function Templates.
*   Class Templates.
*   Template instantiation.

**Detailed Notes:**

1.  **Problem:** Often, the logic for a function or class is the same regardless of the specific data type it operates on (e.g., finding the maximum of two numbers, implementing a stack). Writing separate versions for `int`, `float`, `double`, `string`, etc., is repetitive and error-prone.
2.  **Generic Programming:** Writing code that can work with multiple data types without knowing the specific type beforehand. C++ achieves this using *templates*.
3.  **Function Templates:**
    *   **Concept:** A blueprint for creating functions. Allows defining a function once that can work with different data types.
    *   **Syntax:**
        ```cpp
        template <typename T> // or template <class T>
        returnType functionName(T param1, ...) {
            // Function body using type T
        }
        ```
        *   `template <...>`: Template declaration.
        *   `typename T` or `class T`: Declares `T` as a placeholder (template parameter) for a data type. `typename` and `class` are interchangeable here. You can have multiple template parameters (`template <typename T1, typename T2>`).
    *   **Instantiation:** When you call a function template with specific argument types (e.g., `findMax(5, 10)` or `findMax(3.4, 1.2)`), the compiler generates (instantiates) a specific version of the function for those types (`findMax<int>(int, int)` or `findMax<double>(double, double)`).

4.  **Class Templates:**
    *   **Concept:** A blueprint for creating classes. Allows defining a class once that can store or operate on different data types.
    *   **Syntax:**
        ```cpp
        template <typename T> // or template <class T>
        class ClassName {
        private:
            T memberVariable; // Member using the template type
            // ...
        public:
            void functionName(T param); // Method using the template type
            // ...
        };
        ```
    *   **Member Function Definition:** When defining member functions outside the class template, you need to repeat the template prefix and use the template parameter:
        ```cpp
        template <typename T>
        void ClassName<T>::functionName(T param) {
            // Implementation...
        }
        ```
    *   **Instantiation:** You must explicitly specify the data type when creating objects of a class template.
        ```cpp
        ClassName<int> obj1;
        ClassName<double> obj2;
        ClassName<std::string> obj3;
        ```
        The compiler generates separate class definitions for `ClassName<int>`, `ClassName<double>`, etc.

5.  **STL:** The Standard Template Library is built heavily on templates (e.g., `vector<T>`, `list<T>`, `map<K, V>`).

**Code Snippet:**

```cpp
#include <iostream>
#include <string>
#include <vector> // Needed for Stack example below

// --- Function Template ---
template <typename T>
T findMax(T a, T b) {
    return (a > b) ? a : b;
}

// --- Class Template ---
template <typename T>
class Stack {
private:
    std::vector<T> elements; // Use a vector internally

public:
    bool isEmpty() const {
        return elements.empty();
    }

    void push(const T& value) {
        elements.push_back(value);
    }

    T pop() {
        if (isEmpty()) {
            throw std::out_of_range("Stack<>::pop(): empty stack");
        }
        T topValue = elements.back();
        elements.pop_back();
        return topValue;
    }

    T top() const {
         if (isEmpty()) {
            throw std::out_of_range("Stack<>::top(): empty stack");
        }
        return elements.back();
    }
};


int main() {
    // --- Using Function Template ---
    std::cout << "Max(5, 10) = " << findMax(5, 10) << std::endl; // Instantiates findMax<int>
    std::cout << "Max(5.5, 3.1) = " << findMax(5.5, 3.1) << std::endl; // Instantiates findMax<double>
    std::cout << "Max('a', 'z') = " << findMax('a', 'z') << std::endl; // Instantiates findMax<char>
    // std::cout << "Max(5, 3.1) = " << findMax(5, 3.1) << std::endl; // Error! Cannot deduce consistent T

    // --- Using Class Template ---
    Stack<int> intStack; // Instantiates Stack for int
    intStack.push(10);
    intStack.push(20);
    std::cout << "Int Stack Top: " << intStack.top() << std::endl;
    std::cout << "Int Stack Pop: " << intStack.pop() << std::endl;

    Stack<std::string> stringStack; // Instantiates Stack for string
    stringStack.push("Hello");
    stringStack.push("World");
    std::cout << "String Stack Top: " << stringStack.top() << std::endl;
    std::cout << "String Stack Pop: " << stringStack.pop() << std::endl;

    return 0;
}
```

---

### Lecture 31-35: STL - Part I-V (Jun 28, 29 & Jul 1, 2, 2024)

**Topics Covered:**
*   Introduction to STL: Containers, Iterators, Algorithms.
*   Sequence Containers (`vector`, `list`, `deque`, `array`, `forward_list`).
*   Container Adapters (`stack`, `queue`, `priority_queue`).
*   Associative Containers (`set`, `map`, `multiset`, `multimap`).
*   Unordered Associative Containers (`unordered_set`, `unordered_map`, etc.).
*   Iterators: types, usage (`begin`, `end`, `*`, `++`).
*   Algorithms (`sort`, `find`, etc.).
*   `pair` utility.
*   `vector` details: dynamic size, capacity, `push_back`, `at`, `[]`, iterators.
*   `list` details: doubly linked, `push_front`, `push_back`, no random access.
*   `deque` details: double-ended queue, random access, efficient front/back ops.
*   `stack`, `queue`: adapter interfaces.
*   `vector<vector<T>>` for 2D arrays.

**Detailed Notes:**

1.  **STL Overview:** A library of generic components for common programming tasks. Key parts:
    *   **Containers:** Data structures to store collections (e.g., `vector`, `list`, `map`).
    *   **Iterators:** Objects that provide a uniform way to traverse elements in containers (like smart pointers).
    *   **Algorithms:** Generic functions that operate on ranges of elements defined by iterators (e.g., `sort`, `find`, `copy`).

2.  **Containers:**
    *   **Sequence Containers:** Maintain the insertion order.
        *   `vector`: Dynamic array. Fast random access (`[]`, `at`). Fast insertion/deletion at the *end* (`push_back`, `pop_back`). Insertion/deletion in the middle is slow.
        *   `list`: Doubly-linked list. No random access. Fast insertion/deletion *anywhere*. Uses bidirectional iterators.
        *   `deque`: Double-ended queue. Fast random access. Fast insertion/deletion at *both ends* (`push_front`, `pop_front`, `push_back`, `pop_back`). More complex internally than vector.
        *   `array`: Fixed-size array wrapper (size known at compile time). Fast random access. No dynamic resizing.
        *   `forward_list`: Singly-linked list. Uses forward iterators only. Most memory efficient for simple linear lists.
    *   **Associative Containers:** Elements stored in sorted order based on keys. Fast search, insertion, deletion (logarithmic time).
        *   `set`: Stores unique keys.
        *   `multiset`: Allows duplicate keys.
        *   `map`: Stores key-value pairs, unique keys.
        *   `multimap`: Allows duplicate keys (key-value pairs).
    *   **Unordered Associative Containers:** Elements stored based on hash values (unordered). Fastest average time for search, insertion, deletion (constant time). Worst-case time can be linear. Use when order doesn't matter. (`unordered_set`, `unordered_map`, etc.).
    *   **Container Adapters:** Provide a restricted interface on top of an underlying container (usually `vector`, `deque`, or `list`).
        *   `stack`: LIFO (Last-In, First-Out). Operations: `push`, `pop`, `top`.
        *   `queue`: FIFO (First-In, First-Out). Operations: `push`, `pop`, `front`, `back`.
        *   `priority_queue`: Element with highest priority (default is max-heap) is always at the `top`. Operations: `push`, `pop`, `top`.

3.  **Iterators:**
    *   Objects that "point" to elements within a container.
    *   Provide a common interface for algorithms to work with different containers.
    *   Common operations: `*it` (dereference to get value), `++it` (move to next element).
    *   Getting iterators: `container.begin()` (points to first element), `container.end()` (points *past* the last element).
    *   Types (determine capabilities): Input, Output, Forward, Bidirectional, Random Access. `vector` and `deque` have random access iterators (`it + n`). `list` has bidirectional (`++`, `--`).

4.  **Algorithms:**
    *   Generic functions in `<algorithm>` header (and `<numeric>`).
    *   Operate on ranges specified by iterators (e.g., `[begin, end)`).
    *   Examples: `sort`, `find`, `count`, `copy`, `reverse`, `accumulate`, `for_each`.

5.  **`pair`:**
    *   Simple template struct in `<utility>` to hold two values (potentially different types).
    *   `std::pair<type1, type2> p;`
    *   Access members: `p.first`, `p.second`.
    *   Creation helper: `std::make_pair(val1, val2)`.

**Code Snippet (Illustrating Vector, List, Pair, Stack, Algorithm):**

```cpp
#include <iostream>
#include <vector>
#include <list>
#include <stack>
#include <string>
#include <utility> // For pair
#include <algorithm> // For sort

int main() {
    // --- std::vector ---
    std::cout << "--- Vector Example ---" << std::endl;
    std::vector<int> v; // Dynamic array of ints
    v.push_back(10);    // Add to end
    v.push_back(30);
    v.push_back(20);

    std::cout << "Vector elements (using range-based for): ";
    for (int elem : v) {
        std::cout << elem << " ";
    }
    std::cout << std::endl;

    std::cout << "Vector elements (using iterators): ";
    for (std::vector<int>::iterator it = v.begin(); it != v.end(); ++it) {
        std::cout << *it << " ";
    }
    std::cout << std::endl;

    std::cout << "Element at index 1: " << v[1] << std::endl; // Access using []
    std::cout << "Size: " << v.size() << std::endl;

    // Using algorithm
    std::sort(v.begin(), v.end());
    std::cout << "Sorted vector: ";
     for (int elem : v) {
        std::cout << elem << " ";
    }
    std::cout << std::endl;


    // --- std::list ---
    std::cout << "\n--- List Example ---" << std::endl;
    std::list<std::string> l;
    l.push_back("World");
    l.push_front("Hello"); // Add to front
    l.push_back("!");

    std::cout << "List elements: ";
    for (const std::string& s : l) {
        std::cout << s << " ";
    }
    std::cout << std::endl;
    // std::cout << l[1]; // Error! list does not support random access []


    // --- std::pair ---
    std::cout << "\n--- Pair Example ---" << std::endl;
    std::pair<std::string, int> p1 = std::make_pair("Age", 30);
    std::cout << "Pair: " << p1.first << " = " << p1.second << std::endl;


    // --- std::stack (Adapter) ---
    std::cout << "\n--- Stack Example ---" << std::endl;
    std::stack<int> s; // Uses deque by default
    s.push(100);
    s.push(200);
    std::cout << "Stack top: " << s.top() << std::endl; // 200
    s.pop();
    std::cout << "Stack top after pop: " << s.top() << std::endl; // 100


    // --- Vector of Vectors (2D) ---
     std::cout << "\n--- Vector of Vectors ---" << std::endl;
     std::vector<std::vector<int>> matrix = { {1, 2}, {3, 4}, {5, 6} };
     matrix[1].push_back(99); // Add element to second row

     for(const auto& row : matrix) {
         for(int val : row) {
             std::cout << val << "\t";
         }
         std::cout << std::endl;
     }

    return 0;
}
```

---

### Lecture 36: Problem Solving (Jul 14, 2024)

**Topics Covered:**
*   Backtracking algorithm examples (Rat in Maze, N-Queens, Sudoku Solver).
*   General backtracking approach.
*   Sudoku Solver implementation details.

**Detailed Notes:**

1.  **Backtracking:** A general algorithmic technique for solving problems recursively by trying to build a solution incrementally, one piece at a time, removing those solutions ("backtracking") that fail to satisfy the constraints of the problem at any point in time.
2.  **Common Problems:**
    *   **Rat in a Maze:** Find a path from start to end in a grid, avoiding obstacles.
    *   **N-Queens:** Place N chess queens on an N×N chessboard so that no two queens threaten each other.
    *   **Sudoku Solver:** Fill a 9×9 grid so that each column, each row, and each of the nine 3×3 subgrids contain all digits from 1 to 9.
    *   **Knight's Tour:** Find a sequence of moves of a knight on a chessboard such that the knight visits every square exactly once.
3.  **General Backtracking Algorithm:**
    ```
    function solve(problem_state):
        if problem_state is a final solution:
            return true // or print/store solution

        for each possible choice from current state:
            if choice is valid (isSafe):
                apply choice to problem_state
                if solve(new_problem_state) returns true:
                    return true // Found solution down this path
                undo choice (backtrack) // Remove choice from problem_state

        return false // No solution found from this state
    ```
4.  **Sudoku Solver Implementation:**
    *   **Representation:** Use a 2D array or `vector<vector<int>>` (e.g., 9x9) to represent the board. Use 0 or '.' to represent empty cells.
    *   **`solveSudoku` function (recursive):**
        *   **Base Case:** Find the next empty cell. If no empty cell is found, the board is full and solved, return `true`.
        *   **Recursive Step:** For the found empty cell (row, col):
            *   Iterate through numbers `num` from 1 to 9.
            *   Check if placing `num` at `(row, col)` is valid using `isSafe(board, row, col, num)`.
            *   If `isSafe`:
                *   Place the number: `board[row][col] = num`.
                *   Recursively call `solveSudoku()`.
                *   If the recursive call returns `true`, it means a solution was found down that path, so return `true`.
                *   If the recursive call returns `false`, it means placing `num` didn't lead to a solution. **Backtrack:** Reset the cell `board[row][col] = 0` and try the next number.
        *   If no number from 1-9 works for the current empty cell, return `false` (triggering backtracking in the caller).
    *   **`isSafe` function:** Checks three conditions for placing `num` at `(row, col)`:
        1.  **Row Check:** Iterate through the `row` to see if `num` already exists.
        2.  **Column Check:** Iterate through the `col` to see if `num` already exists.
        3.  **3x3 Box Check:** Determine the starting row and column of the 3x3 box containing `(row, col)`. Iterate through the 3x3 box to see if `num` already exists.
        *   Return `true` only if `num` is not found in the row, column, AND the 3x3 box. Otherwise, return `false`.

**Code Snippet (Sudoku Solver):**

```cpp
#include <iostream>
#include <vector>

#define N 9 // Size of the Sudoku grid

// Function to print the Sudoku grid
void printGrid(const std::vector<std::vector<int>>& grid) {
    for (int row = 0; row < N; row++) {
        for (int col = 0; col < N; col++) {
            std::cout << grid[row][col] << " ";
        }
        std::cout << std::endl;
    }
}

// Function to check if it's safe to place 'num' at grid[row][col]
bool isSafe(const std::vector<std::vector<int>>& grid, int row, int col, int num) {
    // Check if 'num' is not already present in current row, current column, and current 3x3 box

    // 1. Check row
    for (int c = 0; c < N; c++) {
        if (grid[row][c] == num) {
            return false;
        }
    }

    // 2. Check column
    for (int r = 0; r < N; r++) {
        if (grid[r][col] == num) {
            return false;
        }
    }

    // 3. Check 3x3 box
    int boxStartRow = row - row % 3;
    int boxStartCol = col - col % 3;
    for (int r = 0; r < 3; r++) {
        for (int c = 0; c < 3; c++) {
            if (grid[r + boxStartRow][c + boxStartCol] == num) {
                return false;
            }
        }
    }

    // If safe in all checks
    return true;
}

// Function to find an empty location (returns true if found, updates row and col)
bool findEmptyLocation(const std::vector<std::vector<int>>& grid, int& row, int& col) {
    for (row = 0; row < N; row++) {
        for (col = 0; col < N; col++) {
            if (grid[row][col] == 0) { // 0 indicates empty cell
                return true;
            }
        }
    }
    return false; // No empty location found
}

// Main recursive backtracking function to solve Sudoku
bool solveSudoku(std::vector<std::vector<int>>& grid) {
    int row, col;

    // Base Case: If there is no empty location, we are done
    if (!findEmptyLocation(grid, row, col)) {
        return true; // Success!
    }

    // Recursive Step: Try numbers 1-9 for the empty location
    for (int num = 1; num <= 9; num++) {
        // Check if it's safe to place the number
        if (isSafe(grid, row, col, num)) {
            // Make tentative assignment
            grid[row][col] = num;

            // Recursively call solve for the next state
            if (solveSudoku(grid)) {
                return true; // If successful, propagate true up
            }

            // Failure, undo & try next number (Backtrack)
            grid[row][col] = 0;
        }
    }

    // This triggers backtracking
    return false; // No number worked for this cell
}

int main() {
    // Example Sudoku grid (0 represents empty cells)
    std::vector<std::vector<int>> grid = {
        {5, 3, 0, 0, 7, 0, 0, 0, 0},
        {6, 0, 0, 1, 9, 5, 0, 0, 0},
        {0, 9, 8, 0, 0, 0, 0, 6, 0},
        {8, 0, 0, 0, 6, 0, 0, 0, 3},
        {4, 0, 0, 8, 0, 3, 0, 0, 1},
        {7, 0, 0, 0, 2, 0, 0, 0, 6},
        {0, 6, 0, 0, 0, 0, 2, 8, 0},
        {0, 0, 0, 4, 1, 9, 0, 0, 5},
        {0, 0, 0, 0, 8, 0, 0, 7, 9}
    };

    std::cout << "Unsolved Sudoku:" << std::endl;
    printGrid(grid);
    std::cout << "\nSolving...\n" << std::endl;

    if (solveSudoku(grid)) {
        std::cout << "Solved Sudoku:" << std::endl;
        printGrid(grid);
    } else {
        std::cout << "No solution exists for the given Sudoku." << std::endl;
    }

    return 0;
}
```

---
