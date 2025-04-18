# Инструкция по работе с ветками в Git

## Как получить ветку с сервера

1. **Обновить список веток с удалённого репозитория**:
   git fetch --all
Переключиться на нужную ветку (если она уже отслеживается):

git checkout имя_ветки
Если ветка новая и её нет локально, создать её и переключиться:


git checkout -b имя_ветки origin/имя_ветки
Как слить одну ветку с другой
Перейти в ветку, в которую нужно влить изменения (например, main):


git checkout main
Выполнить слияние с нужной веткой (например, feature-branch):


git merge feature-branch
Если возникли конфликты, разрешить их:

Открыть файлы с конфликтами, исправить их.

Добавить исправленные файлы:


git add имя_файла
Продолжить слияние:


git merge --continue
Что сделать после слияния веток
Проверить статус репозитория:


git status
Убедиться, что всё работает (запустить тесты, проверить изменения).

Отправить изменения на удалённый репозиторий:


git push origin имя_ветки
Если ветка больше не нужна, её можно удалить:

Локально:


git branch -d имя_ветки
На удалённом репозитории:


git push origin --delete имя_ветки
Обновить основную ветку (если нужно):


git pull origin main
Copy

### Как добавить файл в репозиторий:
1. Сохраните этот текст в файл `merge-how-to.md`.
2. Добавьте его в Git:
   ```bash
   git add merge-how-to.md
Зафиксируйте изменения:

bash
Copy
git commit -m "Добавлена инструкция по слиянию веток"
Отправьте на сервер:

bash
Copy
git push origin имя_ветки