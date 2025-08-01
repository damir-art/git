# Работа с git
Устанавливаем програму: https://git-scm.com (куча окон при утсановке, сделай гайд).

Настраиваем логин и почту, котрые будут видны при комитах.

```bash
git config --global user.name "Твоё имя"
git config --global user.email "твоя@почта.com"
```

Переходим в репозиторий:

```bash
git status # узнаём текущее состояние репозитория
git init # инициализируем репозиторий (если не склонировал с помощью Github Desktop)
```

Работа с проектом:
```bash
git status        # Проверяешь изменения
git add file.txt  # Добавляешь нужное в индекс или все git add .
git status        # Убедился, что всё правильно
git commit -m "Добавил важный файл" # Создаёт снимок изменений
git push          # Отправляет коммиты на GitHub
git pull          # Забирает обновления с GitHub
```

Команды:
status, add, push, pull, checkout, diff, init, log, reset, restore, stash, switch