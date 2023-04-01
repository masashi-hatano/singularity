# Singularity Tutorial

## 1. build singularity image
You can build singularity image (.sif) from definition file (.def).
```
sudo singularity build pytorch2.0.sif 11.8.0-cudnn8-devel-ubuntu20.04.def
```

## 2. run singularity container
Once you created singularity image, you are now ready to start singularity container based on the image.

(optional) Singularity allows you to map directories on your host system to directories within your container using bind mounts.
This will bind `/mnt/ssd1` on the host to `/data` in the container 
```
export SINGULARITY_BIND="/mnt/ssd1:$PWD/data"
```
Run singularity container
```
singularity shell --nv pytorch2.0.sif
```

## References
- [how to write a definition file](https://docs.sylabs.io/guides/latest/user-guide/definition_files.html)
- [how to use singularity](https://tmyoda.hatenablog.com/entry/20200817/1597663325)
