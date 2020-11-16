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

## How to update ganache-cli with new snapshot

1) Delete existing db:

```bash
cd ganache-snapshot
rm -rf ganache_db/
```
2) Start a new ganache-cli with desired configuration:

```bash
ganache-cli -m <MNEMONIC> -a <NUMBER_OF_ACCOUNTS> --db ganache_db
```

3) run migration scripts

```bash
cd path-to-idetix-repo
truffle migrate --reset --network ganachecli
```

4) Stop ganache-cli
5) Build the docker image
```bash
docker build -t idetix/ganache-cli .
```

6) Push to dockerhub
```bash
docker push idetix/ganache-cli
```
