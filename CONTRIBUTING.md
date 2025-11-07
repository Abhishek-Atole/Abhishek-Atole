# Contributing to Abhishek Atole's Projects

Thank you for your interest in contributing! This document provides guidelines for contributing to the projects in this repository.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Workflow](#development-workflow)
- [Coding Standards](#coding-standards)
- [Commit Guidelines](#commit-guidelines)
- [Pull Request Process](#pull-request-process)
- [Reporting Issues](#reporting-issues)

## Code of Conduct

By participating in this project, you agree to abide by the [Code of Conduct](CODE_OF_CONDUCT.md). Please read it before contributing.

## Getting Started

1. **Fork the repository** you want to contribute to
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/<your-username>/<project-name>.git
   cd <project-name>
   ```
3. **Create a feature branch**:
   ```bash
   git checkout -b feature/your-feature-name
   ```

## Development Workflow

### Prerequisites

- C++ compiler with C++17/C++20 support (GCC 9+, Clang 10+, or MSVC 2019+)
- CMake 3.15 or higher
- Git for version control
- (Optional) Docker for containerized builds

### Building the Project

```bash
mkdir build && cd build
cmake ..
make -j$(nproc)
```

### Running Tests

```bash
cd build
ctest --output-on-failure
```

or

```bash
make test
```

## Coding Standards

### C++ Style Guide

- Follow modern C++ best practices (RAII, smart pointers, const-correctness)
- Use meaningful variable and function names
- Prefer `snake_case` for functions and variables, `PascalCase` for classes
- Keep functions small and focused (single responsibility principle)
- Document complex logic with clear comments
- Use `const` and `constexpr` where appropriate

### Code Formatting

- Indentation: 4 spaces (no tabs)
- Line length: max 100 characters
- Braces: Allman style preferred for functions, K&R style for control flow
- Use clang-format if available (configuration may be provided in project root)

### Documentation

- Add Doxygen-style comments for public APIs:
  ```cpp
  /**
   * @brief Brief description of the function
   * @param param1 Description of param1
   * @return Description of return value
   */
  ```
- Update README.md if adding new features or changing usage
- Add inline comments for non-obvious implementation details

## Commit Guidelines

Write clear, descriptive commit messages following this format:

```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types

- **feat**: New feature
- **fix**: Bug fix
- **docs**: Documentation changes
- **style**: Code style changes (formatting, missing semicolons, etc.)
- **refactor**: Code refactoring without changing functionality
- **perf**: Performance improvements
- **test**: Adding or updating tests
- **chore**: Maintenance tasks, dependency updates

### Example

```
feat(parser): add support for JSON configuration files

- Implement JSON parser using nlohmann/json library
- Add configuration schema validation
- Update documentation with JSON config examples

Closes #42
```

## Pull Request Process

1. **Ensure your code builds** without warnings and all tests pass
2. **Update documentation** if you've changed APIs or added features
3. **Add or update tests** to cover your changes
4. **Run static analysis** tools if available (cppcheck, clang-tidy)
5. **Create a pull request** with a clear title and description:
   - Reference related issues (e.g., "Fixes #123")
   - Describe what changed and why
   - Include screenshots/examples if applicable
6. **Respond to review feedback** promptly and make requested changes
7. **Squash commits** if requested before merging

### PR Checklist

- [ ] Code compiles without errors or warnings
- [ ] All tests pass
- [ ] New tests added for new functionality
- [ ] Documentation updated
- [ ] Code follows project style guidelines
- [ ] Commit messages are clear and descriptive
- [ ] No unnecessary files included (build artifacts, IDE configs)

## Reporting Issues

### Bug Reports

Include the following information:

- **Description**: Clear description of the bug
- **Steps to reproduce**: Detailed steps to trigger the issue
- **Expected behavior**: What should happen
- **Actual behavior**: What actually happens
- **Environment**: OS, compiler version, CMake version
- **Code sample**: Minimal reproducible example if possible
- **Stack trace**: If the program crashes

### Feature Requests

Include:

- **Problem description**: What problem does this solve?
- **Proposed solution**: How should it work?
- **Alternatives considered**: Other approaches you've thought about
- **Additional context**: Use cases, examples, mockups

## Questions?

If you have questions about contributing, feel free to:

- Open a discussion issue
- Reach out via email: abhiatole03@gmail.com
- Connect on LinkedIn: [linkedin.com/in/abhishek-atole](https://www.linkedin.com/in/abhishek-atole/)

Thank you for contributing! 🚀
