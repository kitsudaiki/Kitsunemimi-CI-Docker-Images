from ubuntu:20.04

RUN apt-get update && apt-get upgrade -y

COPY files/nointeractive.sh /tmp/
RUN chmod +x /tmp/nointeractive.sh && /tmp/nointeractive.sh

RUN apt-get install -y gcc g++ make qt5-qmake bison flex xxd git ssh

RUN apt-get install -y opencl-headers ocl-icd-opencl-dev curl apt-utils unzip tar curl xz-utils wget clinfo docker

RUN cd /tmp &&\
    curl --referer https://drivers.amd.com/drivers/linux -O https://drivers.amd.com/drivers/linux/amdgpu-pro-20.30-1109583-ubuntu-20.04.tar.xz &&\
    tar -Jxvf amdgpu-pro-20.30-1109583-ubuntu-20.04.tar.xz &&\
    cd amdgpu-pro-20.30-1109583-ubuntu-20.04/ &&\
    ./amdgpu-install -y  --headless --no-dkms --opencl=legacy

