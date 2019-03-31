# tensorflow-avx2
a collection of custom builds of latest tensorflow with avx2 support


## windows
| link                                                                 | TF      | PY  | CPU/GPU  |
| -------------------------------------------------------------------- | ------- | --- | -------- |
| [fo40225](https://github.com/fo40225/tensorflow-windows-wheel)       | 1.4-1.9 | 36  | CPU, GPU |
| [aluo-x](https://github.com/aluo-x/tensorflow_windows)               | 1.5     | 36  | CPU      |
| [faisalthaheem](https://github.com/faisalthaheem/tensorflow-windows) | 1.4-1.8 | 35  | CPU      |

## linux
| link                                                            | TF            | PY    | CPU/GPU |
| --------------------------------------------------------------- | ------------- | ----- | ------- |
| [lakshayg](https://github.com/lakshayg/tensorflow-build)        | 1.1-1.10      | 35,36 | CPU,GPU |
| [inoryy](https://github.com/inoryy/tensorflow-optimized-wheels) | 1.10-1.13,2.0 | 36,37 | CPU     |
| [bukalapak](https://github.com/bukalapak/tensorflow-build)      | 1.10          | 35,36 | CPU     |

## miscellaneous
1. To view which wheel your platform supports, you can run blew code.

    Run
      ```
      from pip._internal.pep425tags import get_supported as f; print(f())
      ```
    If failed try 
      ```
      from pip.pep425tags import get_supported as f; print(f())
      ```
2. **Do not rename whl filename** e.g. `..._amd64.whl` to `..._amd64(avx2).whl`, or rename back before installation.
   The `pip` identifies the file by its filename. Otherwise you will fail with "**`whl is not a supported wheel on this platform`**".