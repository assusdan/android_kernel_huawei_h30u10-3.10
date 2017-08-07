3.10.54 Kernel Source For Huawei H30U10
------

		sudo apt-get install ccache
		sudo gedit ~/.bashrc
Add these below lines at the end of .bashrc :

		export USE_CCACHE=1
		export CCACHE_DIR=~/android/.ccache

Build the kernel:

		sudo chmod -R 777 * ~/android_kernel_huawei_h30u10-3.10/arm-eabi-4.8
		cd ~/android_kernel_huawei_h30u10-3.10/kernel-3.10
		export ARCH=arm && export ARCH_MTK_PLATFORM=mt6582 && export CROSS_COMPILE=~/android_kernel_huawei_h30u10-3.10/arm-eabi-4.8/bin/arm-eabi-
		make clean
		make h30u10_defconfig
		./build.sh
