This is a very unofficial repo for FSL singularity recipes used at the
[MPIB](https://www.mpib-berlin.mpg.de/). A while ago we used to automatically
push images to the amazing singularity hub. Since that project has been
abandoned, we use this repo primarily as a recipe reference.

The base container is debian 10 and it should work fine with CUDA as well.

## Build
```
export VERSION=6.0.6.1
singularity build fsl-$VERSION.sif Singularity.$VERSION
```

## Run it
```
singularity exec fsl-$VERSION.sif fslmaths
singularity exec --nv fsl-$VERSION eddy_cuda9.1
```


Some older images are still available on the
[read-only](https://singularityhub.github.io/singularityhub-docs/2021/going-read-only/)
[mirror provided by
datalad.org](https://datasets.datalad.org/?dir=/shub/MPIB/singularity-fsl) and
can be pulled directly.

## older, pre-built images from singularity-hub
(last updated  in April 2021)

```
# Download a (versioned) container
singularity pull shub://MPIB/singularity-fsl:6.0.3
```


## FSL

Project Home: https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/

These are containers primarily used at the MPI for Human Development.

## Cuda

Starting with Singularity 6.0.2 we include Nvidia CUDA through Debian backports repositories.
Make sure your Nvidia driver on the host [supports it](https://docs.nvidia.com/deploy/cuda-compatibility/index.html#binary-compatibility) and add the `--nv` flag with singularity.


## Note

Please be aware of FSL's strict license regarding non-commercial use.
