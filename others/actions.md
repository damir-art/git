# GitHub Actions
**GitHub Actions** — это встроенная система CI/CD в GitHub, которая позволяет **автоматизировать всё, что угодно**, от тестов до деплоя, прямо при пуше, пулл-реквесте или даже по расписанию. Давай разложу по полочкам, как я умею:

---

## 🧠 Что такое GitHub Actions?

Это **инструмент для автоматического выполнения сценариев (workflows)**, которые ты описываешь в YAML-файлах внутри своего репозитория.

Формально:

> GitHub Actions — это система **контейнеризированного CI/CD**, которая запускает «действия» на серверах GitHub, когда происходят определённые события (push, pull request, release, и т.д.).

---

## 📦 Структура

Всё крутится вокруг вот этой магии:

```bash
.github/workflows/название_файла.yml
```

### Пример простого файла:

```yaml
name: Привет, GitHub Actions!

on: [push]

jobs:
  say-hello:
    runs-on: ubuntu-latest
    steps:
      - name: Клонируем репо
        uses: actions/checkout@v4

      - name: Приветствие
        run: echo "Привет из GitHub Actions 🎉"
```

---

## 🔧 Основные компоненты:

| Компонент | Описание                                                           |
| --------- | ------------------------------------------------------------------ |
| `on`      | Что запускает workflow (push, pull\_request, schedule, и т.д.)     |
| `jobs`    | Список задач, которые надо выполнить                               |
| `runs-on` | Где запускать задачу (например: `ubuntu-latest`, `windows-latest`) |
| `steps`   | Пошаговые команды или действия (actions), которые будут выполнены  |

---

## 🎯 Что можно делать с GitHub Actions?

* 🧪 Тестировать код (юнит-тесты, линтеры и т.д.)
* 🚀 Автоматически деплоить сайт, бот, сервер и т.д.
* ⚙️ Запускать cron-задачи (`schedule`)
* 📦 Публиковать пакеты (npm, PyPI, Docker)
* 💬 Отправлять уведомления в Telegram, Discord и т.д.
* 🕵️ Проверять PR на соответствие требованиям

---

## 🛠️ Типы действий (Actions):

* **Официальные** — от GitHub (`actions/checkout`, `actions/setup-node`, и т.д.)
* **Кастомные** — написаны другими пользователями или тобой (на JavaScript или Docker)
* **Локальные** — ты можешь писать их прямо внутри своего репо

---

## 🚀 Пример CI для Node.js проекта

```yaml
name: Node CI

on: [push]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4
      - name: Установка Node.js
        uses: actions/setup-node@v4
        with:
          node-version: 18

      - name: Установка зависимостей
        run: npm ci

      - name: Тесты
        run: npm test
```

---

## 📆 Cron (по расписанию)

```yaml
on:
  schedule:
    - cron: '0 3 * * 1' # Каждый понедельник в 03:00 UTC
```

---

## 📌 Где смотреть логи?

На GitHub в репозитории:
**Actions → выбираешь workflow → смотришь логи прямо в браузере.** Очень удобно!

---

## 🧠 Плюсы GitHub Actions:

* Не нужно настраивать Jenkins, Travis, CircleCI и т.п.
* Бесплатный тариф (2000 минут/мес на публичных и приватных репо)
* Полностью интегрирован в GitHub
* Можно кастомизировать под любые нужды

---

## ⚠️ На что обратить внимание?

* Если у тебя **приватный репозиторий**, есть лимиты минут (но можно докупить)
* Важно **кэшировать зависимости** (npm, pip и т.д.) для скорости
* Больше сложных задач = больше YAML и управления переменными

---

## 💥 Хочешь пример для своего проекта?

Скажи, что ты разрабатываешь (Node.js, Python, HTML+CSS, Docker?) — и я подгоню тебе workflow под ключ. Или хочешь сделать автоматическую публикацию сайта? Тоже сделаем!

---

Так что, Actions — это твой личный DevOps-бот. Только ты — главный дирижёр. Хочешь — пусть тестит, хочешь — пусть деплоит. Просто напиши ему это в YAML 😎

Хочешь продолжим и сделаем action под твой проект?
