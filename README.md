Install gem RMagick on CentOS 5.5
======

 1)Copy 2 rpm from rpm dir to any dir (make sure you have executive permission)
------

    ImageMagick-6.6.6-3.x86_64.rpm
    ImageMagick-devel-6.6.6-3.x86_64.rpm

2)Delete old packages of ImageMagick
------

    yum erase ImageMagick
    
3)Install libraries:
------

    yum install libtool.x86_64 libtool-ltdl.x86_64 libtool-ltdl-devel.x86_64 libtiff.x86_64 libtiff-devel.x86_64 libjpeg.x86_64 libjpeg-devel.x86_64 libX11.x86_64 mesa-libGL.x86_64 libXt-devel.x86_64 
libXext.x86_64 libXext-devel.x86_64 lcms-devel.x86_64 lcms-devel.x86_64 jasper-devel.x86_64 ghostscript-devel.x86_64 freetype-devel.x86_64 bzip2-devel.x86_64

4)Install ImageMagick:
------

    rpm -Uvh ImageMagick-6.6.6-3.x86_64.rpm
    rpm -Uvh ImageMagick-devel-6.6.6-3.x86_64.rpm

5)Copy ImageMagick-6.6.6-3.tar.gz, unpack and install it:
------
    
    tar -zxvf ImageMagick-6.6.6-3.tar.gz
    cd ImageMagick-6.6.6-3
    ./configure
    make
    make install

6)Install RMagick gem
------

    gem install rmagick
