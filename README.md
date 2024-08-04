```sh
# build
dk build -t favorites-node .

# create network
docker network create favorites-net

# term1: db
docker run --name mongodb --network favorites-net mongo

# term2: app
dkr --name favorites -p80:3000 --network favorites-net favorites-node
```
