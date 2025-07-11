# Python Cursor Rules

A comprehensive set of Cursor rules for Python development with modern tooling and best practices.

## Overview

These rules are designed for Python projects using **UV** for dependency management and following modern Python development practices. They enforce consistent project structure, coding standards, and documentation practices.

## Rules Included

### 1. Project Structure (`python-project-structure.mdc`)
- **Type**: Always
- **Purpose**: Defines consistent project organization and folder structure
- **Features**:
  - UV-based dependency management
  - Notebooks stored in `notebooks/` folder
  - Standard project layout with `src/`, `tests/`, and configuration files

### 2. Coding Standards (`python-coding-standards.mdc`)
- **Type**: Auto Attached (*.py files)
- **Purpose**: Enforces Python best practices and code style
- **Features**:
  - PEP 8 compliance
  - Type hints requirement
  - Error handling best practices
  - Code organization guidelines

### 3. Jupyter Notebook Standards (`jupyter-notebook-standards.mdc`)
- **Type**: Auto Attached (notebooks/**/*.ipynb)
- **Purpose**: Maintains clean, organized notebook structure
- **Features**:
  - Consistent notebook organization
  - Documentation requirements
  - Data science best practices
  - Version control considerations

### 4. UV Workflow (`uv-workflow.mdc`)
- **Type**: Agent Requested
- **Purpose**: Provides UV package manager commands and workflows
- **Features**:
  - Dependency management commands
  - Virtual environment handling
  - Best practices for UV usage

### 5. README Template (`readme-template.mdc`)
- **Type**: Manual
- **Purpose**: Template for creating clean, focused README files
- **Features**:
  - UV-focused installation instructions
  - Clean, minimal structure
  - No irrelevant deployment or alternative package manager info

## Quick Setup

### Option 1: Copy All Rules
```bash
# In your project root
mkdir -p .cursor/rules
cd .cursor/rules

# Download all Python rules
curl -O https://raw.githubusercontent.com/adilmoujahid/cursor-rules/main/python/python-project-structure.mdc
curl -O https://raw.githubusercontent.com/adilmoujahid/cursor-rules/main/python/python-coding-standards.mdc
curl -O https://raw.githubusercontent.com/adilmoujahid/cursor-rules/main/python/jupyter-notebook-standards.mdc
curl -O https://raw.githubusercontent.com/adilmoujahid/cursor-rules/main/python/uv-workflow.mdc
curl -O https://raw.githubusercontent.com/adilmoujahid/cursor-rules/main/python/readme-template.mdc
```

### Option 2: Selective Installation
Choose only the rules you need:
- **Essential**: `python-project-structure.mdc` + `python-coding-standards.mdc`
- **For Data Science**: Add `jupyter-notebook-standards.mdc`
- **For Documentation**: Add `readme-template.mdc`
- **For UV Help**: Add `uv-workflow.mdc`

## Prerequisites

- **UV**: Install UV package manager
  ```bash
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```
- **Python 3.8+**: Modern Python version
- **Cursor Editor**: Latest version with rules support

## Recommended Project Structure

```
my-python-project/
├── .cursor/
│   └── rules/              # Cursor rules
├── src/                    # Source code
│   └── my_package/
├── notebooks/              # Jupyter notebooks
├── tests/                  # Test files
├── .env.example           # Environment variables template
├── .gitignore            # Git ignore file
├── pyproject.toml        # Project configuration
├── README.md             # Project documentation
└── ruff.toml            # Linting configuration
```

## Common UV Commands

These commands are reinforced by the rules:

```bash
# Project setup
uv init
uv sync

# Add dependencies
uv add pandas numpy requests
uv add --dev pytest black ruff mypy

# Run commands
uv run python script.py
uv run jupyter lab
uv run pytest
```

## Best Practices Enforced

- **Type Hints**: All function parameters and return values
- **Documentation**: Comprehensive docstrings and comments
- **Testing**: Unit tests for all business logic
- **Code Quality**: Consistent formatting and linting
- **Project Organization**: Clear separation of concerns
- **Dependency Management**: Proper use of UV for all package operations

## Integration with Development Tools

These rules work well with:
- **Black**: Code formatting
- **Ruff**: Fast linting and formatting
- **MyPy**: Static type checking
- **Pytest**: Testing framework
- **Pre-commit**: Git hooks for code quality

## Customization

You can modify these rules to fit your specific needs:
1. Edit the `.mdc` files in your project's `.cursor/rules/` directory
2. Adjust patterns, types, or content as needed
3. Add project-specific rules for domain knowledge

## Examples

### Using the README Template
```
@readme-template
```
This will provide the template for creating a clean README.md file.

### Auto-Applied Rules
When you work on Python files, the coding standards will automatically apply. When working in notebooks, the notebook standards will be active.

## Troubleshooting

**Rule not applying?**
- Check the rule type and ensure files match the patterns
- For Agent Requested rules, make sure descriptions are clear
- Verify the `.mdc` format is correct

**Need help with UV?**
- The UV workflow rule provides comprehensive command examples
- Check the official UV documentation for advanced usage

## Contributing

Found an issue or have a suggestion? Please contribute:
1. Fork the main repository
2. Make your changes to the Python rules
3. Test the rules in a real project
4. Submit a pull request

## License

MIT License - see the main repository's LICENSE file for details.