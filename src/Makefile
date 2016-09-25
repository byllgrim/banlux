include config.mk

all: linux_get linux_install

linux_get:
	mkdir -p ./linux
	-git clone ${LINUXGIT} ./linux

linux_install:
	mkdir -p ../boot
	cd ./linux && \
		git pull && \
		make defconfig && \
		make -j4 && \
		INSTALL_PATH=../../boot make install && \
		INSTALL_MOD_PATH=../.. make modules_install
