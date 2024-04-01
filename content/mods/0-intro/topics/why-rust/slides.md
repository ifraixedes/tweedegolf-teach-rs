---
layout: section
---

# Why learn Rust?

---
layout: default
---
# How to choose a language

What characteristics do you want?

<v-click>1. Efficiency</v-click><br/>
<v-click>2. Safety</v-click><br/>
<v-click>3. Elegance</v-click><br/>
<v-click>4. Practical relevance</v-click><br/>
<br/>
<v-click>Most languages provide 2 of the above characteristics, whereas Rust offers a balance of all them</v-click>

<!-- 
Try asking the audience first

[click][click][click][click]

Let's give some detail in how Rust provides them
-->

---
layout: default
---
# Rust's characteristics

## Efficiency & portability

<v-click>- It's a compiled language, not interpreted</v-click><br/>
<v-click>- No garbage collector</v-click><br/>
<v-click>- The compiler (i.e. `rustc`) uses LLVM as its backend</v-click><br/><br/>

<v-click><b>Conclusion</b>: Its performance is equivalent to C and C++</v-click>

<!--
[click]
This means not having to pay the penalty of translating the source code to machine code on each run because it generates a binary file (i.e. zeros and ones) which is execute directly by the target architecture and operative system.

[click]
Apart it doesn't require a garbage collector, hence, there isn't any sub-process in the runtime that executes aside with the program / application. No sub-process means no using extra resources when running the program / application.

[click]
This means that when you compile Rust code, it first gets compiled into LLVM's intermediate representation (IR), a low-level programming language that is platform-independent. LLVM is renowned for its powerful optimization capabilities. It can perform a wide range of optimizations on the IR code, such as function inlining, loop unrolling, and dead code elimination. These optimizations can significantly improve the performance of the compiled code

LLVM supports a vast array of target platforms, including various architectures and operating systems. This means that Rust can compile to a wide range of platforms, making it highly portable with minimal changes to the source code.

LLVM is continuously updated with new optimizations and support for new hardware architectures. By leveraging LLVM, Rust can benefit from these improvements, ensuring that Rust programs remain performant and up-to-date with the latest hardware technologies.


[click]
It achieves this through its zero-cost abstractions, which means that you don't pay (in terms of performance) for the high-level features that make programming in Rust safer and more productive. Moreover nowadays, performance isn't just about running fast, it's also about consuming less energy to contribute reduce the CO2 emissions.
-->

---
layout: default
---
# Rust's characteristics

## Safety
<v-click>- Strong type system</v-click><br/>
<v-click>- Explicit errors instead of exceptions</v-click><br/>
<v-click>- Explicit initialization</v-click><br/>
<v-click>- Tracking of values' lifetimes</v-click><br/><br/>

<v-click><b>If it compiles, it is more often free of this "programming bugs"!!!</b></v-click>

<!--
[click]
With its strong type system, Rust forces the developer to

[click]
Handle errors through a specific return type that allows to access the result value when there isn't an error or to the error when there is one.

[click]
Variables must be initialized before use. This means that your program won't crash because you declared a variable without assigning it a value and because there aren't implicit values, it's clear when reading the code what value they have assigned when before use without requiring to remember which are the default values for each different types.

[click]
Its ownership model and borrowing system are designed to eliminate common programming errors like null pointer dereferencing, double free, and data races at compile time.

[click]
All of them make Rust a safe language, where many errors are caught before the code is even run.

Note the double quote in "programming bugs"; that's to mark the difference with "business logic bugs", Rust won't prevent any of them.

-->

---
layout: default
---
# Rust's characteristics

## Elegance
<v-click>- Data types can capture many problem domains</v-click><br/>
<v-click>- Orthogonal, expression-oriented language</v-click><br/>
<v-click>- Combine declarative and imperative paradigms</v-click><br/>
<v-click>- Concise syntax instead of boilerplate</v-click><br/>
<v-click>- Toolchain that suggests improvements to your code</v-click><br/>
<v-click>- Documentation</v-click><br/>

<!--
[click]
Rust's type system is powerful and flexible enough to model complex data structures and behaviors. By using Rust's enums, structs, traits, and other type constructs, developers can precisely define the shape and behavior of data, making the code more expressive and easier to understand.

[click]
Rust's features and constructs are designed to work well together in a consistent and predictable manner. It's also expression-oriented, meaning that Rust values expressions over statements. In Rust, almost everything is an expression, which can return a value and can be used in places where statements are expected. Some people consider this design choice produce more concise and readable code, as it allows for the use of powerful abstractions and patterns.

[click]
Rust supports both declarative and imperative programming paradigms.

Declarative programming focuses on what the program should accomplish without specifying how to achieve it.
Imperative programming, on the other hand, focuses on how to achieve a result step by step.

Rust's support for both paradigms allows developers to choose the most appropriate approach for their problem, leading to the possibility to produce more flexible and maintainable code. NOTE, this is double-edged sword because it isn't always easy to see which approach will lead to more readable and maintainable code and people with strong preference to one of the paradigms can lead to one of them that produced the opposite result.

[click]
Rust's syntax is designed to be concise and expressive, reducing the amount of boilerplate code required. This is achieved through features like pattern matching, type inference, and the use of macros.

The goal is to make the code more readable and maintainable, allowing developers to focus on the problem domain rather than the syntax. However, macros aren't very straight forward to develop, so whereas the macro consumers may have less boilerplate code, the logic behind the macro can be hard to understand, provoking that the macros to be hard to maintain.

[click]
Rust's toolchain, including the compiler (rustc) and the package manager (cargo), is designed to be helpful and informative. The compiler provides detailed error messages and warnings, often suggesting fixes or improvements to your code. This feature helps developers write better code more quickly, as they can leverage the compiler's expertise to catch and correct errors early in the development process.

[click]
Rust has a great official documentation. It has an official on-line free book and the standard library is well documented.

Rust has a kind of code comments that are to document the code, they support Markdown syntax, and allow to write examples which show how to use the code and they run as tests. rustdoc (a tool distributed with Rust) that generates HTML format from all this codes and examples. https://docs.rs publishes the crates documentation automatically when a new crate is published or an existing one is updated.
-->

---
layout: default
---
# Rust is practical

<v-click>- Supported on many platforms</v-click><br/>
<v-click>- Can interface with legacy C code</v-click><br/>
<v-click>- Active user base maintains a healthy ecosystem</v-click><br/>
<v-click>- Everyday there are more companies adopting it (e.g. Microsoft, Amazon, Google, etc.)</v-click><br/><br/>

<v-click><b>In summary</b>: Rust is gaining popularity in various domains, including web development, systems programming, and embedded systems</v-click>

<!--
[click]
Rust's cross-platform support is one of its strengths. It can compile to a wide range of platforms, including various operating systems (Windows, macOS, Linux, etc.) and architectures (x86, ARM, MIPS, etc.). This portability makes Rust a versatile choice for developing applications that need to run on multiple platforms without significant modifications

[click]
Rust provides robust mechanisms for interfacing with existing C libraries and code-bases. Rust's Foreign Function Interface (FFI) allows it to call C functions and use C libraries directly, making it easier to integrate Rust into existing systems that are written in C. This capability is particularly valuable for systems programming, embedded systems, and other areas where legacy code-bases are common.

[click]
There are many developers contributing to the language, its libraries, and tools. This activity leads to a rapid development of new libraries, tools, and best practices, as well as quick responses to bugs and feature requests. An active ecosystem also means that there's a wealth of resources available for learning and troubleshooting.

[click]

[click]
Its performance and safety features make it a practical choice for a wide range of applications, from creating web servers to writing operating systems.

-->