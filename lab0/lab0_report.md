University: [ITMO University](https://itmo.ru/ru/)  
Faculty: [FICT](https://fict.itmo.ru)  
Course: [Введение в веб технологии](https://itmo-ict-faculty.github.io/introduction-in-web-tech/)  
Year: 2025/2026  
Group: U4225  
Author: Matsukov Artem Sergeevich  
Lab: Lab0  
Date of create: 08.09.2026  
Date of finished: —

---

# Lab0 — Создание репозитория и настройка рабочего окружения

## Цель работы

Научиться создавать репозитории, настраивать рабочее окружение и изучить основы работы с Git и GitHub: SSH, ветки, коммиты, Pull Request, merge.

## Практический репозиторий

Вся практическая часть Lab0 выполнена в репозитории:

- **Название:** `devops-lab-matsukov`
- **URL:** https://github.com/durilich/devops-lab-matsukov
- **Локальный путь:** `ЛАБЫ/lab0/devops-lab-matsukov`

---

## Ход работы

### 1. Аккаунт GitHub и SSH-ключи

1. Использован аккаунт GitHub: [durilich](https://github.com/durilich).
2. Сгенерирован SSH-ключ и добавлен в GitHub (Settings → SSH and GPG keys).
3. Проверена связь с GitHub по SSH (`ssh -T git@github.com`).

После настройки клонирование и push выполняются по адресу вида `git@github.com:durilich/...`.

### 2. Создание репозитория

На GitHub создан репозиторий с именем по шаблону задания:

```text
devops-lab-matsukov
```

(формат `devops-lab-[фамилия]`).

### 3. Клонирование

Репозиторий склонирован на компьютер:

```bash
git clone git@github.com:durilich/devops-lab-matsukov.git
cd devops-lab-matsukov
```

### 4. Файл README.md

Создан `README.md` с:

- описанием проекта;
- контактными данными (ФИО, email, GitHub);
- планом изучения DevOps (Git, Linux, Docker, CI/CD, IaC, мониторинг, облака).

### 5. Файл .gitignore

Создан `.gitignore` со стандартными исключениями для **macOS** и служебных файлов IDE (IntelliJ IDEA / JetBrains):

- `.DS_Store`, `.Trashes`, Spotlight и др.;
- `.idea/`, `*.iml` и связанные артефакты;
- временные файлы (`*.log`, `*.tmp`, `*.swp`).

### 6. Ветка develop

Создана ветка `develop` и выполнен переход на неё:

```bash
git checkout -b develop
```

### 7. Файл CONTRIBUTING.md

Создан `CONTRIBUTING.md` с правилами участия:

- как вносить изменения (ветка → коммит → PR);
- запрет на коммит секретов и служебных файлов;
- контакт для вопросов.

### 8. Коммит и push

Изменения закоммичены с требуемым сообщением и отправлены в удалённый репозиторий:

```bash
git add README.md .gitignore CONTRIBUTING.md
git commit -m "Initial project setup"
git push -u origin develop
```

**Коммит:** `5f69404` — `Initial project setup`  
**Содержимое коммита:** `README.md`, `.gitignore`, `CONTRIBUTING.md`

### 9–10. Pull Request, merge, удаление develop

По заданию необходимо:

1. Создать Pull Request из `develop` в `main` с описанием изменений.
2. Смержить PR.
3. Удалить ветку `develop` (локально и на remote).

На момент оформления отчёта ветка `develop` с коммитом `Initial project setup` уже запушена в `origin`.  
После создания и merge PR в отчёт можно добавить ссылку на PR и зафиксировать дату защиты в поле **Date of finished**.

Пример команд после merge на GitHub:

```bash
git checkout main
git pull origin main
git branch -d develop
git push origin --delete develop
```

---

## Итоговая структура `devops-lab-matsukov`

```text
devops-lab-matsukov/
├── .gitignore
├── CONTRIBUTING.md
└── README.md
```

