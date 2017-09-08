# new_haven_io_ethereum
Ethereum experiments

# About
Total first pass hack at experimenting with ethereum using docker.

# Steps taken
* `docker-compose up -d`
* `docker-compose exec miner /bin/sh`
```
apk update
apk upgrade
apk add vim
vim genesis.json # https://github.com/ethereum/go-ethereum#defining-the-private-genesis-state
vim alloc 
mkdir .ethereum
geth init --datadir ./.ethereum genesis.json
bootnode --genkey=boot.key # this is where things fell down
```

# TODO
* [ ] handle volume mounting or copying so there no more vim and pasting inside the container
* [ ] build a bootnode (fork the container?)
* [ ] try running the bootnode command inside the same container and geth bootstrap to localhost
