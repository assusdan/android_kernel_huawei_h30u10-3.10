3.10.54 Kernel Source For Micromax Unite 2
------

		sudo apt-get install ccache
		sudo gedit ~/.bashrc
Add these below lines at the end of .bashrc :

		export USE_CCACHE=1
		export CCACHE_DIR=~/android/.ccache

Build the kernel:

		sudo chmod -R 777 * ~/android_kernel_micromax_a106/arm-eabi-4.8
		cd ~/android_kernel_micromax_a106/kernel-3.10
		export ARCH=arm && export ARCH_MTK_PLATFORM=mt6582 && export CROSS_COMPILE=~/android_kernel_micromax_a106/arm-eabi-4.8/bin/arm-eabi-
		make clean
		make a106_defconfig
		./build.sh
