# DEPRECATED

This rule is deprecated.

---

# Part of the [CursorCult](https://github.com/CursorCult)

# DesignToTest

Design interfaces for rapid, isolated testing.

**Install**

```sh
pipx install cursorcult
cursorcult link DesignToTest
```

Rule file format reference: https://cursor.com/docs/context/rules#rulemd-file-format

**When to use**

- Writing tests currently requires large fixtures, mocks, or environment setup.
- You want failing tests to point directly to the responsible unit.
- You're willing to expose more surface area to enable high-signal tests.

**What it enforces**

- Core logic is reachable through small, explicit, deterministic interfaces.
- Avoid monolithic units that require heavy setup/teardown to test.
- Promote internal "engine/kernel" operations to public or protected when it materially improves testability.

**Credits**

- Developed by Will Wieselquist. Anyone can use it.
