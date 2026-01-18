# Contributing to LLM Security Toolkit

First off, thank you for considering contributing to the LLM Security Toolkit! It's people like you who make this resource valuable for the AI security community.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How Can I Contribute?](#how-can-i-contribute)
- [Submission Guidelines](#submission-guidelines)
- [Style Guide](#style-guide)

## Code of Conduct

This project adheres to a code of conduct. By participating, you are expected to uphold this code. Please be respectful and constructive in all interactions.

## How Can I Contribute?

### 🐛 Reporting Issues

- **Broken Links**: Found a dead link? Open an issue with the link and section.
- **Outdated Information**: Tools change quickly. Let us know if something is outdated.
- **Incorrect Information**: Spot an error? Please report it.

### ✨ Adding New Resources

We welcome additions of:

- **Security Tools**: Open source or commercial tools for LLM security
- **Research Papers**: Academic papers on LLM vulnerabilities and defenses
- **Frameworks**: Governance, compliance, or security frameworks
- **Learning Resources**: Courses, tutorials, and educational content

### 📝 Improving Documentation

- Fix typos or grammatical errors
- Improve descriptions for clarity
- Add missing information to existing entries
- Translate content (future goal)

## Submission Guidelines

### For New Tools/Resources

Before submitting, please ensure:

1. **Relevance**: The resource is directly related to LLM security
2. **Quality**: The tool/resource is actively maintained and reputable
3. **Not a Duplicate**: Check if it's already listed
4. **Proper Category**: Place it in the most appropriate section

### Pull Request Process

1. **Fork** the repository
2. **Create a branch**: `git checkout -b feature/add-new-tool`
3. **Make your changes** following the style guide below
4. **Test your changes**: Ensure all links work
5. **Commit**: Use clear, descriptive commit messages
6. **Push**: `git push origin feature/add-new-tool`
7. **Open a PR**: Provide a clear description of your changes

### Commit Message Format

```
type: short description

Longer description if needed.

- Bullet points for multiple changes
- Another change
```

Types: `add`, `update`, `fix`, `remove`, `docs`

Example:
```
add: NeMo Guardrails to guardrails section

Added NVIDIA's NeMo Guardrails with description and GitHub link.
```

## Style Guide

### Adding a Tool (Table Format)

```markdown
| [**Tool Name**](https://github.com/org/tool) | Brief description (max 100 chars). | ![GitHub stars](https://img.shields.io/github/stars/org/tool) | Language |
```

### Adding a Paper

```markdown
| [Paper Title](https://arxiv.org/abs/xxxx.xxxxx) | Authors et al. | Year | Topic |
```

### Adding a Resource

```markdown
| [Resource Name](https://url.com) | Provider | Level/Type |
```

### General Formatting

- Use **bold** for tool names in tables
- Include GitHub star badges for open source tools when possible
- Keep descriptions concise but informative
- Use proper capitalization
- End descriptions without periods in tables

### Link Requirements

- Use HTTPS links when available
- Link directly to the tool/resource (not through redirects)
- Prefer official sources over third-party

## Questions?

Feel free to open an issue for any questions about contributing. We're happy to help!

---

Thank you for contributing to LLM Security! 🛡️
