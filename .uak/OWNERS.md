# Shared-file owners

One writer per shared file. Others ask the owner with `uak msg ID --kind request`. Patterns are relative, with no spaces; directories end in `/`.
An owner is not a prerequisite for everyone: consumers work on published contracts and mocks. To transfer ownership, open a PR to main.

| Pattern | Owner task |
|---|---|
| pyproject.toml | APP-002 |
| uv.lock | APP-002 |
| app/main.py | APP-001 |
| .github/workflows/ | APP-001 |
| .uak/PROJECT.md | APP-001 |

Delete rows for technologies you don't use. `/uak-plan` creates APP-001 (setup) and APP-002 (contract).
