<div align="center">

<img src="https://yeditepe.edu.tr/themes/custom/yeditepe/logo.svg" alt="Yeditepe University Logo" width="120"/>

# CSE 211 — Data Structures
## Term Project

<br>

<img src="https://img.shields.io/badge/Yeditepe-University-1a5276?style=for-the-badge" alt="Yeditepe University"/>
<img src="https://img.shields.io/badge/Department-Computer_Science_&_Engineering-2980b9?style=for-the-badge" alt="CSE"/>
<img src="https://img.shields.io/badge/Semester-2025--2026_Fall-27ae60?style=for-the-badge" alt="Fall 2025-2026"/>

<br><br>

**Instructor:** Batuhan Edgüer

<br>

---

### Navigation

[**Download**](#-download-your-project) ·
[**Requirements**](#-hard-requirements) ·
[**Structure**](#-project-structure) ·
[**Technical**](#-technical-requirements) ·
[**STL Rules**](#-stl-restrictions) ·
[**Testing**](#-testing-requirements) ·
[**UML**](#-uml--documentation) ·
[**Mistakes**](#-common-mistakes-to-avoid) ·
[**Submit**](#-submission-format) ·
[**Checklist**](#-pre-submission-checklist) ·
[**Tools**](#%EF%B8%8F-tools--libraries)

---

</div>

<br>

## Table of Contents

<details open>
<summary><strong>Expand / Collapse</strong></summary>

<br>

|    § | Section                                                | Description                       |
| ---: | :----------------------------------------------------- | :-------------------------------- |
|    1 | [Download Your Project](#-download-your-project)       | Get your assignment files         |
|    2 | [Quick Start](#-quick-start)                           | Get started in 4 steps            |
|    3 | [Hard Requirements](#-hard-requirements)               | Non-negotiable requirements       |
|    4 | [Project Structure](#-project-structure)               | Directory organization            |
|    5 | [Technical Requirements](#-technical-requirements)     | Language, compiler, build targets |
|    6 | [STL Restrictions](#-stl-restrictions)                 | What you can and cannot use       |
|    7 | [Testing Requirements](#-testing-requirements)         | Test coverage expectations        |
|    8 | [UML & Documentation](#-uml--documentation)            | Required diagrams                 |
|    9 | [Common Mistakes to Avoid](#-common-mistakes-to-avoid) | Critical errors to prevent        |
|   10 | [Submission Format](#-submission-format)               | How to submit your work           |
|   11 | [Pre-Submission Checklist](#-pre-submission-checklist) | Final verification                |
|   12 | [Tools & Libraries](#%EF%B8%8F-tools--libraries)       | Recommended resources             |

</details>

<br>

---

<br>

## ↓ Download Your Project

<div align="center">

### [► Go to Releases Page](../../releases)

</div>

<br>

We have split the project into **two document types**:

| Document          | Description                                                                                                   |    Priority    |
| :---------------- | :------------------------------------------------------------------------------------------------------------ | :------------: |
| **`base.pdf`**    | General specification with shared requirements, data formats, and technical constraints. Applies to everyone. | **Read First** |
| **`PROJ-XX.pdf`** | Your specific assignment describing the unique problem your group must solve.                                 |  Read Second   |

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

## ► Quick Start

```
1. Download base.pdf and read it thoroughly (SERIOUSLY!)
2. Download your assigned PROJ-XX.pdf
3. Set up your project using the structure below
4. Implement, test, document, present!
```

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

## ⚠ Hard Requirements

> [!CAUTION]
> **Missing any of these requirements = significant point loss!**

|       | Requirement                | Description                                                                          |
| :---: | :------------------------- | :----------------------------------------------------------------------------------- |
|   ☐   | **Custom Data Structures** | Implement your own — `std::vector`, `std::map`, `std::list` etc. are **NOT allowed** |
|   ☐   | **Build System**           | Makefile or CMake with `make`, `make test`, `make clean` targets                     |
|   ☐   | **Data Directory**         | Read input from `data/` folder with multiple test files                              |
|   ☐   | **Visual Frontend**        | GUI or TUI that visualizes your solution                                             |
|   ☐   | **Testing**                | Unit tests + edge cases + integration tests                                          |
|   ☐   | **UML Diagrams**           | Class diagram + one behavioral diagram (sequence, activity, etc.)                    |
|   ☐   | **Modular Code**           | Separate headers/source files — no 1000-line monster files                           |
|   ☐   | **Presentation**           | 15-minute demo + code walkthrough + Q&A                                              |

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

## ◈ Project Structure

<table>
<tr>
<td width="50%">

### Source Code

```
project/
│
├── include/
│   ├── data_structures/    ← Custom DS headers
│   ├── core/               ← Core logic headers
│   └── utils/              ← Utility headers
│
├── src/
│   ├── data_structures/    ← DS implementations
│   ├── core/               ← Core logic
│   ├── utils/              ← Utilities
│   └── main.cpp            ← Entry point
│
└── frontend/               ← GUI/TUI code
```

</td>
<td width="50%">

### Testing & Data

```
project/
│
├── tests/
│   ├── unit/               ← Unit tests
│   ├── integration/        ← Integration tests
│   └── edge_cases/         ← Boundary tests
│
├── data/
│   ├── input_default.json  ← Default input
│   ├── edge_case_*.json    ← Edge cases
│   └── expected_*.json     ← Expected outputs
│
└── docs/
    └── uml/                ← UML diagrams
```

</td>
</tr>
<tr>
<td colspan="2">

### Root Files

| File            | Purpose                            |
| :-------------- | :--------------------------------- |
| `Makefile`      | Build system (or `CMakeLists.txt`) |
| `.clang-format` | Code formatting configuration      |
| `README.md`     | Project documentation              |
| `Doxyfile`      | Documentation generator config     |

</td>
</tr>
</table>

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

## ⚙ Technical Requirements

### Language & Compiler

| Requirement   | Specification                                                         |
| :------------ | :-------------------------------------------------------------------- |
| **Language**  | C++17 or later                                                        |
| **Compiler**  | [`g++`](https://gcc.gnu.org/) or [`clang++`](https://clang.llvm.org/) |
| **Platforms** | Linux (Ubuntu 20.04+) · Windows                                       |

### Required Build Targets

| Target       | Description            |
| :----------- | :--------------------- |
| `make`       | Build the project      |
| `make run`   | Build and run          |
| `make test`  | Run all tests          |
| `make clean` | Remove build artifacts |
| `make deps`  | Install dependencies   |

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

## ⊘ STL Restrictions

<div align="center">

| ✗ **NOT Allowed**     | ✓ **Allowed**                         |
| :-------------------- | :------------------------------------ |
| `std::vector`         | `std::string`                         |
| `std::list`           | `std::fstream` / `std::iostream`      |
| `std::map`            | `std::unique_ptr` / `std::shared_ptr` |
| `std::set`            | `<algorithm>` on primitive arrays     |
| `std::unordered_map`  | `<functional>`                        |
| `std::queue`          |                                       |
| `std::stack`          |                                       |
| `std::deque`          |                                       |
| `std::array`          |                                       |
| `std::priority_queue` |                                       |

</div>

<br>

> [!IMPORTANT]
> **All custom data structures must use pointer-based implementation.**
> Array-based implementations are NOT allowed.

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

## ⧩ Testing Requirements

Your tests should cover:

| Category         | Test Cases                                     |
| :--------------- | :--------------------------------------------- |
| **Construction** | Default constructor, parameterized constructor |
| **Insertion**    | Beginning, middle, end, duplicate handling     |
| **Deletion**     | Beginning, middle, end, non-existent element   |
| **Search**       | Existing element, non-existent element         |
| **Edge Cases**   | Empty structure, single element, full capacity |
| **Boundary**     | Maximum size, minimum values, overflow         |

<details>
<summary><strong>► Test Organization Structure</strong></summary>

<br>

```
tests/
├── test_main.cpp              ← Test runner
├── unit/
│   ├── test_data_structures.cpp
│   ├── test_algorithms.cpp
│   └── test_utils.cpp
├── integration/
│   ├── test_workflow.cpp
│   └── test_io.cpp
├── edge_cases/
│   ├── test_empty.cpp
│   ├── test_single.cpp
│   └── test_limits.cpp
└── fixtures/
    └── test_helpers.hpp
```

</details>

<details>
<summary><strong>► Memory Testing with Valgrind</strong></summary>

<br>

```bash
valgrind --leak-check=full --show-leak-kinds=all ./build/bin/tests
```

Expected clean output:
```
All heap blocks were freed -- no leaks are possible
```

</details>

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

## △ UML & Documentation

### Required Diagrams

| Diagram               | Purpose                                             |  Required   |
| :-------------------- | :-------------------------------------------------- | :---------: |
| **Class Diagram**     | Shows structure, attributes, methods, relationships |    ✓ Yes    |
| **Sequence Diagram**  | Shows object interactions over time                 | Recommended |
| **Component Diagram** | Shows high-level module organization                |  Optional   |

### UML Notation Reference

| Relationship             | Notation                         |
| :----------------------- | :------------------------------- |
| Inheritance              | Solid line with hollow triangle  |
| Interface Implementation | Dashed line with hollow triangle |
| Composition              | Solid line with filled diamond   |
| Aggregation              | Solid line with hollow diamond   |
| Association              | Plain solid line                 |
| Dependency               | Dashed line with arrow           |

<details>
<summary><strong>► UML Tools</strong></summary>

<br>

| Tool         | Type                                 | Link                                          |
| :----------- | :----------------------------------- | :-------------------------------------------- |
| **PlantUML** | Text-based, version control friendly | [plantuml.com](https://plantuml.com/)         |
| **Draw.io**  | Free web-based editor                | [draw.io](https://app.diagrams.net/)          |
| **Mermaid**  | Markdown-integrated                  | [mermaid.js.org](https://mermaid.js.org/)     |
| **Umbrello** | Open source desktop app              | [umbrello.kde.org](https://umbrello.kde.org/) |
| **StarUML**  | Professional modeling tool           | [staruml.io](https://staruml.io/)             |

</details>

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

## ✗ Common Mistakes to Avoid

> [!WARNING]
> **These mistakes will cost you significant points!**

| ✗ Mistake                                     | ✓ Solution                                    |
| :-------------------------------------------- | :-------------------------------------------- |
| Using `std::vector` or other STL containers   | Implement your own data structures            |
| No Makefile (we can't build = we can't grade) | Include `Makefile` or `CMakeLists.txt`        |
| Hardcoded paths or no `data/` directory       | Use relative paths, read from `data/`         |
| No tests or only testing "happy path"         | Write unit, integration, and edge case tests  |
| All code in one giant file                    | Modularize: separate headers and source files |
| Frontend that doesn't visualize the solution  | Actually show the algorithm/data in action    |

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

## ◰ Submission Format

<div align="center">

```
GroupID_ProblemNumber.zip
```

**Example:** `Group05_01.zip`

</div>

<br>

> [!IMPORTANT]
> **Submit source code only!** Do NOT include:
> - Compiled binaries (`*.o`, `*.exe`, `*.so`)
> - Build directories (`build/`, `bin/`)
> - IDE files (`.idea/`, `.vscode/`)
> - Version control (`.git/`)
> - Temporary files (`*.tmp`, `*.log`)
> - External libraries (fetch via `make deps`)

### Fresh Build Test

Before submitting, extract your zip to a new directory and verify:

```bash
unzip Group05_01.zip -d /tmp/test
cd /tmp/test/Group05_01
make deps
make
make test
make run
```

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

## ✓ Pre-Submission Checklist

<div align="center">

|       | Category    | Item                                                                             |
| :---: | :---------- | :------------------------------------------------------------------------------- |
|   ☐   | **Build**   | Code compiles without errors                                                     |
|   ☐   | **Build**   | No compiler warnings                                                             |
|   ☐   | **Testing** | All tests pass                                                                   |
|   ☐   | **Testing** | No memory leaks ([Valgrind](https://valgrind.org/) clean)                        |
|   ☐   | **Code**    | Code is formatted ([clang-format](https://clang.llvm.org/docs/ClangFormat.html)) |
|   ☐   | **Code**    | No prohibited STL containers                                                     |
|   ☐   | **Code**    | Minimum two custom data structures                                               |
|   ☐   | **Code**    | Pointer-based implementation                                                     |
|   ☐   | **Docs**    | Documentation generates ([Doxygen](https://www.doxygen.nl/))                     |
|   ☐   | **Docs**    | README is complete                                                               |
|   ☐   | **Docs**    | UML diagrams included                                                            |
|   ☐   | **Docs**    | Presentation slides included                                                     |
|   ☐   | **App**     | Frontend works                                                                   |
|   ☐   | **App**     | Data files included in `data/`                                                   |

</div>

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

## ⚒️ Tools & Libraries

### Core Tools

| Tool             | Purpose                     | Link                                                                                 |
| :--------------- | :-------------------------- | :----------------------------------------------------------------------------------- |
| **GNU Make**     | Build automation            | [gnu.org/software/make](https://www.gnu.org/software/make/)                          |
| **CMake**        | Cross-platform build system | [cmake.org](https://cmake.org/)                                                      |
| **GCC**          | GNU Compiler Collection     | [gcc.gnu.org](https://gcc.gnu.org/)                                                  |
| **Clang**        | LLVM C++ compiler           | [clang.llvm.org](https://clang.llvm.org/)                                            |
| **clang-format** | Code formatter              | [clang.llvm.org/docs/ClangFormat.html](https://clang.llvm.org/docs/ClangFormat.html) |
| **Doxygen**      | Documentation generator     | [doxygen.nl](https://www.doxygen.nl/)                                                |
| **Valgrind**     | Memory debugger             | [valgrind.org](https://valgrind.org/)                                                |

### Frontend Frameworks

<details>
<summary><strong>► C++ GUI Libraries</strong></summary>

<br>

| Framework      | Description                  | Link                                                         |
| :------------- | :--------------------------- | :----------------------------------------------------------- |
| **Qt**         | Cross-platform, feature-rich | [qt.io](https://www.qt.io/)                                  |
| **Dear ImGui** | Immediate mode GUI           | [github.com/ocornut/imgui](https://github.com/ocornut/imgui) |
| **wxWidgets**  | Native look-and-feel         | [wxwidgets.org](https://www.wxwidgets.org/)                  |
| **FLTK**       | Lightweight, fast            | [fltk.org](https://www.fltk.org/)                            |
| **GTKmm**      | C++ bindings for GTK         | [gtkmm.org](https://www.gtkmm.org/)                          |
| **Nana**       | Modern C++ GUI library       | [github.com/cnjinhao/nana](https://github.com/cnjinhao/nana) |

</details>

<details>
<summary><strong>► Terminal UI (TUI) Libraries</strong></summary>

<br>

| Library      | Description              | Link                                                                       |
| :----------- | :----------------------- | :------------------------------------------------------------------------- |
| **ncurses**  | Classic terminal UI      | [invisible-island.net/ncurses](https://invisible-island.net/ncurses/)      |
| **FTXUI**    | Modern C++ TUI           | [github.com/ArthurSonzogni/FTXUI](https://github.com/ArthurSonzogni/FTXUI) |
| **termbox2** | Minimal terminal library | [github.com/termbox/termbox2](https://github.com/termbox/termbox2)         |

</details>

<details>
<summary><strong>► Web Interface (REST API)</strong></summary>

<br>

| Framework       | Description                     | Link                                                                           |
| :-------------- | :------------------------------ | :----------------------------------------------------------------------------- |
| **Crow**        | Fast micro web framework        | [crowcpp.org](https://crowcpp.org/)                                            |
| **Drogon**      | High-performance HTTP framework | [github.com/drogonframework/drogon](https://github.com/drogonframework/drogon) |
| **cpp-httplib** | Single-header HTTP library      | [github.com/yhirose/cpp-httplib](https://github.com/yhirose/cpp-httplib)       |
| **Pistache**    | Modern HTTP framework           | [pistacheio.github.io/pistache](http://pistacheio.github.io/pistache/)         |

</details>

<details>
<summary><strong>► Desktop/Hybrid Apps</strong></summary>

<br>

| Framework        | Description                           | Link                                            |
| :--------------- | :------------------------------------ | :---------------------------------------------- |
| **Electron**     | Web tech for desktop (with C++ addon) | [electronjs.org](https://www.electronjs.org/)   |
| **Tauri**        | Lightweight alternative to Electron   | [tauri.app](https://tauri.app/)                 |
| **Neutralinojs** | Lightweight cross-platform apps       | [neutralino.js.org](https://neutralino.js.org/) |

</details>

### C++/Python Integration

| Tool             | Description                              | Link                                                                                   |
| :--------------- | :--------------------------------------- | :------------------------------------------------------------------------------------- |
| **pybind11**     | Modern C++/Python bindings (recommended) | [github.com/pybind/pybind11](https://github.com/pybind/pybind11)                       |
| **ctypes**       | Python built-in FFI                      | [docs.python.org/3/library/ctypes.html](https://docs.python.org/3/library/ctypes.html) |
| **cffi**         | C Foreign Function Interface             | [cffi.readthedocs.io](https://cffi.readthedocs.io/)                                    |
| **SWIG**         | Multi-language wrapper generator         | [swig.org](https://www.swig.org/)                                                      |
| **Boost.Python** | Boost C++/Python interop                 | [boost.org/libs/python](https://www.boost.org/doc/libs/release/libs/python/)           |

### Testing Frameworks

| Framework       | Description                       | Link                                                                                                       |
| :-------------- | :-------------------------------- | :--------------------------------------------------------------------------------------------------------- |
| **Catch2**      | Modern header-only test framework | [github.com/catchorg/Catch2](https://github.com/catchorg/Catch2)                                           |
| **Google Test** | Full-featured testing framework   | [github.com/google/googletest](https://github.com/google/googletest)                                       |
| **doctest**     | Fastest single-header testing     | [github.com/doctest/doctest](https://github.com/doctest/doctest)                                           |
| **CTest**       | CMake's testing driver            | [cmake.org/cmake/help/latest/manual/ctest.1.html](https://cmake.org/cmake/help/latest/manual/ctest.1.html) |

### Data Parsing Libraries

| Library                 | Format                  | Link                                                                                               |
| :---------------------- | :---------------------- | :------------------------------------------------------------------------------------------------- |
| **nlohmann/json**       | JSON                    | [github.com/nlohmann/json](https://github.com/nlohmann/json)                                       |
| **RapidJSON**           | JSON (high performance) | [rapidjson.org](https://rapidjson.org/)                                                            |
| **simdjson**            | JSON (fastest)          | [github.com/simdjson/simdjson](https://github.com/simdjson/simdjson)                               |
| **yaml-cpp**            | YAML                    | [github.com/jbeder/yaml-cpp](https://github.com/jbeder/yaml-cpp)                                   |
| **fast-cpp-csv-parser** | CSV                     | [github.com/ben-strasser/fast-cpp-csv-parser](https://github.com/ben-strasser/fast-cpp-csv-parser) |
| **pugixml**             | XML                     | [pugixml.org](https://pugixml.org/)                                                                |
| **toml++**              | TOML                    | [github.com/marzer/tomlplusplus](https://github.com/marzer/tomlplusplus)                           |

<br>

<div align="right">
<a href="#cse-211--data-structures">↑ Back to Top</a>
</div>

---

<br>

<div align="center">

### For complete details, read `base.pdf`

<br>

*Good luck with your projects!*

<br>

---

<sub>CSE 211 — Data Structures · Term Project · 2025-2026 Fall Semester</sub>

</div>
