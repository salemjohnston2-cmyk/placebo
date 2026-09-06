Placebo

«Understand what you're doing, not how it works.»

Placebo is an experimental programming language designed around expressing intent rather than implementation mechanics.

It currently runs through a browser-based interpreter written in JavaScript.

Status: Experimental — v0.1.0

The language, syntax, runtime behavior, and architecture are still evolving.

---

What is Placebo?

Most programming languages expose a large amount of implementation detail through their syntax.

Placebo explores a different direction:

«What if writing a program could feel more like describing what you want the computer to do?»

Placebo is an experiment in that idea.

It has its own lexer, parser, interpreter, runtime, built-in functions, control flow, functions, collections, error handling, and interactive browser environment.

It is not intended to replace existing languages. The purpose of the project is to explore a different programming model and see how far it can go.

---

Example

A simple Placebo program:

store total = 0

loop 10 times
    total = total + 1
end

output total

Placebo also supports functions:

function greet(name)
    output "Hello, (name)"
end

greet("world")

The repository contains larger examples, including an implementation of Conway's Game of Life.

---

Features

The current interpreter includes:

- Variables
- Numbers
- Strings
- Lists
- Dictionaries
- Arithmetic
- Comparisons
- Boolean logic
- Conditional statements
- "while" loops
- Iteration
- Repetition
- Functions
- Closures
- Lambdas
- Multiple return values
- Error handling
- Input
- String interpolation
- List and dictionary operations
- File-like browser storage
- Built-in utility functions

The language is implemented with:

Source
  ↓
Lexer
  ↓
Parser
  ↓
Interpreter
  ↓
Runtime

---

Try it

The current version is designed to run directly in a web browser.

Open "placebo.html" and use the built-in playground.

No build system is required for the current experimental version.

---

Examples

Hello World

See:

examples/hello.placebo

Oracle

An interactive example demonstrating input, functions, conditions, and randomness:

examples/oracle.placebo

Game of Life

A larger program demonstrating that Placebo can express a non-trivial algorithm:

examples/game-of-life.placebo

---

Project Structure

placebo/
├── placebo.html
├── examples/
│   ├── hello.placebo
│   ├── oracle.placebo
│   └── game-of-life.placebo
├── docs/
│   └── language.md
├── README.md
├── LICENSE
└── .gitignore

The current implementation intentionally remains simple. The interpreter and browser playground are currently contained in a single HTML file.

The architecture is expected to evolve as the language becomes more stable.

---

Language Documentation

The current language reference is available in:

docs/language.md

The documentation describes the behavior of the current implementation rather than an idealized future version of Placebo.

---

Current Status

Placebo is experimental software.

The language is usable, but its semantics are not yet considered frozen.

Areas that will evolve include:

- Interpreter/runtime architecture
- Assignment semantics
- Mutation semantics
- Loop scoping
- Dictionary behavior
- Error reporting
- Asynchronous operations
- Module/loading behavior
- Separation of the language engine from the browser environment

These are tracked as development issues rather than being hidden behind a claim of completeness.

---

Roadmap

v0.1 — Experimental

- Initial interpreter
- Browser playground
- Core language
- Functions and lambdas
- Collections
- Control flow
- Error handling
- Built-in functions
- Example programs

v0.2 — Language Stability

- Formalize language semantics
- Improve runtime errors
- Clarify assignment and mutation
- Improve loop scoping
- Improve dictionary semantics
- Add language conformance tests

v0.3 — Standalone Runtime

- Separate interpreter from browser UI
- Create a standalone runtime
- Introduce a command-line interface

Future

Potential future work includes:

- Standard library
- Modules
- Package management
- Better I/O
- HTTP capabilities
- Editor support
- Syntax highlighting
- Language server support

The roadmap is intentionally flexible. Placebo is an exploration, and the language will evolve based on what is learned from building and using it.

---

Contributing

Placebo is an experimental project and feedback is welcome.

Useful contributions include:

- Finding language inconsistencies
- Reporting bugs
- Writing example programs
- Suggesting improvements to the language
- Improving documentation
- Adding tests
- Improving the interpreter

Before proposing a large language feature, please open an issue and explain the problem the feature is intended to solve.

---

Philosophy

Placebo is an experiment in programming language design.

The goal is not to hide computation or make programming magical.

The goal is to explore whether a programming language can make the intent of a program easier to understand without removing the power of programming itself.

---

License

Placebo is released under the MIT License.
