# Full Stack Learning Roadmap

## Етап 3: JavaScript

Освойте типи даних, функції, масиви, об'єкти, DOM, події, модулі, Promise, async/await, `fetch` і обробку помилок. Результат етапу - To-do app та застосунок погоди, що працює з API.

Цей репозиторій містить практичну дорожню карту для вивчення Full Stack розробки з нуля. Кожен етап винесений в окрему гілку: переходьте за посиланням, вивчайте тему та додавайте власні практичні проєкти.

## Навчальні гілки

| Етап | Тема | Гілка |
| --- | --- | --- |
| 1 | Основи розробки | [01-development-foundations](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/01-development-foundations) |
| 2 | HTML та CSS | [02-html-css](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/02-html-css) |
| 3 | JavaScript | [03-javascript](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/03-javascript) |
| 4 | TypeScript | [04-typescript](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/04-typescript) |
| 5 | React frontend | [05-react-frontend](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/05-react-frontend) |
| 6 | Node.js та backend | [06-nodejs-backend](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/06-nodejs-backend) |
| 7 | Бази даних | [07-databases](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/07-databases) |
| 8 | Авторизація та безпека | [08-authentication-security](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/08-authentication-security) |
| 9 | Тестування | [09-testing](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/09-testing) |
| 10 | Деплой і DevOps | [10-deployment-devops](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/10-deployment-devops) |
| 11 | Портфоліо | [11-portfolio](https://github.com/demiusdelph-developer/full-Stack-tgc/tree/11-portfolio) |

## Як навчатись

1. Рухайтесь за етапами від першого до одинадцятого.
2. Приділяйте близько 70% часу практиці та 30% теорії.
3. Завершуйте кожен етап готовою функцією або невеликим проєктом.

## Повний план

## Тривалість навчання

За умови навчання приблизно 2 години на день, 5-6 днів на тиждень, реалістично досягти рівня junior full-stack developer за 9-12 місяців.

## План навчання

| Етап | Тривалість | Технології та теми | Результат |
| --- | --- | --- | --- |
| 1. Основи розробки | 2-3 тижні | Як працює веб: браузер, HTTP, DNS, клієнт/сервер; Git і GitHub; VS Code; командний рядок | GitHub-профіль і перший репозиторій |
| 2. HTML та CSS | 4-6 тижнів | Семантичний HTML, форми, CSS selectors, box model, Flexbox, Grid, responsive design, accessibility | Адаптивний сайт-візитка та лендінг |
| 3. JavaScript | 8-10 тижнів | Типи, функції, масиви, об'єкти, DOM, події, async/await, Promise, fetch, modules, обробка помилок | To-do app, погодний застосунок через API |
| 4. TypeScript | 2-3 тижні | Типи, interfaces, generics, union types, типізація API та компонентів | Перепис одного JavaScript-проєкту на TypeScript |
| 5. React frontend | 6-8 тижнів | Компоненти, props, state, hooks, routing, forms, Context, робота з API, React Query або TanStack Query | SPA: каталог товарів, блог або трекер задач |
| 6. Node.js та backend | 6-8 тижнів | Node.js, npm, Express або NestJS, REST API, middleware, валідація, логування, структура проєкту | API для власного React-проєкту |
| 7. Бази даних | 4-5 тижнів | SQL, PostgreSQL, таблиці, зв'язки, індекси, migrations; ORM: Prisma або Drizzle | Backend з PostgreSQL і CRUD |
| 8. Авторизація та безпека | 3-4 тижні | Password hashing, JWT, cookies, refresh tokens, roles, CORS, rate limiting, validation, environment variables | Реєстрація, логін, ролі користувачів |
| 9. Тестування | 3-4 тижні | Unit-тести: Vitest/Jest; API-тести; React Testing Library; базове E2E: Playwright | Покритий тестами API та ключові UI-сценарії |
| 10. Деплой і DevOps | 2-3 тижні | Docker, CI/CD через GitHub Actions, Vercel/Netlify для frontend, Render/Railway/Fly.io для backend, PostgreSQL у хмарі | Повністю задеплоєний full-stack застосунок |
| 11. Портфоліо | 4-8 тижнів | Архітектура, документація, README, UI/UX, робота з багами, code review | 2-3 якісні проєкти на GitHub |

## Рекомендований стек

- **Frontend:** HTML, CSS, JavaScript, TypeScript, React, React Router, TanStack Query.
- **Backend:** Node.js, Express або NestJS, REST API.
- **Database:** PostgreSQL + Prisma.
- **Auth:** JWT у HTTP-only cookies.
- **Tools:** Git, GitHub, VS Code, Postman/Bruno, Docker.
- **Deploy:** Vercel + Render/Railway + Neon/Supabase PostgreSQL.

## Порядок навчання

1. Не переходьте до React, доки не зможете самостійно зробити кілька невеликих застосунків на чистому JavaScript.
2. Не починайте складний backend, доки не розумієте HTTP, `fetch`, JSON, async/await і структуру REST API.
3. Вивчайте SQL до ORM: Prisma має спрощувати роботу з базою даних, а не замінювати розуміння її основ.
4. Після кожного нового блоку робіть практичний проєкт і публікуйте його на GitHub.
5. Виділяйте приблизно 70% часу на практику і 30% на теорію.

## Проєкти для портфоліо

1. **Task Manager** - React + Node.js + PostgreSQL: авторизація, задачі, статуси, дедлайни та фільтри.
2. **E-commerce mini shop** - каталог, пошук, кошик, замовлення та адмін-панель.
3. **Full-stack блог** - авторизація, статті, коментарі, ролі автора й адміністратора, завантаження зображень.
4. **Фінансовий трекер** - категорії витрат, графіки, фільтри за датою та експорт даних.

## Ритм навчання

Кожен тиждень завершуйте невеликою готовою функцією або проєктом, а не лише переглядом уроків.
