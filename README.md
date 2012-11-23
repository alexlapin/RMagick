Install gem RMagick on CentOS 5.5
======

<h3>1. Copy 2 rpm from rpm dir to any dir (make sure you have executive permission)</h3>

    ImageMagick-6.6.6-3.x86_64.rpm
    ImageMagick-devel-6.6.6-3.x86_64.rpm

<h3>2. Delete old packages of ImageMagick</h3>

    yum erase ImageMagick
    
<h3>3. Install libraries:</h3>

    yum install libtool.x86_64 libtool-ltdl.x86_64 libtool-ltdl-devel.x86_64 libtiff.x86_64 libtiff-devel.x86_64 libjpeg.x86_64 libjpeg-devel.x86_64 libX11.x86_64 mesa-libGL.x86_64 libXt-devel.x86_64 libXext.x86_64 libXext-devel.x86_64 lcms-devel.x86_64 lcms-devel.x86_64 jasper-devel.x86_64 ghostscript-devel.x86_64 freetype-devel.x86_64 bzip2-devel.x86_64

<h3>4. Install ImageMagick:</h3>

    rpm -Uvh ImageMagick-6.6.6-3.x86_64.rpm
    rpm -Uvh ImageMagick-devel-6.6.6-3.x86_64.rpm

<h3>5. Copy ImageMagick-6.6.6-3.tar.gz, unpack and install it:</h3>
    
    tar -zxvf ImageMagick-6.6.6-3.tar.gz
    cd ImageMagick-6.6.6-3
    ./configure
    make
    make install
    
<h3>6. Set the right path</h3>

    PKG_CONFIG_PATH=/usr/local/lib/pkgconfig/
    
<h3>7. Install RMagick gem</h3>

    gem install rmagick
