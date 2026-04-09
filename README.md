```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OpenProject Custom Logo Setup</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            color: #24292e;
            background: #fff;
            padding: 2rem;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: #fff;
            border-radius: 8px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
            overflow: hidden;
        }

        .header {
            background: linear-gradient(135deg, #1a6d9c 0%, #0d4b6e 100%);
            color: white;
            padding: 3rem 2rem;
            text-align: center;
        }

        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            font-weight: 600;
        }

        .header p {
            font-size: 1.2rem;
            opacity: 0.95;
        }

        .badge-container {
            margin-top: 1rem;
        }

        .badge {
            display: inline-block;
            background: rgba(255,255,255,0.2);
            padding: 0.3rem 0.8rem;
            border-radius: 20px;
            margin: 0 0.3rem;
            font-size: 0.85rem;
        }

        .content {
            padding: 2rem;
        }

        h2 {
            color: #1a6d9c;
            margin-top: 2rem;
            margin-bottom: 1rem;
            padding-bottom: 0.5rem;
            border-bottom: 2px solid #e1e4e8;
            font-size: 1.5rem;
        }

        h3 {
            color: #0d4b6e;
            margin-top: 1.5rem;
            margin-bottom: 0.75rem;
            font-size: 1.25rem;
        }

        .step {
            background: #f6f8fa;
            border-left: 4px solid #1a6d9c;
            padding: 1.5rem;
            margin: 1.5rem 0;
            border-radius: 6px;
        }

        .step-number {
            display: inline-block;
            background: #1a6d9c;
            color: white;
            width: 28px;
            height: 28px;
            text-align: center;
            line-height: 28px;
            border-radius: 50%;
            font-weight: bold;
            margin-right: 0.5rem;
            font-size: 0.9rem;
        }

        code {
            background: #f1f1f1;
            padding: 0.2rem 0.4rem;
            border-radius: 3px;
            font-family: 'SF Mono', Monaco, 'Cascadia Code', monospace;
            font-size: 0.85rem;
            color: #d73a49;
        }

        pre {
            background: #24292e;
            color: #e1e4e8;
            padding: 1rem;
            border-radius: 6px;
            overflow-x: auto;
            margin: 1rem 0;
            font-size: 0.85rem;
            line-height: 1.45;
        }

        pre code {
            background: none;
            color: inherit;
            padding: 0;
        }

        .screenshot {
            text-align: center;
            margin: 2rem 0;
            padding: 1rem;
            background: #f6f8fa;
            border-radius: 8px;
        }

        .screenshot img {
            max-width: 100%;
            border-radius: 6px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }

        .screenshot-caption {
            margin-top: 0.75rem;
            color: #586069;
            font-size: 0.9rem;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin: 1rem 0;
        }

        th, td {
            border: 1px solid #e1e4e8;
            padding: 0.75rem;
            text-align: left;
        }

        th {
            background: #f6f8fa;
            font-weight: 600;
        }

        .info-box {
            background: #e8f4f8;
            border-left: 4px solid #1a6d9c;
            padding: 1rem;
            margin: 1rem 0;
            border-radius: 4px;
        }

        .warning-box {
            background: #fff5e8;
            border-left: 4px solid #f66a0a;
            padding: 1rem;
            margin: 1rem 0;
            border-radius: 4px;
        }

        .success-box {
            background: #e8f8e8;
            border-left: 4px solid #28a745;
            padding: 1rem;
            margin: 1rem 0;
            border-radius: 4px;
        }

        .footer {
            background: #f6f8fa;
            text-align: center;
            padding: 2rem;
            color: #586069;
            border-top: 1px solid #e1e4e8;
        }

        .tree {
            background: #f6f8fa;
            padding: 1rem;
            border-radius: 6px;
            font-family: monospace;
            margin: 1rem 0;
        }

        @media (max-width: 768px) {
            body {
                padding: 0;
            }
            .content {
                padding: 1rem;
            }
            .header h1 {
                font-size: 1.75rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🚀 OpenProject Custom Logo Setup</h1>
            <p>Полное руководство по замене логотипов в Docker-контейнере</p>
            <div class="badge-container">
                <span class="badge">OpenProject 17</span>
                <span class="badge">Docker Compose</span>
                <span class="badge">Volume Mounting</span>
                <span class="badge">Production Ready</span>
            </div>
        </div>

        <div class="content">
            <!-- Скриншот -->
            <div class="screenshot">
                <img src="https://github.com/user-attachments/assets/9f8c03c6-6471-4f22-9e34-7ddaa3566f52" alt="Пример успешной замены логотипа">
                <div class="screenshot-caption">✅ Результат после замены логотипа</div>
            </div>

            <!-- Оглавление -->
            <h2>📋 Содержание</h2>
            <ul style="margin-bottom: 2rem; columns: 2; list-style-position: inside;">
                <li><a href="#requirements" style="color: #1a6d9c;">Предварительные требования</a></li>
                <li><a href="#structure" style="color: #1a6d9c;">Структура проекта</a></li>
                <li><a href="#steps" style="color: #1a6d9c;">Пошаговая инструкция</a></li>
                <li><a href="#verify" style="color: #1a6d9c;">Проверка результата</a></li>
                <li><a href="#troubleshooting" style="color: #1a6d9c;">Устранение проблем</a></li>
                <li><a href="#commands" style="color: #1a6d9c;">Полезные команды</a></li>
            </ul>

            <!-- Предварительные требования -->
            <h2 id="requirements">📦 Предварительные требования</h2>
            <ul>
                <li>Установленный Docker и Docker Compose</li>
                <li>Проект OpenProject, развернутый через Docker</li>
                <li>Доступ к файловой системе сервера</li>
                <li>Подготовленные файлы логотипов (PNG)</li>
            </ul>

            <div class="info-box">
                💡 <strong>Примечание:</strong> Имена файлов логотипов содержат уникальные хеши. Важно точно скопировать имена из вашего контейнера.
            </div>

            <!-- Структура -->
            <h2 id="structure">📁 Структура проекта</h2>
            <div class="tree">
                <pre style="background: none; padding: 0; margin: 0;"><code>/opt/openproject/openproject/
├── docker-compose.yml          # Основной конфиг Docker
├── tmp/                        # Папка с кастомными логотипами
│   ├── logo-white-bg-ua-*.png  # Светлый логотип
│   └── logo-black-bg-ua-*.png  # Тёмный логотип
└── README.md                   # Документация</code></pre>
            </div>

            <!-- Инструкция -->
            <h2 id="steps">🔧 Пошаговая инструкция</h2>

            <div class="step">
                <strong><span class="step-number">1</span> Создайте папку <code>tmp</code> в корне проекта</strong>
                <pre><code>cd /opt/openproject/openproject
mkdir -p tmp</code></pre>
            </div>

            <div class="step">
                <strong><span class="step-number">2</span> Подготовьте файлы логотипов</strong>
                <pre><code># Скопируйте ваши логотипы в папку tmp с правильными именами
cp /path/to/your/light-logo.png ./tmp/logo-white-bg-ua-1524d9ac40e1bc2f0e6d3cf499704cc40318e0ff3e46e2678cb91e9f3fadd426.png
cp /path/to/your/dark-logo.png ./tmp/logo-black-bg-ua-3ac60ba3fde04b597a904611d9295ad7705d6d55d4fd77441e5307d8cded70ae.png</code></pre>
            </div>

            <div class="step">
                <strong><span class="step-number">3</span> Подмените <code>docker-compose.yml</code></strong>
                <p>Добавьте секцию <code>volumes</code> в сервис <code>web</code>:</p>
                <pre><code>services:
  web:
    # ... остальные настройки ...
    volumes:
      - "./tmp/logo-white-bg-ua-1524d9ac40e1bc2f0e6d3cf499704cc40318e0ff3e46e2678cb91e9f3fadd426.png:/app/public/assets/logo-white-bg-ua-1524d9ac40e1bc2f0e6d3cf499704cc40318e0ff3e46e2678cb91e9f3fadd426.png"
      - "./tmp/logo-black-bg-ua-3ac60ba3fde04b597a904611d9295ad7705d6d55d4fd77441e5307d8cded70ae.png:/app/public/assets/logo-black-bg-ua-3ac60ba3fde04b597a904611d9295ad7705d6d55d4fd77441e5307d8cded70ae.png"</code></pre>
            </div>

            <div class="step">
                <strong><span class="step-number">4</span> Пересоберите и перезапустите контейнеры</strong>
                <pre><code># Остановите и удалите web контейнер
docker compose stop web
docker compose rm -f web

# Запустите заново
docker compose up -d web

# Проверьте монтирование
docker compose exec web ls -la /app/public/assets/ | grep logo</code></pre>
            </div>

            <!-- Проверка -->
            <h2 id="verify">✅ Проверка результата</h2>
            <ul>
                <li><strong>Очистите кэш браузера:</strong> <code>Ctrl + Shift + Delete</code> или режим инкогнито</li>
                <li><strong>Проверьте светлую тему:</strong> должен отображаться <code>logo-white-bg-ua</code></li>
                <li><strong>Проверьте тёмную тему:</strong> должен отображаться <code>logo-black-bg-ua</code></li>
                <li><strong>DevTools:</strong> F12 → Network → найти файл логотипа</li>
            </ul>

            <div class="success-box">
                🎉 <strong>Готово!</strong> Если вы видите свой логотип — всё работает правильно.
            </div>

            <!-- Устранение проблем -->
            <h2 id="troubleshooting">🐛 Устранение проблем</h2>
            <table>
                <thead>
                    <tr>
                        <th>Проблема</th>
                        <th>Решение</th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td>Логотип не обновляется</td>
                        <td>Очистите кэш браузера (Ctrl+F5) или откройте в режиме инкогнито</td>
                    </tr>
                    <tr>
                        <td>Ошибка "not a directory"</td>
                        <td>Проверьте существование файла в папке <code>tmp/</code></td>
                    </tr>
                    <tr>
                        <td>Файл имеет старую дату</td>
                        <td>Пересоздайте контейнер: <code>docker compose rm -f web && docker compose up -d web</code></td>
                    </tr>
                    <tr>
                        <td>Логотип не соответствует теме</td>
                        <td>Замените оба файла (светлый и тёмный) или скопируйте светлый поверх тёмного</td>
                    </tr>
                    <tr>
                        <td>Ошибка монтирования</td>
                        <td>Убедитесь, что пути в volume абсолютные или относительно docker-compose.yml</td>
                    </tr>
                </tbody>
            </table>

            <!-- Полезные команды -->
            <h2 id="commands">⌨️ Полезные команды</h2>
            <pre><code># Просмотр логов web контейнера
docker compose logs web -f

# Вход в контейнер
docker compose exec web bash

# Поиск всех логотипов в контейнере
docker compose exec web find /app/public/assets -name "*logo*.png"

# Копирование файла из контейнера на хост
docker compose cp web:/app/public/assets/logo-white-bg-ua-*.png ./tmp/

# Просмотр информации о монтировании
docker inspect openproject-web-1 | grep -A 10 "Mounts"

# Принудительная перекомпиляция ассетов
docker compose exec web bash -c "cd /app && RAILS_ENV=production bundle exec rake assets:precompile"</code></pre>

            <!-- Альтернативный метод -->
            <h2>🔄 Альтернативный метод (без volume)</h2>
            <p>Если вы не хотите редактировать <code>docker-compose.yml</code>, можно использовать <code>docker cp</code>:</p>
            <pre><code># Скопируйте файл в контейнер
docker compose cp ./tmp/your-logo.png web:/app/public/assets/logo-white-bg-ua-1524d9ac40e1bc2f0e6d3cf499704cc40318e0ff3e46e2678cb91e9f3fadd426.png

# Замените все логотипы
docker compose exec web bash -c '
  for file in /app/public/assets/*logo*.png; do
    cp /app/public/assets/logo-white-bg-ua-1524d9ac40e1bc2f0e6d3cf499704cc40318e0ff3e46e2678cb91e9f3fadd426.png "$file"
  done
'

# Очистите кэш
docker compose exec web rm -rf tmp/cache/*</code></pre>

            <div class="warning-box">
                ⚠️ <strong>Внимание:</strong> Метод с <code>docker cp</code> не сохраняет изменения после перезапуска контейнера. Для постоянного эффекта используйте volume.
            </div>

            <!-- Часто задаваемые вопросы -->
            <h2>❓ Часто задаваемые вопросы</h2>
            <details style="margin-bottom: 1rem;">
                <summary style="cursor: pointer; font-weight: bold; color: #1a6d9c;">Как узнать точные имена файлов в моём контейнере?</summary>
                <pre style="margin-top: 0.5rem;"><code>docker compose exec web find /app/public/assets -name "*logo*.png"</code></pre>
            </details>
            <details style="margin-bottom: 1rem;">
                <summary style="cursor: pointer; font-weight: bold; color: #1a6d9c;">Нужно ли пересобирать все контейнеры или только web?</summary>
                <p>Достаточно пересоздать только <code>web</code> контейнер, так как только он отвечает за отображение ассетов.</p>
            </details>
            <details style="margin-bottom: 1rem;">
                <summary style="cursor: pointer; font-weight: bold; color: #1a6d9c;">Поддерживаются ли другие форматы (SVG, JPG)?</summary>
                <p>OpenProject использует PNG для логотипов. Рекомендуется использовать PNG с прозрачностью для лучшего результата.</p>
            </details>
        </div>

        <div class="footer">
            <p>📄 OpenProject распространяется под лицензией GPLv3</p>
            <p>Сделано с ❤️ для OpenProject Community</p>
            <p style="margin-top: 0.5rem; font-size: 0.85rem;">
                <a href="https://www.openproject.org" style="color: #1a6d9c;">Официальный сайт</a> •
                <a href="https://github.com/opf/openproject" style="color: #1a6d9c;">GitHub репозиторий</a>
            </p>
        </div>
    </div>
</body>
</html>
```
