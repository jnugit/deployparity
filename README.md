# deployparity
deploy parity node via docker-compose

### Generate Docker-compose
./parity-deploy.sh --config aura --name jnuchain

### RUN
docker-compose up -d

### log
docker-compose logs -f

## TO DO LIST
* add ethstats monitor
```
monitor:
    image: buythewhale/ethstats_monitor
    volumes:
      - ./monitor/app.json:/home/ethnetintel/eth-net-intelligence-api/app.json:ro
  dashboard:
    image: buythewhale/ethstats
    volumes:
      - ./dashboard/ws_secret.json:/eth-netstats/ws_secret.json:ro
    ports:
      - 3001:3000
 ```
