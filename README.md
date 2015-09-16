# Deploy Docker containers with DeployBot

1. Create a machine

  ```bash
  docker-machine create \
      -d digitalocean \
      --digitalocean-access-token $DO_TOKEN \
      --digitalocean-image docker \
      --digitalocean-region sgp1 \
      --digitalocean-size 512mb \
      deploybot-demo
  ```

  Check if it works

  ```bash
  eval $(docker-machine env deploybot-demo)
  docker info
  ```

2. Sign up for DeployBot

3. Connect a repository

4. Create an environment

5. Add a server

  SSH to the machine

  ```bash
  docker-machine ssh deploybot-demo
  ```

  Install `docker-compose`

  ```bash
  VERSION_NUM=1.4.1 curl -L https://github.com/docker/compose/releases/download/$VERSION_NUM/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
  ```

