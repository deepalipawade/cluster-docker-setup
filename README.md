Cluster repo - https://gitlab.cs.uni-saarland.de/mara00002/torch-condor-template
- Has clear instruction about setting up miniconda env
- Any new installations that are required
- Along with distinct setup and run jobs

Another way to go about using exisitng Docker image instead of the one given in .sub files
- Creating docker environment using the docker image - [https://hub.docker.com/repository/docker/depalipawade/mmaction2/general](https://hub.docker.com/r/depalipawade/mmaction2/tags)
- Edit train.sub file, change docker image to - depalipawade/mmaction2:tensorflow
- Execute sub file to create a setup job

To set up SSH keys to avoid entering password and username@domain

```
scp ~/.ssh/sic_cluster.pub <team_id>@conduit.cs.uni-saarland.de:~/
mkdir -p ~/.ssh
cat ~/sic_cluster.pub >> ~/.ssh/authorized_keys
chmod 600 ~/.ssh/authorized_keys
```

To check if ssh key is working(since key is not accessible, we are checking - manually by specifying the private key)- 
```
ssh -i ~/.ssh/sic_cluster nnti 
```


To add key automatically - 
```
Host my-cluster
  HostName cluster-ip
  User myuser
  IdentityFile ~/.ssh/sic_cluster
```

References :
1. Refer only last part since we already have an image we dont need to create docker image from scratch - https://mgit.cs.uni-saarland.de/Joschka/cluster-tutorial/-/tree/main
2. https://github.com/open-mmlab/mmaction2
3. Original CLuster Doc repo - https://gitlab.cs.uni-saarland.de/mara00002/torch-condor-template
