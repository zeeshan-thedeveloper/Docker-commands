# Digital ocean
#### 1. docker build -t [APP_NAME] .
#### 2. docker run -p 80:80 [APP_NAME]
#### 3. doctl registry create [REGISTRY_NAME]
#### 4. doctl registry login
#### 5. docker tag [APP_NAME] registry.digitalocean.com/[REGISTRY_NAME]/[APP_NAME]
#### 6. docker push registry.digitalocean.com/[REGISTRY_NAME]/[APP_NAME]
#### 7. docker run -p 80:80 registry.digitalocean.com/[REGISTRY_NAME]/[APP_NAME]

