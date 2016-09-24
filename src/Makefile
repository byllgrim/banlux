include config.mk

all: linux

linux:
	git clone ${LINUXGIT} ./linux/
	cd ./linux/ && \
		make defconfig && \
		make && \
		INSTALL_PATH=../boot/ make install && \
		INSTAL_MOD_PATH=../ make modules_install
