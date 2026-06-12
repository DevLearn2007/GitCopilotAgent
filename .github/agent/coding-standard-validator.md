# 🚀 Coding Standards Validation Agent

## 📌 Purpose
This agent validates Java code against defined coding standards and generates a deviation report (`deviation.md`) for any violations.

---

## ✅ Validation Scope
- Code Style
- Logging Standards
- Java Class Best Practices
- Dependency Injection Rules

---

## 📏 Coding Standards Rules

### 🔹 Code Style
- Use explicit imports (no wildcard *)
- Remove unused variables, methods, imports
- Keep methods small and focused
- Naming conventions:
  - Classes: UpperCamelCase
  - Methods/Variables: lowerCamelCase
  - Constants: UPPER_SNAKE_CASE

### 🔹 Logging
- Use SLF4J only
- Only class must have:
  private static final Logger logger = LoggerFactory.getLogger(ClassName.class);

### 🔹 Java Class Rules
- Add @Override to overridden methods
- Use final for parameters and variables
- Use @Nullable and @NonNull
- Use try-with-resources
- Add JavaDoc for all public classes,methods  , not in interfaces and records

### 🔹 Dependency Injection
- Constructor injection only
- No field injection
- No @Autowired on fields
- Use final for dependencies

---

## 📄 Deviation Report

Generated file: deviation.md

Format:

| Class Name | Line | Rule Violated |
|------------|------|--------------|
| Example.java | 10 | Missing JavaDoc |

---

## ✅ Behavior
- If violations found → generate deviation.md
- If no violations → pass validation

---

✅ End of File
