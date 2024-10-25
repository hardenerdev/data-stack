# data-stack

DappHomes data stack.

## deployment

### env variables

Please, modify env variables to meet your needs:

```bash
cp .env.example .env
```

| Name | Description | Example |
|---|---|---|
| CP_VERSION | Apache Kafka version | 7.7.1 |
| CLUSTER_ID | Apache Kafka cluster identifier | ZDVlY2FiZDllNTczNGM4OG |

When running in KRaft mode a `CLUSTER_ID` needs to explicitely created. This identifier is a UUID and can be generated in Unix systems as follows:

```bash
cat /proc/sys/kernel/random/uuid | tr -d '-' | base64 | cut -b 1-22
```

### deploy

```bash
git clone git@github.com:DappHomes/data-stack.git
cd data-stack
docker compose up -d
```
