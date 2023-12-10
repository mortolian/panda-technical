![horizontal-sm.webp](docs%2Fhorizontal-sm.webp)
# Panda Technical Project - Laravel API Consumer

Your task will require using the Panda API to collect a set of information, and building a
basic dashboard to view the information.

1. Project details
2. Project Setup
3. Project References and Attributions

---

## Project Details

### General

You need to use the following:

- [x] Laravel
- [x] Laravel standards 
- [x] Laravel services (e.g. Laravel Http, not curl, etc).
- [ ] Tailwind
- [ ] Alpine (if you use JS)
- [ ] A charts library of your choice. Recommendations would be Chart.js or Apache Echarts.
- [ ] For the environment we recommend a docker-compose.yml in the main repo that brings
  up any services you need. If you are not familiar with docker you can document any other
  method required in a README.
- [x] Please create a GitHub repo 
- [ ] share it with dbfx on GitHub (https://github.com/dbfx)

### Part 1: Authentication

- [ ] Accept an email address and password for the production Panda backend. You can create
  this user and password (for your testing) by downloading the Panda app (visit
  https://get.joinpanda.com on mobile) and signing up for free.

- [ ] Finish the sign up process so that your full account exists (choose keywords, etc).
- [ ] You can then login as that user by sending a POST request to: https://api.joinpanda.com/api/auth/email/login/

With the following data:

- [ ] “email”: “your@email.com”
- [ ] “password”: “yourpassword”
- [ ] This will return a “key” value in JSON which is your Bearer token for authenticating the
  rest of your requests.

### Part 2: Forest Sessions

- [ ] Use the bearer token to request: https://api.joinpanda.com/api/session?page_size=100&page=1&home_territory=all
  This will return an array of our upcoming live sessions in the app. You should cache this for a sensible period.

### Part 3: Dashboard

Show a dashboard that gives information about the upcoming Forest sessions.

Examples would be:

- [ ] Number per day
- [ ] Next session
- [ ] Highlights based on your keywords (you can use /api/me on production to get keywords for the user)
- [ ] Any other ideas you have
- [ ] Try to make it usable, look good, and show information in a well-thought-out way.

---

## Project Setup

- Laravel v10.35.0 (PHP v8.2.13)

The project will run in development mode using Laravel Sail to facilitate a local Docker `Development` and `Testing`
environment.
If you are unfamiliar with sail you can find the documentation here: https://laravel.com/docs/10.x/sail#main-content

The project runs using the latest versions or at least latest stable versions of everything requested.

The project was developed using `PHPStorm` as the IDE, but should be viewable in any IDE with the standards being checked with
`Laravel PINT` and `.editorconfig`.

Clone the project

```bash
git clone git@github.com:mortolian/panda-technical.git
```

Start the project with Docker (Laravel Sail)

```bash
php artisan sail:install
./vendor/bin/sail up
```

Run the setup

```bash
```

Stop Composer

```bash
./vendor/bin/sail stop
```

## Run Project Tests

Code quality checks

```bash
./vendor/bin/sail composer run pint
```

Run Unit and Feature Tests

```bash

```

## Project References and Attributions

- https://www.joinpanda.com/
- [README.laravel.md](docs/README.laravel.md)
