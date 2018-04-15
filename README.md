# gendermeme-scnlp-docker
A multi-container application running Gendermeme and a Stanford Core NLP server.

## How to run this code
Clone this repo
```
git clone https://github.com/joeybones/gendermeme-corenlp-docker.git
```

Deploy the docker-compose.yml in swarm mode
```
docker swarm init
docker stack deploy -c docker-compose.yml gendermeme-scnlp-docker
```

Get requests to `http://localhost:5000` with a `text` parameter will be run through the NLP server and through gendermeme
