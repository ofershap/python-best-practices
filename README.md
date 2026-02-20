# Python Best Practices

Modern Python 3.12+ patterns your AI agent should use. Type hints, async/await, Pydantic v2, uv package manager, match statements, and project structure.

## Install

### Cursor IDE

```
/add-plugin python-best-practices
```

### Claude Code

```
/plugin install python-best-practices
```

### Skills only (any agent)

```bash
npx skills add ofershap/python-best-practices/python-best-practices
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

### Skills

- **python-best-practices** - Modern Python 3.12+ patterns your AI agent should use. Type hints, async/await, Pydantic v2, uv package manager, match statements, and project structure.

### Rules

- **best-practices** - Always-on rules that enforce current Python patterns

### Commands

- `/audit` - Scan your codebase for Python anti-patterns

## Why This Plugin?

AI agents are trained on data that includes outdated patterns. This plugin ensures your agent uses current Python best practices:

1. **Outdated type hints** - Agents emit `from typing import List, Union, Optional` and `List[str]` instead of `list[str]` and `X | Y`.
2. **Pydantic v1 API** - Agents use deprecated `@validator`, `@root_validator`, and `class Config` instead of `field_validator`, `model_validator`, and `ConfigDict`.
3. **Legacy path handling** - Agents use `os.path.join` and string paths instead of `pathlib.Path`.
4. **Old packaging** - Agents create `setup.py` and `requirements.txt` instead of `pyproject.toml` and uv.
5. **Pre-PEP 695 generics** - Agents use `TypeVar` and `Generic[T]` instead of Python 3.12+ type parameter syntax `def f[T](x: T) -> T`.

## License

MIT
