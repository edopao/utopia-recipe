# Utopia Development Env Recipe

This set of Yaml files make up the [Stackinator](https://github.com/eth-cscs/stackinator) recipe for the [Utopia](https://bitbucket.org/zulianp/utopia/) development environment on Hohgant.
By means of the Stackinator tool, it is possible to create a [Spack](https://github.com/spack/spack) stack with the tools and libraries needed to build Utopia.

This Utopia recipe enables the CUDA variant on the Spack packages, whenever available, so that it is possible to use Utopia on the A100 nodes of Hohgant with the [Trilinos](https://github.com/trilinos/Trilinos) GPU backend.

Please refer to the [arbor-recipe](https://github.com/bcumming/arbor-recipe) guide for instructions how to build the development environment using Stackinator and how to mount it.

After the development environment is mounted on `/user-environment`, load the modules required by Utopia:

    module use /user-environment/modules/
    module avail
    module load cmake cray-mpich cuda gcc hypre openblas petsc slepc suite-sparse trilinos yaml-cpp
