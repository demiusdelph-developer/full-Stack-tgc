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

### Домен та IP-адреса

**IP-адреса** - це числова адреса пристрою в мережі. Вона потрібна, щоб інші пристрої могли знайти саме цей сервер. Наприклад, IPv4-адреса має вигляд `142.250.74.142`. Сервер сайту, ваш роутер і комп'ютер мають IP-адреси.

**Домен** - це зручне для людини ім'я сайту, наприклад `github.com` або `example.com`. Запам'ятати назву набагато легше, ніж число IP-адреси. Один домен може мати кілька IP-адрес, а одна IP-адреса може обслуговувати кілька сайтів.

### DNS

**DNS (Domain Name System)** - це система, яка перекладає доменне ім'я на IP-адресу. Її можна уявити як телефонну книгу інтернету: ви знаєте ім'я контакту, а DNS знаходить його номер.

Коли ви відкриваєте `github.com`, браузер не знає, до якого сервера підключатися. Він звертається до DNS-сервера із запитанням: «Яка IP-адреса відповідає домену `github.com`?» У відповідь отримує IP-адресу, після чого може встановити з'єднання із сервером. Браузер і операційна система тимчасово зберігають цю відповідь у кеші, тому повторні відкриття сайту відбуваються швидше.

### URL

**URL (Uniform Resource Locator)** - повна адреса ресурсу в інтернеті. Розберімо `https://example.com:443/articles?id=10#comments`:

- `https` - протокол, тобто правило, за яким браузер і сервер спілкуються;
- `example.com` - домен;
- `443` - порт, умовний номер «входу» на сервер; для HTTPS це типовий порт, тому його зазвичай не пишуть;
- `/articles` - шлях до конкретного ресурсу;
- `?id=10` - параметр запиту, що передає додаткові дані;
- `#comments` - фрагмент сторінки, до якого браузер прокрутить документ; на сервер він не надсилається.

### HTTP та HTTPS

**HTTP (HyperText Transfer Protocol)** - набір правил для обміну даними між клієнтом і сервером. Браузер надсилає HTTP-запит, а сервер повертає HTTP-відповідь. Сам HTTP не шифрує дані.

**HTTPS** - це HTTP, захищений шифруванням TLS. Він захищає дані під час передавання: наприклад, пароль, який ви вводите на сайті, не має бути доступним людям у тій самій мережі. Для реальних сайтів завжди використовуйте HTTPS.

### Що відбувається під час відкриття сайту

1. Користувач вводить URL, наприклад `https://example.com`.
2. Браузер виділяє домен `example.com` і через DNS дізнається IP-адресу сервера.
3. Браузер підключається до цієї IP-адреси; для HTTPS спочатку встановлюється захищене TLS-з'єднання.
4. Браузер надсилає HTTP-запит, наприклад `GET /`.
5. Сервер обробляє запит і повертає HTTP-відповідь: статус, заголовки та дані, наприклад HTML.
6. Браузер читає HTML, окремо завантажує CSS, JavaScript, зображення та відображає сторінку.

### Будова HTTP-запиту та відповіді

Запит `GET /products` означає: «сервере, надішли мені список товарів». Він містить метод, шлях, заголовки та іноді тіло з даними.

```http
GET /products HTTP/1.1
Host: example.com
Accept: application/json
```

Відповідь містить статус, заголовки та тіло:

```http
HTTP/1.1 200 OK
Content-Type: application/json

[{"id": 1, "name": "Laptop"}]
```

Корисні HTTP-методи: `GET` для читання даних, `POST` для створення, `PUT` або `PATCH` для оновлення, `DELETE` для видалення. Поширені статуси: `200 OK` - успіх, `201 Created` - ресурс створено, `400 Bad Request` - некоректні дані, `401 Unauthorized` - потрібна автентифікація, `404 Not Found` - ресурс не знайдено, `500 Internal Server Error` - помилка сервера.

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

1. Відкрийте клон поточного репозиторію `full-Stack-tgc` у VS Code командою `code .`.
2. Створіть у ньому папку `practice\foundations`.
3. Створіть файл `practice\foundations\notes.md`.
4. Додайте до нього короткі нотатки про DNS, HTTP і Git.

## 4. Git

Git зберігає історію змін проєкту локально. Commit - це зафіксований зріз змін із коротким зрозумілим повідомленням.

Налаштуйте автора commits один раз:

```powershell
git config --global user.name "Ваше ім'я"
git config --global user.email "ваш-email@example.com"
```

Базовий робочий цикл:

```powershell
git status
git add .
git commit -m "docs: add first notes"
git log --oneline
```

Поточний репозиторій уже створений і прив'язаний до GitHub, тому команда `git init` тут не потрібна.

Створення окремої гілки:

```powershell
git switch -c practice/git-basics
git branch
```

Не додавайте до Git паролі, токени, ключі доступу або файли `.env`. Для цього використовуйте `.gitignore`.

## 5. GitHub

GitHub зберігає Git-репозиторії віддалено та дозволяє працювати над кодом разом.

Для навчання і практики використовуйте цей репозиторій `full-Stack-tgc`: створювати інший не потрібно. У ньому зберігатимуться матеріали уроків, ваші нотатки та практичні завдання.

1. Створіть акаунт на [GitHub](https://github.com/), якщо його ще немає.
2. Клонуйте цей репозиторій на свій комп'ютер.
3. Для кожного завдання створюйте окрему гілку від потрібного навчального етапу.
4. Публікуйте гілку та створюйте pull request, коли робота готова.

```powershell
git switch -c practice/dns-notes
git add practice\foundations\notes.md
git commit -m "docs: add DNS notes"
git push -u origin practice/dns-notes
```

## Практичне завдання

У поточному репозиторії створіть таку структуру:

```text
full-Stack-tgc/
└── practice/
    └── foundations/
        ├── web-basics.md
        ├── terminal.md
        └── git.md
```

У цих трьох файлах коротко зафіксуйте, що ви вивчили. Зробіть щонайменше три логічні commits:

1. `docs: add web request notes`
2. `docs: add terminal practice notes`
3. `docs: add Git workflow notes`

## Чекліст завершення

- [ ] Я пояснюю різницю між клієнтом, сервером і API.
- [ ] Я розумію, для чого потрібні DNS, URL, HTTP-запит і HTTP-відповідь.
- [ ] Я вмію переходити між папками й створювати файли в терміналі.
- [ ] Я вмію створити Git-репозиторій, commit і гілку.
- [ ] Я вмію відправити проєкт на GitHub.
- [ ] Я додав нотатки та практичні файли в поточний репозиторій.
- [ ] Я опублікував власну гілку з виконаною практикою.

## Навігація за етапами

[Основи розробки](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/01-development-foundations) · [HTML та CSS](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/02-html-css) · [JavaScript](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/03-javascript) · [TypeScript](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/04-typescript) · [React frontend](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/05-react-frontend) · [Node.js та backend](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/06-nodejs-backend) · [Бази даних](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/07-databases) · [Авторизація та безпека](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/08-authentication-security) · [Тестування](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/09-testing) · [Деплой і DevOps](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/10-deployment-devops) · [Портфоліо](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/11-portfolio)

[Переглянути розгорнутий навчальний план](https://github.com/demiusdelph-developer/full-Stack-tgc#full-stack-learning-roadmap)
