# AI PROJECT GUIDELINES

## 🎯 Purpose

This project is developed with the assistance of AI (ChatGPT).
The goal is to maintain a **clean, modular, maintainable, and deterministic system**.

The AI is a **tool**, not a decision maker.

---

## ⚠️ Core Principles

1. **DO NOT ASSUME ANYTHING**

   * If something is not explicitly defined → ask or do nothing

2. **DO NOT ADD FEATURES**

   * Only implement what is explicitly requested

3. **FOLLOW THE SPEC ONLY**

   * The file `SPEC.md` is the single source of truth
   * If there is a conflict → SPEC wins

4. **NO CREATIVE SOLUTIONS**

   * Prefer simple, predictable, standard solutions

5. **NO DUPLICATION**

   * Never duplicate logic
   * Always reuse existing modules/services

6. **KEEP CODE CLEAN**

   * Remove unused code
   * Avoid dead code
   * Avoid commented-out blocks

---

## 🧱 Architecture Rules

* Use modular structure

* Each module must be:

  * Independent
  * Testable
  * Clearly defined

* Separation of concerns is mandatory:

  * UI (components/pages)
  * Logic (services)
  * Data (models)

* No business logic inside UI components

---

## 📁 Folder Structure (Must Follow)

```
/src
  /components
  /pages
  /services
  /models
  /utils
```

* Do not create new folders unless explicitly approved
* Do not move files without reason

---

## 🔌 API Rules

* All API communication must go through a service layer
* No direct API calls inside components

Each API must follow:

```
Input:
- explicit fields

Output:
- explicit fields
```

No implicit structures allowed

---

## 🧠 State Management Rules

* Avoid global state unless explicitly required
* Keep state minimal and local when possible

---

## 🔄 Refactor Rules

* Do NOT rewrite the entire system at once
* Use incremental refactor (Strangler Pattern)

Steps:

1. Identify module
2. Isolate module
3. Rebuild clean version
4. Replace old implementation

---

## 🧪 Code Quality Checklist (Before Merge)

* No duplicated code
* No unused variables/functions
* Clear naming
* Single responsibility per function
* No hidden side effects

---

## 🤖 How to Work With AI

When asking AI to implement something:

### ALWAYS PROVIDE:

* Clear task
* Relevant SPEC section
* Constraints

### Example:

```
Task: Implement UserService

Constraints:
- Must follow API contract from SPEC.md
- No business logic in components
- No new dependencies
```

---

## 🚫 Forbidden Actions

* Adding new libraries without approval
* Changing architecture without approval
* Writing “temporary” code
* Ignoring SPEC
* Making assumptions

---

## ✅ Development Flow

1. Define requirement in SPEC.md
2. Break into small task
3. Implement with AI (focused prompt)
4. Review code (manual + AI audit)
5. Merge

---

## 📌 Notes

* If something is unclear → STOP and clarify
* Precision is more important than speed
* Clean code now = less pain later

---

## 🧹 Graveyard (To Maintain)

Keep a list of:

* Deprecated features
* Removed modules
* Old APIs

This prevents code resurrection and duplication

---