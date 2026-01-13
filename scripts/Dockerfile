ARG ARCH=x86_64 # Or "aarch64"
FROM quay.io/pypa/manylinux_2_28_${ARCH}

ARG ARCH
ARG CUDA_12_TOOLKIT_VERSION=12.9.1
RUN curl -fsSL https://developer.download.nvidia.com/compute/cuda/repos/rhel8/${ARCH}/cuda-rhel8.repo \
    -o /etc/yum.repos.d/cuda.repo && \
    yum -y install cuda-toolkit-12-${CUDA_12_TOOLKIT_VERSION}

RUN manylinux-interpreters ensure-all
