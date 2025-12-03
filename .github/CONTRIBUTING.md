# Contributing to FluentPDF-AI-Powered-Text-to-Speech-Web-App

Thank you for considering contributing to **FluentPDF-AI-Powered-Text-to-Speech-Web-App**! As an elite architected project, we maintain the highest standards for code quality, consistency, and maintainability.

## 1. Our Guiding Principles

Our contribution process is governed by the Apex Technical Authority's core philosophies:

*   **Zero-Defect:** Strive for immaculate code. Bugs and issues should be proactively identified and resolved.
*   **High-Velocity:** Streamlined processes ensure rapid iteration and delivery without compromising quality.
*   **Future-Proof:** Architect for scalability, adaptability, and longevity, embracing industry best practices and emerging standards.

## 2. Code of Conduct

This project adheres to a strict Code of Conduct. By participating, you agree to uphold these standards, promoting an open, welcoming, respectful, and collaborative environment. Please refer to the [CODE_OF_CONDUCT.md](https://github.com/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App/blob/main/CODE_OF_CONDUCT.md) for details.

## 3. How to Contribute

We welcome contributions in various forms:

*   **Reporting Bugs:** If you find a bug, please open an issue using the **Bug Report** template.
*   **Suggesting Enhancements:** Ideas for new features or improvements can be submitted as issues with the **Enhancement Suggestion** template.
*   **Submitting Pull Requests:** Propose your changes by following the steps below.

## 4. Development Workflow

All contributions are expected to follow our established development workflow:

1.  **Fork the Repository:** Create your own fork of the `chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App` repository.
2.  **Clone Your Fork:** Clone your forked repository to your local development machine:
    bash
    git clone https://github.com/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App.git
    cd FluentPDF-AI-Powered-Text-to-Speech-Web-App
    
3.  **Create a New Branch:** Before making any changes, create a descriptive branch for your contribution:
    bash
    git checkout -b feature/your-new-feature
    # or
    git checkout -b fix/your-bug-fix
    
4.  **Make Your Changes:** Implement your feature or fix. Ensure adherence to the project's architectural patterns and coding standards.
5.  **Lint and Format:** Run the project's linter and formatter to ensure consistency:
    bash
    # Example for a Python project (assuming Ruff is configured)
    ruff check --fix .
    ruff format .
    
    *Note: Consult the `.github/workflows/ci.yml` and `AGENTS.md` for the exact commands and expected stack.* 
6.  **Test Your Changes:** Ensure all tests pass. Run the test suite to verify your changes haven't introduced regressions:
    bash
    # Example for a Python project (assuming Pytest)
    pytest
    
    *Note: If you are adding new functionality, you must also add corresponding tests.
7.  **Commit Your Changes:** Commit your changes with clear, concise, and descriptive commit messages.
    bash
    git commit -m "feat: Add user authentication module"
    # or
    git commit -m "fix: Resolve issue with PDF parsing error"
    
8.  **Push to Your Fork:** Push your changes to your branch in your forked repository:
    bash
    git push origin feature/your-new-feature
    
9.  **Open a Pull Request:** Navigate to the original repository (`chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App`) and open a new Pull Request from your branch. Provide a detailed description of your changes, referencing any relevant issues.

## 5. Branching Strategy

We employ a simplified Gitflow-like branching strategy:

*   **`main`:** Represents the stable, production-ready code.
*   **`develop`:** Integration branch for new features and ongoing development. All pull requests should target `develop`.
*   **Feature Branches:** Branched off `develop` (e.g., `feature/user-auth`, `feature/pdf-converter`).
*   **Fix Branches:** Branched off `develop` for bug fixes (e.g., `fix/parsing-error`, `fix/ui-glitch`).

## 6. AI Agent Directives Compliance

All contributions must align with the directives specified in the **[AGENTS.md](https://github.com/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App/blob/main/AGENTS.md)** file. This ensures consistency in architectural patterns, testing methodologies, and technological choices.

## 7. Pull Request Reviews

*   All Pull Requests (PRs) will be reviewed by at least one maintainer.
*   Reviews will focus on code quality, adherence to architectural principles, test coverage, and documentation.
*   Please be responsive to feedback and make necessary revisions promptly.

## 8. Project Setup & Environment

Ensure your local development environment matches the project's requirements. Refer to the **[README.md](https://github.com/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App/blob/main/README.md)** for detailed setup instructions and the current tech stack.

## 9. Reporting Security Vulnerabilities

We take security very seriously. If you discover any security vulnerability within this project, please report it to us through the **[SECURITY.md](https://github.com/chirag127/FluentPDF-AI-Powered-Text-to-Speech-Web-App/blob/main/SECURITY.md)** guidelines, rather than opening a public issue.

Thank you for contributing to the success of **FluentPDF-AI-Powered-Text-to-Speech-Web-App**!