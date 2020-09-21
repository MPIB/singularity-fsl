[![https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg](https://www.singularity-hub.org/static/img/hosted-singularity--hub-%23e32929.svg)](https://singularity-hub.org/collections/702)

## Quick start

```
# Download a (versioned) container
singularity pull shub://MPIB/singularity-fsl:6.0.4

# Run it
singularity exec singularity-fsl_6.0.4.sif fslmaths
singularity exec --nv singularity-fsl_6.0.4.sif eddy_cuda9.1
```

## FSL

Project Home: https://fsl.fmrib.ox.ac.uk/fsl/fslwiki/

These are containers primarily used at the MPI for Human Development.

## Cuda

Starting with Singularity 6.0.2 we include Nvidia CUDA through Debian backports repositories.
Make sure your Nvidia driver on the host [supports it](https://docs.nvidia.com/deploy/cuda-compatibility/index.html#binary-compatibility) and add the `--nv` flag with singularity.


## Note

Please be aware of FSL's strict license regarding non-commercial use.
