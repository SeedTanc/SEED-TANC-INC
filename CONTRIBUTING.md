# Contributing to Seed Tanc Inc.

**Thank you for your interest in contributing to Seed Tanc Inc.!**

We welcome contributions from developers, designers, researchers, and innovators. This document provides guidelines and best practices for contributing to our projects.

---

## 📋 Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [Getting Started](#getting-started)
3. [Development Workflow](#development-workflow)
4. [Coding Standards](#coding-standards)
5. [Commit Guidelines](#commit-guidelines)
6. [Pull Request Process](#pull-request-process)
7. [Security Guidelines](#security-guidelines)
8. [Testing Requirements](#testing-requirements)
9. [Documentation](#documentation)
10. [Contact & Support](#contact--support)

---

## 🤝 Code of Conduct

All contributors must adhere to our Code of Conduct:

- **Be respectful** - Treat all team members with respect and professionalism
- **Be inclusive** - Welcome diverse perspectives and backgrounds
- **Be collaborative** - Work together to achieve shared goals
- **Be professional** - Maintain professional conduct in all interactions
- **Be transparent** - Communicate openly and honestly
- **Report violations** - Report Code of Conduct violations to conduct@seedtanc.inc

---

## 🚀 Getting Started

### Prerequisites
- Git installed and configured
- GitHub account with SSH keys set up
- Development environment setup (varies by project)
- Required tools and dependencies installed

### Clone & Setup
```bash
# Clone the repository
git clone git@github.com:SeedTanc/SEED-TANC-INC.git
cd SEED-TANC-INC

# Create a new branch
git checkout -b feature/your-feature-name

# Install dependencies
# (varies by project - see individual README files)
```

### Branch Naming Convention
```
feature/feature-name       # New features
fix/bug-description        # Bug fixes
refactor/what-changed      # Code refactoring
docs/documentation-update  # Documentation changes
test/test-addition         # Test additions
security/security-fix      # Security patches
chore/maintenance-task     # Maintenance tasks
```

---

## 🔄 Development Workflow

### 1. Create Feature Branch
```bash
git checkout -b feature/my-feature
```

### 2. Make Changes
- Follow coding standards
- Write clear, descriptive commits
- Test your changes frequently
- Keep commits logical and atomic

### 3. Run Tests Locally
```bash
# Run unit tests
npm test           # Node.js
python -m pytest   # Python
go test ./...      # Go
cargo test         # Rust
```

### 4. Commit Changes
```bash
git add .
git commit -m "feat: add new feature"
```

### 5. Push & Create PR
```bash
git push origin feature/my-feature
```
Then create a Pull Request on GitHub.

---

## 💻 Coding Standards

### General Principles
- **DRY (Don't Repeat Yourself)** - Avoid code duplication
- **SOLID Principles** - Single responsibility, Open/closed, Liskov substitution, Interface segregation, Dependency inversion
- **KISS (Keep It Simple, Stupid)** - Simple solutions preferred
- **Clean Code** - Readable, maintainable, well-documented
- **Performance** - Optimize for efficiency
- **Security** - Follow security best practices

### Language-Specific Standards

#### Python
```python
# PEP 8 compliant
# Type hints required
# Docstrings for all functions/classes
# Use pytest for testing
```

#### JavaScript/TypeScript
```javascript
// ESLint configured
// Prettier for formatting
// JSDoc comments required
// Use Jest/Vitest for testing
```

#### Go
```go
// gofmt compliant
// golint clean
// godoc comments required
// Use testing package
```

#### Rust
```rust
// rustfmt compliant
// clippy clean
// Doc comments for public items
// Use cargo test
```

### Code Quality
- Minimum 80% test coverage
- Zero critical security issues
- No hardcoded secrets
- No TODO/FIXME without issue reference
- Meaningful variable names
- Max 100-120 characters per line

---

## 📝 Commit Guidelines

### Commit Message Format
```
<type>(<scope>): <subject>

<body>

<footer>
```

### Types
- `feat:` - New feature
- `fix:` - Bug fix
- `refactor:` - Code refactoring
- `perf:` - Performance improvement
- `test:` - Test additions/modifications
- `docs:` - Documentation changes
- `style:` - Code style changes (no logic change)
- `chore:` - Build, CI, dependencies
- `security:` - Security patches

### Example
```
feat(auth): implement JWT token refresh mechanism

Implements automatic JWT token refresh when tokens are within
30 minutes of expiration. Includes new RefreshTokenService class
and integration with existing AuthManager.

Closes #123
Fixes #124
```

### Rules
- Use imperative mood ("add" not "added" or "adds")
- Don't capitalize first letter (unless it's a proper noun)
- No period (.) at the end
- Limit to 50 characters for subject line
- Reference issues when applicable
- One logical change per commit

---

## 🔀 Pull Request Process

### Before Creating PR
- [ ] Code follows style guidelines
- [ ] All tests pass locally
- [ ] Added tests for new functionality
- [ ] Updated documentation
- [ ] No breaking changes (or documented)
- [ ] No security vulnerabilities
- [ ] No secrets committed
- [ ] Commits are clean and logical

### PR Title Format
```
[Type] Brief description
Example: [Feature] Add JWT token refresh mechanism
```

### PR Description Template
```markdown
## Description
Brief description of changes

## Related Issue
Closes #123

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing Done
Describe testing performed

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex logic
- [ ] Documentation updated
- [ ] No new warnings generated
- [ ] New tests added
- [ ] All tests passing
- [ ] No breaking changes

## Screenshots (if applicable)
```

### Review Process
1. **Automatic Checks** - CI/CD pipeline runs
   - Tests must pass
   - Code coverage maintained
   - Linting passes
   - Security scans pass

2. **Code Review** - Minimum 2 approvals required
   - Functionality review
   - Code quality review
   - Security review
   - Testing review

3. **Approval** - Merge approved by maintainers

4. **Merge** - Squash and merge to main

---

## 🔐 Security Guidelines

### Critical
⚠️ **NEVER commit:**
- Passwords or API keys
- Private keys or certificates
- Database credentials
- Tokens or access tokens
- Sensitive configuration
- Personal information

### Review
- Security-focused code review
- SAST scanning required
- Dependency vulnerability checks
- Secret scanning
- Penetration testing for critical features

### Reporting
- Security issues: security@seedtanc.inc
- Use GitHub Security Advisory
- Do NOT create public issues
- Expected response: 24 hours

---

## 🧪 Testing Requirements

### Test Coverage
- Minimum 80% coverage for new code
- 100% coverage for critical paths
- All edge cases tested
- Error handling tested

### Test Types
- **Unit Tests** - Individual function/method tests
- **Integration Tests** - Component interaction tests
- **E2E Tests** - Full workflow tests
- **Performance Tests** - Performance validation
- **Security Tests** - Security vulnerability tests

### Running Tests
```bash
# All tests
npm test / python -m pytest / go test ./...

# Specific test file
npm test -- filename.test.js

# With coverage
npm test -- --coverage

# Watch mode
npm test -- --watch
```

---

## 📚 Documentation

### Required Documentation
- **Code comments** - Complex logic explained
- **Function/method docs** - Purpose, parameters, return values
- **README updates** - New features documented
- **API docs** - Endpoints/methods documented
- **Architecture docs** - Design decisions documented

### Documentation Format
```python
"""Summary line.

Longer description explaining purpose, parameters, and return values.

Args:
    param1 (type): Description
    param2 (type): Description

Returns:
    type: Description

Raises:
    ExceptionType: When this happens

Example:
    >>> result = function(param1, param2)
"""
```

---

## 📞 Contact & Support

### Questions?
- **GitHub Discussions** - Ask in project discussions
- **Email** - dev@seedtanc.inc
- **Documentation** - Check `/docs` directory
- **Issues** - Search existing issues first

### Getting Help
1. Check documentation
2. Search existing issues
3. Ask in discussions
4. Create a new issue
5. Contact team: dev@seedtanc.inc

---

## 🙏 Thank You!

Thank you for contributing to Seed Tanc Inc.! Your contributions help us build better products and accelerate innovation in AI and blockchain technologies.

**Let's build the future together! 🚀**

---

*Last Updated: 2026-05-23*
