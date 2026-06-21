# Skvortsov ADV

Лендинг маркетингового агентства роста — Павел Скворцов (Fractional CMO).

Статический сайт без сборки (HTML/CSS/JS). Хостится на **GitHub Pages**,
домен **skvortsovadv.ru** (надёжно открывается в России, в отличие от Cloudflare/Vercel).

## Структура
- `index.html` — страница (весь текст здесь)
- `styles.css` / `script.js` — стили и логика (форма заявки, мобильное меню)
- `CNAME` — кастомный домен для GitHub Pages
- `robots.txt`, `sitemap.xml`, `favicon.svg`, `og-image.png` — SEO/иконки
- `n8n_lead_webhook.json` — шаблон воркфлоу n8n для приёма заявок (Telegram + Email)

## Деплой
Pages публикует ветку `main` (корень) автоматически при каждом пуше.

## Приём заявок
Форма шлёт данные на webhook из `script.js` (`LEAD_WEBHOOK_URL`). Импортируйте
`n8n_lead_webhook.json` в n8n, впишите Telegram chat_id и SMTP, вставьте URL вебхука.
Пока URL пустой — форма открывает почту и предлагает Telegram, чтобы лиды не терялись.
