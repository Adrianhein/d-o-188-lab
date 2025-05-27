---

Sometimes, "podman" command not able to run even if the system already installed podman. See below error, "admin" user cannot run "podman" command.

    [admin@r-h-e-l-9-LAB ~]$ podman ps 
    WARN[0000] RunRoot is pointing to a path (/run/user/1000/containers) which is not writable. Most likely podman will fail. 
    ##########Error: default OCI runtime "crun" not found: invalid argument
    [admin@r-h-e-l-9-LAB ~]$ 


In this case, we'll need to check login session which direct login with specific non-root user that "podman" can porate.

This should be runing podman command below

    ssh admin@r-h-e-l-9-LAB
    [admin@r-h-e-l-9-LAB ~]$ podman images ; podman ps 
    REPOSITORY  TAG         IMAGE ID    CREATED     SIZE
    CONTAINER ID  IMAGE       COMMAND     CREATED     STATUS      PORTS       NAMES


This cannot run podman command below

    [root@r-h-e-l-9-LAB ~]# su - admin
    [admin@r-h-e-l-9-LAB ~]$ 
    [admin@r-h-e-l-9-LAB ~]$ podman ps 
    WARN[0000] RunRoot is pointing to a path (/run/user/1000/containers) which is not writable. Most likely podman will fail. 
    ##########Error: default OCI runtime "crun" not found: invalid argument
    [admin@r-h-e-l-9-LAB ~]$ 
    
---

