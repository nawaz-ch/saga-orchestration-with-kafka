# saga-orchestration-with-kafka


**For running kafka brokers**



- in docker-compose.yml file, change volumes `/home/nawaz17/kafka/docker-compose/volumes/server-1` according to your local setup.

 - create volumes to run brokers locally
```bash
mkdir volumes
cd volumes
mkdir server-1
mkdir server-2
mkdir server-3
```
- run docker compose file
```bash
  docker compose up -d
```

**Saga-pattern Happy path flow**


![alt](https://github.com/nawaz-ch/saga-orchestration-with-kafka/blob/84191aa212ba8950f473ea15e44132c7606b1138/saga-pattern(happy-path).png)



> [!NOTE]
> In case the paymentDB failed to save the payment, the DB can rollback the transcation. To maintain data consistency,the productsDB and orderDB must be rolledback through compensating transcations.


![alt](https://github.com/nawaz-ch/saga-orchestration-with-kafka/blob/fc0cc2ac85c57129ee214b91610d14bfb444abe3/%5Dcompensating-transcation.png)

