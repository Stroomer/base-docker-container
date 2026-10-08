# Base Docker container

Local development base: a PHP 8.4 / Apache app container, MySQL 8.4 and phpMyAdmin.

## Usage

```sh
docker compose up -d --build
```

| Service    | URL / host            | Credentials   |
|------------|-----------------------|---------------|
| App        | http://localhost:8080 |               |
| phpMyAdmin | http://localhost:8081 | `root` / `root` |
| MySQL      | `localhost:3306`      | `root` / `root`, database `test` |

Application code lives in `src/` (mounted into the container); the web root is `src/public/`.

To change the host ports, copy `.env.example` to `.env` and edit it.

```sh
docker compose down      # stop
docker compose down -v   # stop and delete the database volume
```

The credentials are for local development only.
