# docker-demo


Hard link FE

ln -s hello-world/package.json docker/frontend 
ln -s hello-world/yarn.lock docker/frontend 

Hard link BE

ln example-app/composer.json docker/backend 
ln example-app/composer-lock.json docker/backend 