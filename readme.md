1. Create namespace with:
```
kubectl create -f ./name-file
```
2. Create A secret for Docker Hub.
```
kubectl create secret docker-registry my-registry-secret \
--docker-username=DOCKER_USER \
--docker-password=DOCKER_PASSWORD \
--docker-email=DOCKER_EMAIL
```
Example:
```
kubectl create secret docker-registry docker-registry-secret \
--docker-username=***** \
--docker-password=********
```
3. Create secret for nextjs app from .env.next file 
```
kubectl create secret generic nextjs-env-secret --from-env-file=./.env.next
```
4. Create ConfigureMap for languate-tool service.
