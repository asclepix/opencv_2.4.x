### OpenCV: Open Source Computer Vision Library

#### on Ubuntu 22.04

This branch is a porting of old releases of openCV to Ubuntu 22.04.

**Main changes**

Since opencv 2.4.4, in file `cmake/OpenCVDetectCXXCompiler.cmake`, change `dumpversion` to `dumpfullversion`.

[Explanation](https://answers.opencv.org/question/65548/cmake-error-at-cmakeopencvdetectcxxcompilercmake/) is that in `gcc` with higher version, `dumpversion` function can't get true full version number of compiler so that `cmake` progress will fail.

----

    stdlib.h: No such file or directory

Disable pre-compiled headers, either from cmake-gui or using the command line parameter

    ENABLE_PRECOMPILED_HEADERS=OFF

----

Replace

    #include <sys/sysctl.h>

with

    #include <linux/sysctl.h>

----

Remove `throw` from method definitions.

#### Resources

* Homepage: <http://opencv.org>
* Docs: <http://docs.opencv.org>
* Q&A forum: <http://answers.opencv.org>
* Issue tracking: <http://code.opencv.org>

#### Contributing

Please read before starting work on a pull request: <http://code.opencv.org/projects/opencv/wiki/How_to_contribute>

Summary of guidelines:

* One pull request per issue;
* Choose the right base branch;
* Include tests and documentation;
* Clean up "oops" commits before submitting;
* Follow the coding style guide.
