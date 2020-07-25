# deployment

1) clone this repo

```bash
git clone https://github.com/bc-ticketing/deployment.git
```

2) edit `.env` file with necessary environment variables such as passwords, api key etc.

3) download latest changes from docker hub:

```bash
docker-compose pull
```

4) run containers

```bash
docker-compose up
```
