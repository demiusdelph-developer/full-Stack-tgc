# Основи розробки

Перший етап створює фундамент для подальшого навчання Full Stack. Тут ви дізнаєтесь, як працює веб, налаштуєте робоче середовище та навчитесь зберігати код у Git і GitHub.

## Цілі етапу

Після завершення ви зможете:

- пояснити шлях запиту від браузера до сервера;
- користуватись терміналом для роботи з файлами й Git;
- створювати репозиторії, commits і гілки;
- публікувати власний код на GitHub;
- налаштувати VS Code для щоденної розробки.

## 1. Як працює веб

### Клієнт, сервер і браузер

- **Клієнт** - браузер або застосунок, з якого користувач надсилає запит.
- **Сервер** - програма або комп'ютер, що отримує запит, виконує логіку та повертає відповідь.
- **Браузер** - завантажує HTML, CSS і JavaScript та відображає вебсторінку.
- **API** - інтерфейс, через який frontend і backend обмінюються даними.

### DNS, URL та HTTP

1. Користувач вводить URL, наприклад `https://example.com`.
2. DNS знаходить IP-адресу сервера для домену.
3. Браузер надсилає HTTP-запит, наприклад `GET /`.
4. Сервер повертає HTTP-відповідь: статус, заголовки та дані.
5. Браузер завантажує пов'язані ресурси й рендерить сторінку.

Корисні HTTP-методи: `GET` для читання даних, `POST` для створення, `PUT` або `PATCH` для оновлення, `DELETE` для видалення. Поширені статуси: `200 OK`, `201 Created`, `400 Bad Request`, `401 Unauthorized`, `404 Not Found`, `500 Internal Server Error`.

## 2. Робоче середовище

Встановіть:

- [Git](https://git-scm.com/downloads);
- [Visual Studio Code](https://code.visualstudio.com/);
- сучасний браузер: Chrome, Edge або Firefox;
- [Node.js LTS](https://nodejs.org/) - він знадобиться на наступних етапах.

У VS Code встановіть розширення **Prettier - Code formatter**, **ESLint** і **GitLens**. Увімкніть автоматичне форматування під час збереження файлу.

## 3. Командний рядок

Відкрийте PowerShell або вбудований термінал VS Code. Основні команди:

```powershell
Get-Location              # поточна папка
Get-ChildItem             # список файлів
Set-Location path\to\dir  # перехід до папки
New-Item notes.txt        # створення файлу
New-Item project -ItemType Directory  # створення папки
```

Практика:

1. Створіть папку `fullstack-learning`.
2. У ній створіть папку `foundations`.
3. Створіть файл `notes.md`.
4. Відкрийте цю папку у VS Code командою `code .`.

## 4. Git

Git зберігає історію змін проєкту локально. Commit - це зафіксований зріз змін із коротким зрозумілим повідомленням.

Налаштуйте автора commits один раз:

```powershell
git config --global user.name "Ваше ім'я"
git config --global user.email "ваш-email@example.com"
```

Базовий робочий цикл:

```powershell
git init
git status
git add .
git commit -m "docs: add first notes"
git log --oneline
```

Створення окремої гілки:

```powershell
git switch -c practice/git-basics
git branch
```

Не додавайте до Git паролі, токени, ключі доступу або файли `.env`. Для цього використовуйте `.gitignore`.

## 5. GitHub

GitHub зберігає Git-репозиторії віддалено та дозволяє працювати над кодом разом.

1. Створіть акаунт на [GitHub](https://github.com/), якщо його ще немає.
2. Створіть порожній репозиторій `fullstack-learning`.
3. Прив'яжіть локальний репозиторій і надішліть перший commit:

```powershell
git remote add origin https://github.com/USERNAME/fullstack-learning.git
git branch -M main
git push -u origin main
```

Для кожної нової функції створюйте гілку, публікуйте її через `git push -u origin NAME`, а потім створюйте pull request.

## Практичне завдання

Створіть репозиторій `web-foundations` із такою структурою:

```text
web-foundations/
├── README.md
├── notes/
│   ├── web-basics.md
│   ├── terminal.md
│   └── git.md
└── .gitignore
```

У `README.md` коротко напишіть, що ви вивчили. Зробіть щонайменше три логічні commits:

1. `docs: add web request notes`
2. `docs: add terminal practice notes`
3. `docs: add Git workflow notes`

## Чекліст завершення

- [ ] Я пояснюю різницю між клієнтом, сервером і API.
- [ ] Я розумію, для чого потрібні DNS, URL, HTTP-запит і HTTP-відповідь.
- [ ] Я вмію переходити між папками й створювати файли в терміналі.
- [ ] Я вмію створити Git-репозиторій, commit і гілку.
- [ ] Я вмію відправити проєкт на GitHub.
- [ ] У мене є опублікований репозиторій із notes і зрозумілим README.

## Навігація за етапами

[Основи розробки](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/01-development-foundations) · [HTML та CSS](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/02-html-css) · [JavaScript](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/03-javascript) · [TypeScript](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/04-typescript) · [React frontend](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/05-react-frontend) · [Node.js та backend](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/06-nodejs-backend) · [Бази даних](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/07-databases) · [Авторизація та безпека](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/08-authentication-security) · [Тестування](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/09-testing) · [Деплой і DevOps](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/10-deployment-devops) · [Портфоліо](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/11-portfolio)

[Переглянути розгорнутий навчальний план](https://github.com/demiusdelph-developer/full-Stack-tgc#full-stack-learning-roadmap)
