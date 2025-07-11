# Cursor Rules Collection

A curated collection of [Cursor](https://cursor.com) rules for various programming languages and frameworks. These rules help maintain consistency, enforce best practices, and improve your development workflow across different projects.

## What are Cursor Rules?

Cursor rules are reusable instructions that provide persistent context to the AI assistant. They help ensure consistent code style, project structure, and development practices across your projects.

## Repository Structure

```
cursor-rules/
├── python/              # Python development rules
├── javascript/          # JavaScript/Node.js rules (coming soon)
├── nextjs/             # Next.js framework rules (coming soon)
├── react/              # React framework rules (coming soon)
├── typescript/         # TypeScript rules (coming soon)
└── templates/          # Reusable templates and examples
```

## Available Rule Sets

### ✅ Python
Complete set of rules for Python development with modern tooling:
- **Project Structure**: Organization and folder layout
- **Coding Standards**: PEP 8 compliance, type hints, and best practices
- **UV Workflow**: Virtual environment management with UV
- **Jupyter Notebooks**: Notebook organization and standards
- **Documentation**: Clean README templates

[📁 View Python Rules](./python/)

## Quick Start

1. **Choose your language/framework** from the folders above
2. **Copy the rules** you want to use
3. **Create `.cursor/rules/` directory** in your project
4. **Add the rule files** to your project's `.cursor/rules/` folder
5. **Start coding** with AI assistance tailored to your stack

## How to Use

### Method 1: Manual Setup
```bash
# In your project root
mkdir -p .cursor/rules
cd .cursor/rules

# Copy rule files from this repo
curl -O https://raw.githubusercontent.com/adilmoujahid/adil-cursor-rules/main/python/python-project-structure.mdc
curl -O https://raw.githubusercontent.com/adilmoujahid/adil-cursor-rules/main/python/python-coding-standards.mdc
# ... add other rules as needed
```

### Method 2: Using Cursor
1. Open Cursor Settings > Rules
2. Click "New Cursor Rule"
3. Copy and paste the content from the rule files in this repo
4. Save with the appropriate filename

## Rule Types

- **Always**: Applied to every context automatically
- **Auto Attached**: Triggered when working with specific file patterns
- **Agent Requested**: Available for AI to use when relevant
- **Manual**: Explicitly referenced with @rule-name

## Contributing

We welcome contributions! Please:

1. Fork this repository
2. Create a new branch for your rule set
3. Follow the existing structure and naming conventions
4. Add comprehensive documentation
5. Submit a pull request

### Adding New Rule Sets

When adding rules for a new language/framework:

1. Create a new folder with a descriptive name
2. Include a README.md explaining the rules
3. Use the `.mdc` format for all rules
4. Provide setup instructions
5. Include examples where helpful

## Best Practices for Rule Creation

- **Keep rules focused**: Each rule should have a single, clear purpose
- **Provide examples**: Include code snippets and use cases
- **Use appropriate types**: Choose the right rule type for each use case
- **Document thoroughly**: Explain what each rule does and why it's useful
- **Test rules**: Verify that rules work as expected in real projects

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.