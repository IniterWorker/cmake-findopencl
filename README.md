Ultimate FindOpenCL.cmake
=========================

FindOpenCL.cmake macro, which automatically finds OpenCL SDK in Windows (currently looks for Nvidia, Intel and AMD SDKs), OSX and Linux. In Windows it also tries linking if 32bit or 64bit lib versions should be used.

## Motivation

This was originally developed as a part of http://elhigu.github.io/opencl-testsuite/, but I believe that other projects could also benefit from this.

There are already few FindOpenCL.cmake macros available, but they usually didn't work well on three major platforms. Especially recognizing Windows OpenCL SDKs usually had problems and did require manually setting `OpenCL_INCPATH` and `OpenCL_LIBPATH`.

Also OSX implemantations usually did find only system OpenCL libraries and didn't allow to choose e.g. pocl or any other implementation to use for linking.

I've been developing this mostly on Windows and OSX so if there are any patches to make it work better in Linux, please send pull request. All contribution would be very much appreciated. 

## Try it out

```
git clone https://github.com/elhigu/cmake-findopencl.git
mkdir build
cmake ../cmake-findopencl
```