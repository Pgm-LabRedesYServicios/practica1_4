# Previous steps
In order to be able to deploy this config, the following lines must be added to
the file `~/.ssh/config` (assuming that the key to access the remote virtual
server is `amazon_free_1.pem`)

``` ssh-config
Host amazon_labredes
    User ubuntu
    HostName <the address that amazon gives you>
    Port 22
    IdentityFile ~/.ssh/amazon_free_1.pem
```

# Deployment of Docker service
Since the application is packaged in a Dockerfile, we can deploy the service
with Ansible, in order to do that we need to write a playbook for that.
