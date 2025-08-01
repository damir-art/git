# Что такое инициализация репозитория?
## 🚀 Что делает `git init`

Команда:

```bash
git init
```

Инициализирует (то есть **создаёт**) **новый репозиторий Git** в текущей папке. Это превращает обычную папку на твоём компьютере в **репозиторий**, где Git начинает отслеживать изменения файлов.

---

## 🧠 Что происходит "под капотом"

Когда ты вводишь `git init`, Git:

1. Создаёт в папке скрытую директорию **`.git`** — это **мозг** репозитория.
2. Там хранится:
   * История коммитов
   * Ветки
   * Настройки
   * И вся информация, необходимая для отслеживания изменений
3. С этого момента ты можешь:
   * Делать `git add`, `git commit`, `git log` и т.д.
   * Подключать удалённый репозиторий (`git remote add origin ...`)
   * Пушить в GitHub или GitLab

---

## 🛠️ Когда нужно использовать `git init`

Ты запускаешь `git init` в таких случаях:

| Сценарий                                       | Нужно ли `git init`         |
| ---------------------------------------------- | --------------------------- |
| Хочешь создать новый проект с Git              | ✅ Да                        |
| Склонировал репозиторий с GitHub (`git clone`) | ❌ Нет — уже инициализирован |
| Работаешь в существующем проекте с `.git`      | ❌ Нет                       |
| Создаёшь свою "песочницу" для экспериментов    | ✅ Почему бы и нет!          |

---

## 🛡️ Пример:

```bash
mkdir my-project
cd my-project
git init
```

Теперь ты можешь создавать файлы, делать `git add .`, `git commit -m "Первый коммит"` и так далее.

---

## ❗Важно:

Если ты уже клонировал репозиторий с GitHub через GitHub Desktop — `git init` **уже сделан за тебя**! Тебе не надо его вызывать второй раз.

---
