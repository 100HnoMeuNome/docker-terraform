# docker-terraform
First nginx container using TF

# how to install terraform

- [Install Terraform](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)
- [Install Docker desktop](https://www.docker.com/products/docker-desktop/)


# fix the error Cannot load builder default

Maybe you can get a error

```Issue : Cannot load builder default: Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running"```

Here how to fix:

- Step 1. Verify context, it should be dektop-linux
  - $ docker context show
  
- Step 2. Change the context if needed
  - $ docker context use desktop-linux
  
- Step 3. Find the docker.sock file location
  - $ docker context ls
  
- Step 4. Create symlink
  - $ sudo ln -s /home/<user>/.docker/desktop/docker.sock /var/run/docker.sock

# quick tutorial
- [How to build](https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli#quick-start-tutorial)
