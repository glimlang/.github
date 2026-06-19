<div align="center">

<img src="https://github.com/user-attachments/assets/0cbb8d29-f729-4ae8-b8ed-26ad09a556d8" width="160" height="160" alt="GlimLang Gecko Mascot" />

# GLIM | LANG

**A tiny, expressive programming language written in pure Python.**

[![PyPI](https://img.shields.io/pypi/v/glimlang?color=0ABFA3&label=PyPI&style=flat-square)](https://pypi.org/project/glimlang)
[![License](https://img.shields.io/badge/License-Apache%202.0-0ABFA3?style=flat-square)](https://github.com/glimlang/glimlang/blob/main/LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8%2B-0ABFA3?style=flat-square&logo=python&logoColor=white)](https://python.org)

[![PyPI Downloads](https://img.shields.io/pypi/dm/glimlang?color=39D353&label=Downloads&style=flat-square)](https://pypi.org/project/glimlang)
[![Version](https://img.shields.io/badge/stable-v1.2.2-39D353?style=flat-square)](https://github.com/glimlang/glimlang/releases)

</div>

---

## 🦎 What is GlimLang?

GlimLang is a clean, friendly, and highly readable scripting language designed for clear syntax, rich built-ins, and fast prototyping. It features a complete hand-written pipeline — Lexical Scanner → Pratt Parser → Abstract Syntax Tree → Tree-Walking Interpreter — entirely in pure Python with zero external dependencies.

> **Designed for Developers:** GlimLang strips away the complex, low-level optimization layers of standard production runtimes. It provides a fully transparent, highly readable codebase where you can observe exactly how scoping, classes, closures, and pattern matching run under the hood.

---

## ⚡ Install

```bash
pip install glimlang==1.2.2
```

Verify installation:

```bash
gl version
# GlimLang v1.2.2
```

Run your first script:

```bash
gl run hello.glim
# Hello, GlimLang world! ✓
```

---

## ✨ Features

| Feature | Description |
|---|---|
| 🔀 **Pattern Matching** | Robust `match` with pipes `\|`, wildcards `_`, and multi-arm blocks |
| 🏗️ **OOP Classes** | Blueprint templates, custom constructors, self-referencing properties |
| ⚙️ **Zero Dependencies** | Pure Python 3.8+ — no external libraries required |
| ⚡ **40+ Built-ins** | Rich standard library out of the box |
| 🔍 **Pratt Parser** | Hand-written operator-precedence AST builder |
| 🧠 **Lexical Closures** | First-class functions with dynamic environment scope maps |
| 🧪 **Try/Catch Diagnostics** | Deep exception frames with positional line and column error mapping |
| 🔁 **REPL** | Interactive Read-Eval-Print Loop terminal session via `gl repl` |

---

## 🚀 Quick Examples

### Hello World

```glim
print "Hello, GlimLang world!"
```

### Variables & Types

```glim
let name = "Glim"
let version = 1.2
let active = true
print f"Welcome to {name} v{version}"
```

### Pattern Matching

```glim
let day = "Sat"

match day {
  "Sat" | "Sun" => print "Weekend!"
  "Mon"         => print "Back to work."
  _             => print "Midweek grind."
}
```

### Classes & OOP

```glim
class Greeter {
  def init(name) {
    self.name = name
  }
  def greet(user) {
    print f"Hello, {user}! I am {self.name}."
  }
}

let bot = Greeter("GlimBot")
bot.greet("Developer")
# Output: Hello, Developer! I am GlimBot.
```

### Functions & Closures

```glim
def make_counter() {
  let count = 0
  fn increment() {
    count = count + 1
    return count
  }
  return increment
}

let counter = make_counter()
print counter()  # 1
print counter()  # 2
print counter()  # 3
```

### Try / Catch

```glim
try {
  let result = 10 / 0
} catch(e) {
  print f"Error caught: {e}"
}
```

---

## 🏗️ Compiler Pipeline

```
Source Code
    ↓
Lexical Scanner      — Tokenizes source character-by-character
    ↓
Pratt Parser         — Builds AST using operator-precedence grammar
    ↓
Abstract Syntax Tree (AST)
    ↓
Tree-Walking Interpreter  — Executes AST nodes recursively
    ↓
Output
```

Every stage is hand-written in readable Python — no generated parsers, no external lexer tools.

---

## 📖 CLI Reference

| Command | Description |
|---|---|
| `gl run <file>` | Execute a `.glim` script file |
| `gl repl` | Launch interactive REPL session |
| `gl version` | Print installed GlimLang version |
| `gl help` | Show all available CLI commands |

---

## 📦 Requirements

- Python **3.8 or higher**
- No external dependencies

---

## 📄 License

GlimLang is dual-licensed under the **Apache License 2.0**.

You may use this project under the terms of either license at your option.


---

## 🤝 Contributing (soon Avaliable Repo)

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/amazing-feature`
3. Commit your changes: `git commit -m 'Add amazing feature'`
4. Push to the branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

---

## 🌐 Links

<div align="center">

🌐 [glimlang.org](https://glimlang.org) &nbsp;·&nbsp;
📖 [Docs](https://glimlang.org/docs) &nbsp;·&nbsp;
💬 [Discord](https://discord.gg/glimlang) &nbsp;·&nbsp;
📦 [PyPI](https://pypi.org/project/glimlang) &nbsp;·&nbsp;
⭐ [Star on GitHub](https://github.com/glimlang/glimlang)

</div>

---

<div align="center">

Made with 🦎 by the GlimLang Community

</div>
