# AGENTS.md — apache2-php8

## What this is
Docker image with Debian, Apache, and PHP 8.3, preconfigured with PHP extensions, composer, wp-cli, and supervisor for SSH + Apache.

## Stack
- Debian (latest)
- Apache2 (+ mod_php8.3, rewrite)
- PHP 8.3 (surys package)
- Supervisor (supervisord)
- Composer
- wp-cli

## Build
```bash
./build.sh   # docker build -t apache2-php8 .
```

## Run
```bash
docker run -p 80:80 -p 22:22 -it apache2-php8
```

## Structure
- `Dockerfile` — image definition
- `supervisord.conf` — supervisor config (Apache + SSH)
- `build.sh` — build helper
- `remove_all_dockers.sh` — cleanup helper

## Conventions
- No comments in code unless asked.
- Verify: `docker build .`