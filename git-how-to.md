# Git & GitHub Инструкция

## 1. Создание SSH-ключа

```bash
# Генерация ключа (Ed25519 - более современный чем RSA)
ssh-keygen -t ed25519 -C "your_email@example.com"

Для своего ключа можно пропустить ввод пароля
Называем ключ  через.ssh/key_1

## 2. Добавление SSH-ключа в GitHub

1. Добавляем ключ:
 ```bash
   - Открываем [GitHub SSH Keys](https://github.com/settings/keys)
   - "New SSH key"
   - Вставляем содержимое (начинается с `ssh-ed25519...`)
   - Сохраняем

2. Проверяем подключение:
   ssh -T git@github.com
   ```
   *(Должно появиться "You've successfully authenticated")*

## 3. Клонирование репозитория

```bash
# Через SSH (рекомендуется)
git clone git@github.com:username/repo.git
```