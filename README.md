# tinyfl

a tiny federated learning framework built with pytorch and fastapi.

## requirements

- python==3.10.10
- torch==1.13.0
- torchvision==0.14.0
- httpx
- uvicorn
- fastapi

## installation

use poetry

```sh
poetry env use 3.10
poetry install
```

or

use conda

```sh
conda create -n tinyfl python=3.10.10
conda activate tinyfl
pip install torch==1.13.0 torchvision==0.14.0 httpx uvicorn fastapi
```

## quickstart

run the aggregator

```sh
poetry run agg config/agg.config.json
```

run the parties

```sh
poetry run party config/party0.config.json
poetry run party config/party1.config.json
poetry run party config/party2.config.json
```

get aggregator status

```sh
curl {aggregator}/
```

start training round

```sh
curl {aggregator}/start_round
```
