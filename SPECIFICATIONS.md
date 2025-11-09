# 🧾 **Specifications Sheet – Task Tracker CLI**

## 📌 **1. Project Overview**

**Project Name:** Task Tracker CLI
**Author:** Mohamed Amine Barkati
**Date:** November 2025
**Version:** 1.0
**Status:** In development

**Description:**
Task Tracker CLI is a **command-line productivity application** designed to help users manage daily tasks efficiently.
The program allows users to **create, modify, delete, and view tasks**, each with associated attributes such as priority, category, and deadline.
All data is stored locally in a **database (SQLite)**, ensuring offline access and simple persistence.

---

## 🌟 **2. Objectives**

### **General Objective**

Develop a **modular and maintainable CLI-based task management system** applying **object-oriented programming principles** and **design patterns**.

### **Specific Objectives**

* Implement CRUD operations for tasks.
* Apply OOP principles (encapsulation, inheritance, polymorphism).
* Integrate at least one design pattern (Singleton, Factory, Strategy…).
* Ensure persistent storage with a simple database or file system.
* Create a clean, intuitive command-line user interface.
* Set up a basic CI pipeline for testing and validation.

---

## 🧩 **3. Functional Requirements**

| **ID** | **Feature**      | **Description**                                                                      | **Priority** |
| ------ | ---------------- | ------------------------------------------------------------------------------------ | ------------ |
| F1     | Add Task         | User can create a new task with title, description, deadline, category, and priority | High         |
| F2     | Edit Task        | User can modify details of an existing task                                          | Medium       |
| F3     | Delete Task      | User can remove a task from the list                                                 | High         |
| F4     | List Tasks       | Display all tasks with key details                                                   | High         |
| F5     | Filter / Sort    | User can filter tasks by category, priority, or due date                             | Medium       |
| F6     | Mark as Done     | User can mark a task as completed                                                    | Medium       |
| F7     | Data Persistence | Tasks are saved and loaded automatically from a file or database                     | High         |
| F8     | Help Command     | Display available commands and syntax                                                | Low          |
| F9     | Export / Import  | Optional feature to export data to JSON or CSV                                       | Optional     |

---

## 🧬 **4. Non-Functional Requirements**

| **Type**            | **Description**                                                         |
| ------------------- | ----------------------------------------------------------------------- |
| **Performance**     | Must handle at least 500 tasks efficiently.                             |
| **Usability**       | Commands should be simple and intuitive.                                |
| **Maintainability** | Code should follow modular structure (separate classes for Task, Storage, CLI, etc.). |
| **Portability**     | Must run on Windows, Linux, and macOS (Java 17+).                       |
| **Security**        | Data stored locally; optional password protection.                      |
| **Testability**     | Unit tests must cover at least 70% of the codebase.                     |

---

## 🏧 **5. System Architecture**

### **Main Components**

1. **Task Manager Module**

    * Handles creation, modification, deletion, and retrieval of tasks.
    * Stores task list in memory before saving.

2. **Storage Module**

    * Responsible for reading/writing data from/to file or SQLite DB.
    * Uses *Singleton* pattern to ensure single access point.

3. **CLI Interface Module**

    * Interprets user commands and routes actions to Task Manager.
    * Displays formatted results in the terminal.

4. **Utility / Helpers**

    * Date parsing, sorting algorithms, and error handling.

### **Architecture Diagram (Text-based)**

```
+-----------------------------+
|        CLI Interface        |
|  (Command Input/Output)     |
+-------------+---------------+
              |
              v
+-------------+---------------+
|         Task Manager         |
| (CRUD Operations, Logic)     |
+-------------+---------------+
              |
              v
+-------------+---------------+
|        Storage Module        |
| (JSON / SQLite Persistence)  |
+-----------------------------+
```

---

## 🧪 **6. Testing Plan**

| **Test Type**         | **Description**                                            |
| --------------------- | ---------------------------------------------------------- |
| **Unit Tests**        | Test CRUD functions, data persistence, and command parser. |
| **Integration Tests** | Verify interactions between CLI, TaskManager, and Storage. |
| **Manual Testing**    | User testing of CLI commands.                              |
| **CI/CD Integration** | Use GitHub Actions to run automated tests on push.         |

---

## 🧯 **7. Tools and Technologies**

| **Category**         | **Tool / Framework**     |
| -------------------- | ------------------------ |
| Programming Language | Python 3.x or Java 17+   |
| Database             | SQLite or JSON file      |
| Version Control      | Git + GitHub             |
| CI/CD                | GitHub Actions           |
| Testing Framework    | pytest / JUnit           |
| Documentation        | Markdown + UML Diagrams  |
| Optional             | Docker, pre-commit hooks |

---

## 🧱 **8. Deliverables**

* Source code (GitHub repository)
* Unit test coverage report
* User manual (`README.md`)
* Specifications (`SPECIFICATIONS.md`)
* Terms & Conditions (`TERMS.md`)
* Demo video or screenshots

---

## 🗕️ **9. Development Timeline**

| **Phase**                         | **Duration** | **Main Deliverable**              |
| --------------------------------- | ------------ | --------------------------------- |
| Phase 1 – Requirements & Design   | 1 week       | Specification sheet + UML diagram |
| Phase 2 – Core Implementation     | 3 weeks      | Task management & persistence     |
| Phase 3 – CLI Integration         | 1 week       | Usable CLI with commands          |
| Phase 4 – Testing & Documentation | 1 week       | Unit tests + README               |
| Phase 5 – CI/CD Setup             | 1 week       | GitHub Actions pipeline           |
| **Total Estimated Time:**         | **~6 weeks** |                                   |

---

## ⚖️ **10. Licensing and Legal**

* License: **MIT License**
* Author retains copyright.
* Open-source contributions welcome via pull requests.

---
