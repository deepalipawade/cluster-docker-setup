Creating docker environment using the docker image - https://hub.docker.com/repository/docker/depalipawade/mmaction2/general
1. Edit train.sub file , change docker image to - depalipawade/mmaction2:tensorflow
2. execute sub file to create a setup job

```
scp ~/.ssh/sic_cluster.pub <team_id>@conduit.cs.uni-saarland.de:~/
mkdir -p ~/.ssh
cat ~/sic_cluster.pub >> ~/.ssh/authorized_keys
chmod 600 ~/.ssh/authorized_keys
```

References :
1. Refer only last part since we already have an image we dont need to create docker image from scratch - https://mgit.cs.uni-saarland.de/Joschka/cluster-tutorial/-/tree/main
2. https://github.com/open-mmlab/mmaction2
3. Original CLuster Doc repo - https://gitlab.cs.uni-saarland.de/mara00002/torch-condor-template
