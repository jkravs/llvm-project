# Target-dev specific build instruction

## Prerequisits

- gcc/9
- clang/11
- cuda/11.4
- cmake/3.21.1
- hwloc/2.5.0

## Build
Compile with

```shell
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=~/.local/install/llvm/target-dev \
    -DLIBOMPTARGET_NVPTX_COMPUTE_CAPABILITIES="60,70" \
    -DLIBOMP_HWLOC_INSTALL_DIR=~/.local/install/hwloc/2.5.0 ..
make -j12
```
