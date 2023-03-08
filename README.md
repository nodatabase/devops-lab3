# DevOps Lab 3 - Docker

## Commands

### Build
```shell
docker build -t nodatabase/my-app .
```
to build the image.

### Push
```shell
docker image push nodatabase/my-app:lab3
```
to push the image to the repo.

### Run
To run locally, run `npm i && npm run start`. (would be running on default port: 3000)
To run in a docker container, use
```shell
docker pull nodatabase/my-app:lab3 && \
docker run --memory=1g --cpus=2 -p 80:3000 --name my-app-container nodatabase/my-app:lab3
```

### Verify correctness
Use
```shell
curl http://localhost
```

