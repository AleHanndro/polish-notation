# Lenguajes y Autómatas 2 (7A - 2025B) - Actividad 4

## Project Overview

Educational python project for converting infix mathematical expressions to postfix (Reverse Polish Notation) and prefix (Polish Notation).

## Development Workflow

- **Environment**: `uv sync` to install dependencies, `source .venv/bin/activate` to activate
- **Testing**: `pytest` (no tests implemented yet)
- **Linting**: `ruff check` and `ruff format` (120 char line length)

## Key Patterns

- **Spanish Naming**: Use Spanish for comments, docstrings, and educational content
- **Python Best Practices**: Follow Python best practices and write Pythonic code
- **Error Handling**: Clear error messages for invalid expressions
- **Comments**: Never write comments that explain what the code does. Instead, write comments that explain why the code does what it does.

## Implementation Notes

- Support operators: `+ - * / ^` with parentheses
- Handle optional spaces in input
- Validate balanced parentheses and valid tokens
- Show intermediate steps (operator queue/stack states)
- Two conversion methods: Shunting Yard for postfix, AST inversion for prefix
- Parentheses are not included in postfix and prefix output as operator precedence is implicit
- **Evaluation**: Compute results using postfix expression (stack-based evaluation) with variable substitution

## Examples

```text
Infix: (A + B) * C ^ D - E
Postfix: A B + C D ^ * E -
Prefix: - * + A B ^ C D E
```

## Dependencies

- [questionary](https://github.com/tmbo/questionary) for interactive CLI
- Core logic should be framework-agnostic for testing
