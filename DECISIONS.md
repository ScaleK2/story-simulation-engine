# Design Decisions

This document records important architectural and gameplay decisions made throughout development.

---

## 2026-07-01

### Goods are data

**Decision**

Goods are defined in data files rather than engine code.

**Reason**

Allows future games to replace the economy without changing simulation logic.

---

## 2026-07-01

### Simulation is UI-independent

**Decision**

The simulation engine contains no rendering logic.

**Reason**

Allows the engine to support web, mobile, desktop or terminal interfaces.

---

## 2026-07-01

### Version 0.1 validates the framework

**Decision**

The first implementation focuses on a simple economic trading game.

**Reason**

The objective is to validate the core simulation framework before introducing more complex systems such as characters, politics and dynasties.

---

## 2026-07-01

### Data over code

**Decision**

Game content should be defined through structured data wherever practical.

**Reason**

Makes future expansions easier and allows AI-assisted content generation without modifying engine logic.

---

## 2026-07-01

### Scope discipline

**Decision**

No new systems are added until the Version 0.1 gameplay loop is fun.

**Reason**

A compelling core loop is more valuable than a large number of unfinished features.
