# LibreChat – Docker + OpenAI + MCP

## Описание
Этот репозиторий позволяет быстро развернуть **LibreChat** с:
- Поддержкой OpenAI API через `${OPENAI_API_KEY}`
- Тремя преднастроенными пресетами моделей
- Доступом к локальным файлам через MCP (`./data`)
- Хранением чатов в MongoDB

Файл `.env.example` содержит шаблон переменных окружения, реальные значения задаются в `.env.local`, который не коммитится.

---

## Структура проекта
- `.env.example` — шаблон переменных окружения
- `.env.local` — локальные значения (игнорируются Git)
- `docker-compose.yml` — описание Docker сервисов
- `librechat.yaml` — конфигурация LibreChat (OpenAI, MCP, пресеты)
- `.gitignore` — исключает приватные файлы

---

## Быстрый старт
1. Скопируйте шаблон переменных:
   ```bash
   cp .env.example .env.local
   ```

2. Заполните `.env.local` нужными значениями:
   - `MONGO_URI
   - `OPENAI_API_KEY`
   - `JWT_SECRET` и другие секреты

3. Запустите контейнеры:
   ```bash
   mkdir -p data
   docker compose up -d --force-recreate
   ```

4. Откройте [http://localhost:3080](http://localhost:3080) и выберите нужный пресет:
   - Everyday Chat
   - Coding Assistant
   - Coding Junior

---

## Примечания
- MCP доступен в папке \`./data\`
- Все конфиги хранятся в \`librechat.yaml\`
