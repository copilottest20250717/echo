# DSH — офлайн-набор документации DeepSeek Harness

Локальная копия официальной документации DeepSeek Harness (dsh), выгруженная, чтобы
проектировать двойника без постоянных обращений в сеть.

## Источник и версия

1. Репозиторий: https://github.com/deepseek-ai/deepseek-harness
2. Ветка/коммит: `master` @ `21638c56315ae6a2b552d6091945d3144c9af32e`
3. Дата выгрузки: 2026-09-28
4. Лицензия upstream: MIT

## Что включено

1. Корневые документы репозитория: `README.md`, `AGENTS.md`, `SAFETY.md`, `CONTRIBUTING.md`, `BENCHMARK.md`, `BRAND_GUIDELINES.md`, `THIRD_PARTY_NOTICES.md`.
2. Каталог `docs/` — вся англоязычная документация (архитектура, подсистемы, гайды, cookbook, Cordis API и туториалы, каталоги, postmortem).
3. `packages/bundle/*/README.md` — описания профилей сборки (base, headless, web-app, sdk-app, sdk-minimal, acp-app).
4. `python/sdk/README.md` и `python/sdk/examples/README.md` — Python SDK.
5. `apps/cli/reference/README.md` — справка по CLI.

## Что исключено

1. Китайские дубликаты (`*.zh.md`) и файлы переводов (`*.i18n.yaml`).
2. Изображения (`*.png`) и схемы сессий (`*.schema.json` оставлены, где относились к документам).
3. Исходный код и бинарные артефакты upstream.

## Навигация по ключевым документам

1. `docs/architecture.md` — архитектура фреймворка, микроядро Cordis, жизненный цикл плагинов.
2. `docs/cordis-primer.md` и `docs/cordis-tutorial/` — введение и туториал по Cordis.
3. `docs/cordis-api/` — API контекста, событий, fiber, registry, service.
4. `docs/subsystems/` — описания подсистем: session, tools, skills, subagent, workflow, plan, goal, schedule, mcp, storage, sandbox, system-prompt и др.
5. `docs/tool-catalog.md`, `docs/config-catalog.md`, `docs/capability-seams.md` — каталоги возможностей и конфигурации.
6. `docs/glossary.md` — терминология.
7. `docs/user/guide/` — Web UI, провайдеры моделей, Python SDK, MCP memory, schedule, GitHub review.
8. `docs/user/develop/` — разработка плагинов и инструментов (basic, framework, practice).
9. `docs/development.md`, `docs/testing.md` — сборка и тесты.
10. `docs/persistence-*` — форматы и история форматов сессий.

## Обновление набора

```
git clone --depth 1 --filter=blob:none --sparse https://github.com/deepseek-ai/deepseek-harness.git dsh-src
git -C dsh-src sparse-checkout set docs
```

Затем скопировать англоязычные `*.md` и `*.json` из `dsh-src/docs` в этот каталог,
а корневые документы и README профилей — в соответствующие подпапки.
