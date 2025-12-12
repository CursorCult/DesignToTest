---
description: "Design interfaces for rapid, isolated testing"
alwaysApply: true
---

# DesignToTest Rule

Design source-code interfaces so correctness can be tested quickly, locally, and with minimal setup.

Requirements:
1. Every non-trivial behavior must be reachable through a small, explicit interface that can be exercised in isolation.
2. Avoid monolithic functions or classes whose logic requires extensive environment setup or teardown to test.
3. Extract “engine” or “kernel” logic into functions or methods with clear, deterministic inputs and outputs; prefer pure or mostly‑pure units where possible.
4. It is acceptable to make such core operations public or protected solely to enable direct, high‑signal tests, even if this broadens the public API.
5. Tests should target these focused interfaces so that failures localize bugs to the defining unit.

When modifying existing code, refactor toward these properties before adding tests if the current shape would force brittle, high‑setup tests.
