#### create docker image

- docker build -t riponwen/posts .
- docker build -t riponwen/query .
- docker build -t riponwen/comments .
- docker build -t riponwen/moderation .

#### pushing docker image to the docker hub

- docker push riponwen/posts
- docker push riponwen/query
- docker push riponwen/comments
- docker push riponwen/moderation

#### build push and deploy an image

- docker build -t riponwen/event-bus .
- docker push riponwen/event-bus
  _get the deployment name:_
  - kubectl get deployments
  - kubectl rollout restart deployment post-depl

#### Create deployment

- kubectl apply -f posts-depl.yaml
- kubectl apply -f event-bus-depl.yaml

### Kubernetes commands

- kubectl apply -f posts-depl.yaml
- kubectl get pods
- kubectl get deployments
- kubectl get services
- kubectl delete deployment posts-depl
- kubectl delete pod posts

#### create alias on mac

- alias k="kubectl"
- alias dps="docker ps"
