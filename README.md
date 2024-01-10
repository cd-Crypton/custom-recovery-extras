# Custom Recovery Extras
Personal collection of files that needed when building custom recovery.

## Missing Fonts
Sometimes, building PBRP keeps on failing because of missing font. Here's what you need to do (make sure are in root directory of your recovery source):
```
cd external/noto-fonts/other && wget https://github.com/cd-Crypton/custom-recovery-extras/raw/main/missing-font.zip && unzip -o missing-font.zip && cd ../../..
```

## Missing Dependencies
In custom recovery tree, if you are trying to inherit `..virtual_ab_ota/compression.mk`, build system will fail due to missing dependencies for snapuserd, apparently gflags were missing. To fix that, do this:
```
mkdir -p external/gflags && cd external/gflags && wget https://github.com/cd-Crypton/custom-recovery-extras/raw/main/gflags.zip && unzip -o gflags.zip && cd ../..
```

# Notes
This is only a temporary fix, an alternative.
