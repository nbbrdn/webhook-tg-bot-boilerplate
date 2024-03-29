# Webhook Telegram Bot Boilerplate

## How to run

Without Docker:

```bash
BOT_TOKEN=token WEBHOOK_SECRET=my-secret BASE_WEBHOOK_URL=https://my-address WEB_SERVER_PORT=my-port python main.py
```

## Development

### First Run

1. Create and activate the Virtual Python Environment.
2. Install requirements

```bash
pip install -r requirements.txt
pip install -r requirements-dev.txt
```

3. Install pre-commit hook

```bash
pre-commit install
```

## Dockerize

Create the Docker image:

```bash
docker build -t telegram-bot .
```

You can check if the Docker image is created using `docker images` command.

Run the Docker container:

```bash
docker run -p 8080:8080 --env BOT_TOKEN=telegram-bot-token --env WEBHOOK_SECRET=mysecret --env BASE_WEBHOOK_URL=mydomain.com --env WEB_SERVER_PORT=8080 telegram-bot
```

## Useful Resources

[Setting Up ngrok on WSL2. Linux & Windows](https://create.hashnode.dev/setting-up-ngrok-on-wsl2-linux-windows)
