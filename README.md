  Unknamed Rom
=====================
Based on PureFusion OS
---------------

Getting Started
---------------

To build PureFusion from source, you'll need to be familiar with
[Git and Repo](http://source.android.com/download/using-repo).


To initialize your local repository, use this command:

	repo init -u https://github.com/buddery/manifest.git -b n-mr2

Then to sync up:

    repo sync -c -f -j8 --force-sync --no-clone-bundle --no-tags
    
##### Setting Up CCache
- CCache is a method of utilizing a specified storage space to speed up building. It can be referred to as the same caching your android device does to speed up application and system boot times. In this case, CCache will help build Pure Fusion faster than standard build times (Able to cut-down 50% of time taken to build).
- To set up CCache, follow the following:


        $ echo "export USE_CCACHE=1" >> ~/.bashrc
      
        $ prebuilts/misc/linux-x86/ccache/ccache -M 50G

     -M 50G
The number before the letter G at the end specifies the amount of space CCache can use in your storage unit. As such, ensure that not too much of space is specified as this might result in unexpected errors although, the more storage you have, its recommended to have more CCache as it will increase the build times. Most efficient build systems are able to utilize CCache to about 120G or more.    
   

After syncing is done, do one of the following to build:

    bash build.sh --help

OR

    1.) . build/envsetup.sh
    2.) brunch device-user/userdebug/eng

Enjoy, Stick around for a while AOSP Building is Fun!!!

##### Contributing - Gerrit
Please do not directly submit pull requests to our github. In order to contribute to our project, you will need to have a gerrit account on our server. Our official gerrit server resides at https://review.purefusionos.com/.

Instructions on submitting code for review can be found [here](https://review.purefusionos.com/Documentation/user-upload.html)
Instructions on submitting using the repo command can be found [here](https://source.android.com/source/using-repo) (recommended - must have full Android source tree synced)

##### Sources
A fork of PureFusionOS have used a mixture of PureNexusProject and PureNexusProject-Mod as a base for their ROM.

PureFusionOS https://github.com/PurefusionOS (PureFusionOS project)
[PureNexusProject-Mod](https://github.com/PureNexusProject-Mod/) (original source PureNexusProject-Mod)

[PureNexusProject](https://github.com/PureNexusProject) (original source PureNexusProject)


