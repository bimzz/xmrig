# XMRig Docker - Dockerized Monero miner

## Basics

This docker image of XMRig lets you mine Monero with 0 dev fees.

## Usage

You can run it using docker or docker-compose. Choose either option A or B.
<br><br>

### [Option A] Using docker:

No need to download anything, simply run:

```shell
docker run -d --name miner cryptrent/xmrig --url=pool.supportxmr.com:5555 --user=46fs56A17gENdhqF1K45v96d4qcKRf5K86hssfS7PHr3j6eBogo4a7WHyhAEytjSaUJEQS785pPFUT3d8P1cZkps3kA2JA5 --pass=worker
docker logs -f miner
```
<br>

### [Option B] Using docker-compose:

```shell
git clone https://github.com/cryptrent/xmrig.git

cd xmrig

# Configure your pool and worker in the docker-compose.yml file
nano docker-compose.yml

docker-compose up -d

docker-compose logs -f
```
<br>

### Dev Fee

The dev fee is 1% by default. To disable, use the `--donate-level=0` parameter.
