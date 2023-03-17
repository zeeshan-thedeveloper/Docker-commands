# Digital ocean
#### 1. docker build -t [APP_NAME] .
#### 2. docker run -p 80:80 [APP_NAME]
#### 3. doctl registry create [REGISTRY_NAME]
#### 4. doctl registry login
#### 5. docker tag [APP_NAME] registry.digitalocean.com/[REGISTRY_NAME]/[APP_NAME]
#### 6. docker push registry.digitalocean.com/[REGISTRY_NAME]/[APP_NAME]
#### 7. docker run -p 80:80 registry.digitalocean.com/[REGISTRY_NAME]/[APP_NAME]
#### 8. doctl kubernetes cluster create [CLUSTER_NAME] --tag [APP_TAG] --auto-upgrade=true --node-pool "name=[APP_POOL_NAME];count=2;auto-scale=true;min-nodes=1;max-nodes=3;tag=[APP_TAG]"
#### 9. kubectl create deployment [APP_NAME] --image=registry.digitalocean.com/[APP_REGISTRY]/[APP_NAME]
#### 10. kubectl patch serviceaccount default -p '{"imagePullSecrets": [{"name": "registry-[REGISTRY_NAME]"}]}' [But for this we can use other command]
#### 11. kubectl get rs
#### 12. kubectl get pods
#### 13. kubectl scale deployment/[APP_NAME] --replicas=20
#### 14. kubectl expose deployment [APP_NAME] --type=LoadBalancer --port=80 --target-port=80
#### 15. doctl compute load-balancer list --format Name,Created,IP,Status
#### 16. doctl auth init





