# Инструкция по переименованию репозитория

## Шаг 1: Переименование на GitHub

1. Перейдите на страницу репозитория: https://github.com/kobyzev-yuri/lse-about.md
2. Нажмите на кнопку **Settings** (в верхней панели репозитория)
3. Прокрутите вниз до секции **Repository name**
4. Измените название с `lse-about.md` на `lse`
5. Нажмите **Rename**

GitHub автоматически перенаправит все ссылки на новое имя.

## Шаг 2: Обновление remote URL в локальном репозитории

После переименования на GitHub выполните:

```bash
cd /mnt/ai/cnn/lse
git remote set-url origin https://github.com/kobyzev-yuri/lse.git
git remote -v  # Проверьте, что URL обновлен
```

## Альтернативный способ (если уже переименовали)

Если вы уже переименовали репозиторий на GitHub, просто выполните:

```bash
cd /mnt/ai/cnn/lse
git remote set-url origin https://github.com/kobyzev-yuri/lse.git
```

## Проверка

После обновления remote URL проверьте:

```bash
git remote -v
```

Должно показать:
```
origin  https://github.com/kobyzev-yuri/lse.git (fetch)
origin  https://github.com/kobyzev-yuri/lse.git (push)
```

---

**Примечание**: После переименования старый URL (`lse-about.md`) будет автоматически перенаправлять на новый (`lse`), но лучше обновить все ссылки.

