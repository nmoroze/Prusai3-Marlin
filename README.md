# Custom Prusa i3 Marlin Configuration

This is the Marlin firmware configuration for my 3D printer. My customized
files are tracked in the top-level, and the Marlin firmware itself is tracked
in a Git submodule for easy updates.

To update the Marlin firmware:
```
cd Marlin
git reset --hard # clear changes
git pull
git checkout <latest-release>
cd ..
```

And then commit the new submodule version.

To use the custom configuration, the corresponding Marlin files must be replaced
by my own:
```
cd Marlin/Marlin
ln -sf ../../Configuration.h Configuration.h
ln -sf ../../Configuration_adv.h Configuration_adv.h
```
