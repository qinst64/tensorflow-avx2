# tensorflow-avx2
a collection of custom builds of tensorflow with avx2 support


## windows
|link|TF|PY|CPU/GPU|
|---|---|---|---|
|[aluo-x](https://github.com/aluo-x/tensorflow_windows)|1.4|36|CPU|
|[fo40225](https://github.com/fo40225/tensorflow-windows-wheel)|1.4|36|CPU,GPU|
|[faisalthaheem](https://github.com/faisalthaheem/tensorflow-windows)|1.4|35|CPU|


## linux and macosx
Refer to this good entry: [lakshayg](https://github.com/lakshayg/tensorflow-build), which includes TF1.1-1.4, PY27/35/36, CPU/GPU


## miscellaneous
1. To view which wheel your platform supports, you can run blew code.
      ```
      import pip
      print(pip.pep425tags.get_supported())
      ```
2. **Do not rename whl filename** e.g. `..._amd64.whl` to `..._amd64(avx2).whl`, or rename back before installation.
   The `pip` identifies the file by its filename. Otherwise you will fail with "**`whl is not a supported wheel on this platform`**".
