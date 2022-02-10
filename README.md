## Create Custom WSL Distros

### Create Distro

`docker run $IMAGE_NAME` \
`docker ps` (to get CONTAINER_ID) \
`sudo docker cp $CONTAINER_ID:/. ~/$DISTRO`

Once rootfs has been extracted/mounted:

`cd ~/$DISTRO` \
`sudo tar -zcvf ~/$DISTRO.tar.gz *`

### Install Distro

run `$DISTRO.exe` from directory with the compressed root file system renamed from `$DISTRO.tar.gz` to `rootfs.tar.gz` to register the distro with WSL.

Alternative is to use `wsl --import`.

