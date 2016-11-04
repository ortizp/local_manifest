Welcome to Cyanogenmod ROM for LG L70
=====================================


Instructions
---------------

Initializing:

First, create a folder to hold the source code: 

	mkdir ~/cm-13.0

Next..

	cd ~/cm-13.0

Initialize local repository:

	repo init -u git://github.com/CyanogenMod/android.git -b cm-13.0

Also add the local manifests:

    git clone https://github.com/ortizp/local_manifestt -b cm-13.0 .repo/local_manifests

Sync up:

	repo sync --force-sync
	
---------------
 
_Building_
---------------

First:

	cd ~/cm-13.0
	echo "export USE_CCACHE=1" >> ~/.bashrc
	~/cm-13.0/prebuilts/misc/linux-x86/ccache/ccache -M 30G

Second:

	. build/envsetup.sh && brunch codename example: brunch mako
