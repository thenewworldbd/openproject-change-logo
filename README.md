# 🚀 OpenProject Custom Logo Setup

Полное руководство по замене логотипов OpenProject в Docker-контейнере

---

## 📦 Требования

- Docker + Docker Compose
- OpenProject (Docker)
- Доступ к серверу
- PNG логотипы

---

## 📁 Структура проекта

```bash
/opt/openproject/openproject/
├── docker-compose.yml
├── tmp/
│   ├── logo-white.png
│   └── logo-black.png
└── README.md

## 🔧 Инструкция
1. Создать папку
cd /opt/openproject/openproject
mkdir -p tmp

2. Найти оригинальные логотипы
docker compose exec web find /app/public/assets -name "*logo*.png"
3. Подменить файлы
cp ./light-logo.png ./tmp/logo-white-bg-ua-XXXX.png
cp ./dark-logo.png ./tmp/logo-black-bg-ua-XXXX.png
4. Добавить volumes
services:
  web:
    volumes:
      - "./tmp/logo-white-bg-ua-XXXX.png:/app/public/assets/logo-white-bg-ua-XXXX.png"
      - "./tmp/logo-black-bg-ua-XXXX.png:/app/public/assets/logo-black-bg-ua-XXXX.png"
5. Перезапуск
docker compose stop web
docker compose rm -f web
docker compose up -d web
✅ Проверка
docker compose exec web ls -la /app/public/assets | grep logo

Очистить кэш браузера (Ctrl + F5)
