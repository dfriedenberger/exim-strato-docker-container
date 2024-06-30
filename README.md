# exim-strato-docker-container


See also: https://hub.docker.com/r/imixs/exim4

## Installation

Create '''.env''' File with some project specific values
```
PROJECT_NAME=smarthost
STRATO_USER=<email>
STRATO_PASSWORT=<password>
```

```
docker-compose up -d 
```

## Test

### Test Configuration
docker exec -it smarthost bash

```
echo "This is the message" | mail -s "The subject" <to-email> -aFrom:<from-email>
```

### test Connection
```
docker run -it --rm debian:bookworm-slim bash
```

```
apt-get update
apt-get install telnet
telnet host.docker.internal 25
```
