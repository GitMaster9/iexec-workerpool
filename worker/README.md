1. Initialize iexec workspace
```bash
iexec init --skip-wallet
```

2. Check "chain.json" ( default has to be set to "bellecour")
```json
{
  "default": "bellecour",
  "chains": {
    "mainnet": {},
    "bellecour": {}
  }
}
```

3. Create iexec wallet (you will need to input a new password, e.g. "password123worker")
```bash
iexec wallet create --keystoredir ./
```

4. Rename the newly created wallet (e.g. "worker_wallet.json")

5. Create a new Docker network (if the worker container need to be on the same network as the scheduler-core containers)
```bash
docker network create iexec_network
```

6. Start the Docker container from the "worker" folder.
```bash
cd worker
```

```bash
docker compose up -d
```
