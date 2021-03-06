### Versions
    Windows10, Cuda8.0, CuDnn6.0, tensorflow1.3.0, anaconda4.2.0(python3.5.2), pyqt5, dlib19.12, opencv3.1.0, opencv2.4.9.1 ...
### Packages

    cuda
    download cuda8.0, cudnn6.0
    $ set
    $ set cudnn_path=
    $ set path=%path%;%cudnn_path%
    
    pip
    $ wget https://bootstrap.pypa.io/get-pip.py
    $ python get-pip.py
       
    dlib-build
    $ wget http://dlib.net/files/dlib-19.12.tar.bz2
    $ tar xvf dlib-19.12.tar.bz2
    #$ cd dlib-19.12/
    $ cd dlib-19.12
    $ pip install cmake
    $ python setup.py install

    tensorflow
    $ pip install -U tensorflow-gpu==1.3.0
          
    opencv
    $ conda install -c menpo opencv3==3.1.0
      
### Code-SSD/OpenAlpr...

   - [SSD]()
   
    $ git clone http://github.com/gustavkkk/surveillance-system.git
    $ cd surveillance-system
    $ mkdir checkpoints
    $ curl -o ssd_300_vgg.ckpt.zip https://raw.githubusercontent.com/balancap/SSD-Tensorflow/master/checkpoints/ssd_300_vgg.ckpt.zip
    $ unzip ssd_300_vgg.ckpt.zip checkpoints
   
   - [OpenAlpr](https://github.com/openalpr/openalpr/issues/660)
   
    $ sudo apt-get install libopencv-dev libtesseract-dev git cmake build-essential libleptonica-dev
    $ sudo apt-get install liblog4cplus-dev libcurl3-dev
    # If using the daemon, install beanstalkd
    $ sudo apt-get install beanstalkd
    # Clone the latest code from GitHub
    $ git clone https://github.com/openalpr/openalpr.git
    # Setup the build directory
    $ cd openalpr/src
    $ mkdir build
    $ cd build
    # setup the compile environment
    $ cmake -DCMAKE_INSTALL_PREFIX:PATH=/usr -DCMAKE_INSTALL_SYSCONFDIR:PATH=/etc ..
    # compile the library
    $ make
    # Install the binaries/libraries to your local system (prefix is /usr)
    $ sudo make install
    # Test the library
    $ wget http://plates.openalpr.com/h786poj.jpg -O lp.jpg
    $ alpr lp.jpg
    $ cd ../src/binding/python
    $ python setup.py install
    
   - [face_recognition](https://github.com/ageitgey/face_recognition)
   
    $ pip download face_recognition==1.2.2
    $ pip install face_recognition==1.2.2
   
### Installation Validation
    $ nvcc --version
    $ nvidia-smi

