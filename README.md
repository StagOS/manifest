[<center><img src="https://i.pinimg.com/736x/8d/3d/04/8d3d049e47b6816f64ba2043782ae285.jpg" height="100%" width="100%;"/></center>](https://github.com/StagOS)

---------------
Getting started
---------------

To get started with Android, you'll need to get
familiar with [Repo](https://source.android.com/source/using-repo.html) and [Version Control with Git](https://source.android.com/source/version-control.html).
you'll also need to get
familiar with [Establishing a build environment](http://source.android.com/source/initializing.html).

To initialize your local repository using the StagOS sources, use a command like this:
```
repo init -u https://github.com/StagOS/manifest.git -b u14
```
Then to sync up:
```
repo sync -jx
```
or
```
repo sync --force-sync -c --no-clone-bundle --no-tags -jx
```
use this for faster sync. (x=no of cores to be used)

Building for your device [Compiler Friendly]
---------------
1) Make sure you've synced all your device specific sources 
2) Just continue building, file renaming and everything will be handled automatically.

[Advanced]
1) Make sure you've synced all your device specific sources
2) copy your device code from (lineage.mk/whatever.mk) to stag_devicename.mk
3) do the necessary changes in your trees
4) include vendor/stag/main.mk (no common.mk or common_full*)
5) Dont forget to set PRODUCT_DEVICE = devicename
6) Now you're all set to build. Follow the below commands 

```bash
source build/envsetup.sh
lunch stag_device-userdebug
make stag
```

## Any Errors ##
1) make sure you've followed the above instructions well, and check [StagOS-Devices](https://github.com/StagOS-Devices) for other device trees and see if you missed/need any of the changes done there 
2) Try to remember wether you've faced any similar error before and try to fix it first.
3) Search in your chat histories to see if anyone before has faced it (For telegram users, and trust me it helps a lot).
4) Searching the github and also lineage gerrit never harms.
5) Still facing the issue don't hesitate to ask in our [Telegram group](https://t.me/HornsOfficial)
6) Or you can just ask at Android Builders help group, (don't forget the rules/template it'd be sad to see you banned)

## Contact US ##
If you want to Maintain for your device
Compile the rom without any bugs and fill the form:
[Maintainer Form](https://maintainers.stag-os.org).  
Or if you just want to say a hi do the same below

[Telegram group](https://t.me/HornsOfficial)  [Telegram Channel](https://t.me/HornsUpdates)

Hope You Enjoy

## Maintaining Authorship ##
----------------
Please make sure if you submit a patch/fix from another ROM that you maintain authorship.
This is very important to not only us but to the entire open source community. It's what keeps it going and encourages more developers to contribute their work.

If you manually cherry pick a patch/fix please add the original author prior to pushing to our Gerrit.
This task is very easy and is usually done after you commit a patch/fix locally.

i.e - Once you type in "git commit -a" the commit message and you have saved it, type in the following:

```bash
git commit --amend --author "Author <email@address.com>"
```

So it should look like this once you get all author's information:

```bash
git commit --amend --author "vjspranav <pranavasri@live.in>"
```
