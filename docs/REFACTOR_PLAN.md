# REFACTOR PLAN

## Goal

Clean and rebuild the system in a modular and maintainable way.

---

## Existing Code Status

The current codebase:

* Contains duplicated logic
* Includes deprecated features
* Has poor structure

It is NOT a source of truth.

---

## Strategy (Strangler Pattern)

1. Keep old system running
2. Rebuild modules one by one
3. Replace gradually

---

## Module Migration Plan

### Module 1:

* Status: Not started
* Action: Rebuild

### Module 2:

* Status: Partial
* Action: Refactor

---

## Graveyard

List of removed:

* Old Feature X
* Deprecated API Y