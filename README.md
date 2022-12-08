# docker-compose mongodb boilerplate

Runs an instance of mongodb and persists mongo files locally. Using this to experiment with mongodb and play around with a few projects

## Usage

Update the environment variables in docker-compose.yml

### Run server
```
docker-compose up -d --build
``` 

### View records in Mongo Express

In browser, go to localhost:8082

### Interacting with this database
```
# From host machine
MONGO_URI=mongodb://<username>:<secure_password>@system-mongo-db:27018/prod?authSource=admin

# From a docker container
MONGO_URI=mongodb://<username>:<secure_password>@host.docker.internal:27018/prod?authSource=admin
```