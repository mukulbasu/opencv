## OpenCV: Open Source Computer Vision Library

### Resources

* Homepage: <https://opencv.org>
  * Courses: <https://opencv.org/courses>
* Docs: <https://docs.opencv.org/4.x/>
* Q&A forum: <https://forum.opencv.org>
  * previous forum (read only): <http://answers.opencv.org>
* Issue tracking: <https://github.com/opencv/opencv/issues>
* Additional OpenCV functionality: <https://github.com/opencv/opencv_contrib> 


### Attribution
This is a fork from https://github.com/opencv/opencv.git for the purpose of using it with slamJS.

### Building
There are 2 ways to build it. Building it for testing with slamJS with CPP or building it for using with JS.

#### CPP build
##### Building opencv
* mkdir build; cd build; rm -rf *
* cmake -DENABLE_PIC=FALSE -DCMAKE_BUILD_TYPE=Release -DCPU_DISPATCH='' -DCV_TRACE=OFF -DBUILD_SHARED_LIBS=OFF -DWITH_1394=OFF -DWITH_ADE=OFF -DWITH_VTK=OFF -DWITH_EIGEN=ON -DWITH_FFMPEG=OFF -DWITH_GSTREAMER=OFF -DWITH_GTK=OFF -DWITH_GTK_2_X=OFF -DWITH_IPP=OFF -DWITH_JASPER=OFF -DWITH_JPEG=ON -DBUILD_JPEG=ON -DBUILD_OPENJPEG=ON -DWITH_WEBP=OFF -DWITH_OPENEXR=OFF -DWITH_OPENGL=OFF -DWITH_OPENVX=OFF -DWITH_OPENNI=OFF -DWITH_OPENNI2=OFF -DWITH_PNG=ON -DBUILD_PNG=ON -DWITH_TBB=OFF -DWITH_TIFF=OFF -DWITH_V4L=OFF -DWITH_OPENCL=OFF -DWITH_OPENCL_SVM=OFF -DWITH_OPENCLAMDFFT=OFF -DWITH_OPENCLAMDBLAS=OFF -DWITH_GPHOTO2=OFF -DWITH_LAPACK=OFF -DWITH_ITT=OFF -DWITH_QUIRC=ON -DBUILD_ZLIB=OFF -DBUILD_opencv_apps=OFF -DBUILD_opencv_calib3d=ON -DBUILD_opencv_dnn=ON -DBUILD_opencv_features2d=ON -DBUILD_opencv_flann=ON -DBUILD_opencv_gapi=OFF -DBUILD_opencv_ml=OFF -DBUILD_opencv_photo=ON -DBUILD_opencv_imgcodecs=ON -DBUILD_opencv_shape=OFF -DBUILD_opencv_videoio=OFF -DBUILD_opencv_videostab=OFF -DBUILD_opencv_highgui=ON -DBUILD_opencv_superres=OFF -DBUILD_opencv_stitching=OFF -DBUILD_opencv_java=OFF -DBUILD_opencv_js=OFF -DBUILD_opencv_python2=OFF -DBUILD_opencv_python3=OFF -DBUILD_EXAMPLES=OFF -DBUILD_PACKAGE=OFF -DBUILD_TESTS=OFF -DBUILD_PERF_TESTS=OFF ..
* make -j20
* copy all the files in build/lib/* to slamJS/third_party/lib/opencv/<arch>/
* copy all the files in build/3rdparty/lib/* to slamJS/third_party/lib/opencv/<arch>/


#### JS build
* Go to platforms/js/
* source buildscript.sh
* copy jspackage/bin/opencv.js to slamJS/third_party/lib/opencv/js/
