# MojoSetup installers

In order to execute the installers build MojoSetup:

```
hg clone https://hg.icculus.org/icculus/mojosetup
wget https://liflg.org/fix_translations.patch
patch mojosetup/scripts/localization.lua fix_translations.patch
mkdir mojosetup/build
cd mojosetup/build
cmake ..
make -j $(nproc) skeleton
```

Get the installer of your choice, e.g. Unreal Tournament and copy its content to the *skeleton* direcory:
```
git clone https://github.com/liflg/unreal.tournament_451-english_x86.git
cp -pr unreal.tournament_451-english_x86/* skeleton/
cd skeleton
./mojosetup
```
