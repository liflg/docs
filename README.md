# MojoSetup installers

In order to execute the installers build MojoSetup:

```
git clone https://github.com/icculus/mojosetup.git
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
