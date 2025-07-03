# 
# d-o-188 note

[1) Verify with podman command for public container registries has already login or not.](https://github.com/Adrianhein/d-o-188-lab/blob/main/verify%20container%20registry%20login)

#

[2) Local Container Registry Server SetUp](https://github.com/Adrianhein/d-o-188-lab/blob/main/Tin_ex188_LAB_SETUP_V1.1.pdf)
#### Update! 
#### Lab Steup, currently using V1 format for registry server.
#### We have to use V2 format now.
#### /etc/containers/registries.conf

    unqualified-search-registries = [
    "registry.access.redhat.com",
    "registry.redhat.io",
    "docker.io"
    ]

    [[registry]]
    location = "my-infra-01:5000"
    insecure = true

#### Should NOT include below block

    [registries.search]
    registries = ["..."]

    [registries.insecure]
    registries = ["..."]


#

[3) Basic podman container commands and usages](https://github.com/Adrianhein/d-o-188-lab/blob/main/Basic%20podman%20commands)

[4) Root container and Rootless container](https://github.com/Adrianhein/d-o-188-lab/blob/main/Rootless%20and%20Root%20containers)

[5) Container Image Managing](https://github.com/Adrianhein/d-o-188-lab/blob/main/Generating%20container%20image%20with%20commit)

[6) Backup and restore the container image](https://github.com/Adrianhein/d-o-188-lab/blob/main/Container%20backup%20and%20restore%20with%20podman)

[7) Dockerfile [Containerfile]](https://github.com/Adrianhein/d-o-188-lab/blob/main/ContainerFile(Dockerfile))

[8) Container volume & storage](https://github.com/Adrianhein/d-o-188-lab/blob/main/Container%20Volumes)

[9) SELinux with podman](https://github.com/Adrianhein/d-o-188-lab/blob/main/SELinux%20with%20podman)

[10) Podman container persistent [creating systemd service for container runtime]](https://github.com/Adrianhein/d-o-188-lab/blob/main/Podman%20container%20persistent)


# 
# Red Hat Certified Specialist in Containers exam [EX188]
[Study points for the exam](https://www.redhat.com/en/services/training/ex188-red-hat-certified-specialist-containers-exam?section=objectives)

[Visit Google](https://www.google.com)
