# LibreChat – Docker + OpenAI + MCP

## Описание
Быстрый запуск LibreChat с:
- OpenAI API
- Пресетами моделей
- MCP для работы с файлами
- MongoDB для хранения данных

---

## Структура
- `.env.example` — шаблон с переменным окружения
- `.env.local` — приватные значения (в .gitignore)
- `docker-compose.yml` — Docker сервисы
- `librechat.yaml` — конфигурация + mcp + пресеты

---

## Запуск
```bash
cp .env.example .env.local # скопировать шаблон, заполнить секреты
mkdir -p data
docker compose up -d --force-recreate
```

Открой [http://localhost:3080](http://localhost:3080) → выбери нужный пресет.

---

## Примечания
- MCP доступен в `./data`
- Настройки моделей → `librechat.yaml`
