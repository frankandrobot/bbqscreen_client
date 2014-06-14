# Ubuntu Precise Notes

## Qt5
It seems that you need to manually compile Qt5. The instructions at http://qt-project.org/wiki/Building_Qt_5_from_Git are for the most part accurate.

However, instead of checking out `stable`, you will `git checkout v5.2.0`

**Note:** You don't have to install WebKit, so follow the instructions to NOT install it

**Note:** If you can't find `qmake` after running `sudo make install`, don't panic. It can be found in `qt5/qtbase/bin` directory. Update your `PATH`

	export PATH=$PATH:/<path to qt5>/qtbase/bin/ 
 
## ffmpeg

     sudo apt-get install yasm
     wget http://www.ffmpeg.org/releases/ffmpeg-2.1.3.tar.gz
     tar xvfa ffmpeg-2.1.3.tar.gz 
     cd ffmpeg-2.1.3/
     CFLAGS=-fPIC ./configure --disable-static --enable-shared
     make
     sudo make install

## Compiling BBQScreen
You'll need to update g++ to v4.7. Follow the instructions here: http://charette.no-ip.com:81/programming/2011-12-24_GCCv47/

