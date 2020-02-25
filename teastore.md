# Images
## Registry
```
descartesresearch/teastore-registry
Mandatory: SERVICE_PORT
Recommended: HOST_NAME
```
```s
docker run -e "HOST_NAME=172.17.0.2" -e "SERVICE_PORT=10000" -p 10000:8080 -d descartesresearch/teastore-registry
```
## Webui
```
descartesresearch/teastore-webui
Mandatory: REGISTRY_HOST, REGISTRY_PORT, SERVICE_PORT
Recommended: HOST_NAME (or USE_POD_IP=true in Kubernetes)
Optional: PROXY_NAME, PROXY_PORT
```
```s
docker run -e "REGISTRY_HOST=172.17.0.2" -e "REGISTRY_PORT=10000" -e "HOST_NAME=172.17.0.2" -e "SERVICE_PORT=8080" -p 8080:8080 -d descartesresearch/teastore-webui
```
## Auth
```
descartesresearch/teastore-auth
Mandatory: REGISTRY_HOST, REGISTRY_PORT, SERVICE_PORT
Recommended: HOST_NAME (or USE_POD_IP=true in Kubernetes)
```
```s
docker run -e "REGISTRY_HOST=172.17.0.2" -e "REGISTRY_PORT=10000" -e "HOST_NAME=172.17.0.2" -e "SERVICE_PORT=2222" -p 2222:8080 -d descartesresearch/teastore-auth
```
## Persistence
```
descartesresearch/teastore-persistence
Mandatory: REGISTRY_HOST, REGISTRY_PORT, SERVICE_PORT, DB_HOST, DB_PORT
Recommended: HOST_NAME (or USE_POD_IP=true in Kubernetes)
```
```s
docker run -e "REGISTRY_HOST=172.17.0.2" -e "REGISTRY_PORT=10000" -e "HOST_NAME=172.17.0.2" -e "SERVICE_PORT=1111" -e "DB_HOST=172.17.0.3" -e "DB_PORT=3306" -p 1111:8080 -d descartesresearch/teastore-persistence
```
## Recommender
```
descartesresearch/teastore-recommender
Mandatory: REGISTRY_HOST, REGISTRY_PORT, SERVICE_PORT
Recommended: HOST_NAME (or USE_POD_IP=true in Kubernetes)
Optional: RECOMMENDER_RETRAIN_LOOP_TIME, RECOMMENDER_ALGORITHM
```
```s
docker run -e "REGISTRY_HOST=172.17.0.2" -e "REGISTRY_PORT=10000" -e "HOST_NAME=172.17.0.2" -e "SERVICE_PORT=3333" -p 3333:8080 -d descartesresearch/teastore-recommender
```
## Image
```
descartesresearch/teastore-image
Mandatory: REGISTRY_HOST, REGISTRY_PORT, SERVICE_PORT
Recommended: HOST_NAME (or USE_POD_IP=true in Kubernetes)
```
```s
docker run -e "REGISTRY_HOST=172.17.0.2" -e "REGISTRY_PORT=10000" -e "HOST_NAME=172.17.0.2" -e "SERVICE_PORT=4444" -p 4444:8080 -d descartesresearch/teastore-image
```

## Db
```
descartesresearch/teastore-db
none
```
```s
docker run -p 3306:3306 -d descartesresearch/teastore-db
```