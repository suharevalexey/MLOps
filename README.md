# Работа с инструментами Python: Ruff и ty

В `src/myproject/main.py` код с ошибками для проверки библиотек Ruff и ty
Настройки инструментов в `pyproject.toml`.

## Запуск

Из корня проекта:

```powershell
uv sync
uv run ruff check .
uv run ruff format --check .
uv run ty check
```

## Настройки

- `tool.ruff`: Python 3.13 и максимальная длина строки 88 символов.
- `tool.ruff.lint.select`: правила стиля `E`, проверки `F`, сортировка импортов `I`.
- `tool.ty.environment`: проверка для Python 3.13.
- `tool.ty.rules`: три выбранных нарушения типов имеют уровень `error`.

Документация: [Ruff](https://docs.astral.sh/ruff/configuration/),
[ty](https://docs.astral.sh/ty/configuration/).
