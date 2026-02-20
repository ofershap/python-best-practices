# Python Best Practices

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Skills](https://img.shields.io/badge/skills.sh-python--best--practices-blue)](https://skills.sh/ofershap/python-best-practices)

Modern Python 3.12+ patterns your AI agent should use. Type hints with `X | Y` syntax, Pydantic v2,
uv package manager, match statements, `pathlib`, `pyproject.toml`, `TaskGroup`, and PEP 695
generics.

> AI coding assistants generate `from typing import List, Union, Optional`, use Pydantic v1
> decorators, create `setup.py`, and reach for `os.path` instead of `pathlib`. This plugin keeps
> your agent on Python 3.12+ patterns.

## Install

### Cursor / Claude Code / Windsurf

```bash
npx skills add ofershap/python-best-practices
```

Or copy `skills/` into your `.cursor/skills/` or `.claude/skills/` directory.

## What's Included

| Type    | Name                    | Description                                                                        |
| ------- | ----------------------- | ---------------------------------------------------------------------------------- |
| Skill   | `python-best-practices` | 15 rules for type hints, Pydantic v2, uv, pathlib, match/case, TaskGroup, and more |
| Rule    | `best-practices`        | Always-on behavioral rule that enforces Python 3.12+ patterns                      |
| Command | `/audit`                | Scan your codebase for outdated Python patterns                                    |

## What Agents Get Wrong

| What the agent writes                      | What Python 3.12+ uses                             |
| ------------------------------------------ | -------------------------------------------------- |
| `from typing import List, Union, Optional` | `list[str]`, `X \| Y`, `X \| None`                 |
| `@validator`, `@root_validator`            | `field_validator`, `model_validator` (Pydantic v2) |
| `class Config:` in Pydantic models         | `model_config = ConfigDict(...)`                   |
| `os.path.join()`, string paths             | `pathlib.Path` for all file operations             |
| `setup.py`, `requirements.txt`             | `pyproject.toml` with uv                           |
| `TypeVar("T")` + `Generic[T]`              | `def f[T](x: T) -> T` (PEP 695)                    |
| `asyncio.gather()`                         | `TaskGroup` for structured concurrency             |

## Related Plugins

- [fastapi-best-practices](https://github.com/ofershap/fastapi-best-practices) - FastAPI async
  patterns, Depends(), project structure
- [typescript-best-practices](https://github.com/ofershap/typescript-best-practices) - TypeScript
  5.x strict patterns

---

If this helped your workflow, a star helps others find it.

## Author

[![Made by ofershap](https://gitshow.dev/api/card/ofershap)](https://gitshow.dev/ofershap)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/ofershap)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github&logoColor=white)](https://github.com/ofershap)

## License

MIT
