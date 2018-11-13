BootStrap: debootstrap
OSVersion: xenial
MirrorURL: http://us.archive.ubuntu.com/ubuntu/

%post

    echo "deb http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial-backports main restricted universe multiverse" | tee -a /etc/apt/sources.list
    echo "deb http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial main restricted" | tee -a /etc/apt/sources.list
    echo "deb http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial multiverse" | tee -a /etc/apt/sources.list
    echo "deb http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial universe" | tee -a /etc/apt/sources.list
    echo "deb http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial-updates main restricted" | tee -a /etc/apt/sources.list
    echo "deb http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial-updates multiverse" | tee -a /etc/apt/sources.list
    echo "deb http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial-updates universe" | tee -a /etc/apt/sources.list
    echo "deb http://security.ubuntu.com/ubuntu xenial-security main restricted" | tee -a /etc/apt/sources.list
    echo "deb http://security.ubuntu.com/ubuntu xenial-security multiverse" | tee -a /etc/apt/sources.list
    echo "deb http://security.ubuntu.com/ubuntu xenial-security universe" | tee -a /etc/apt/sources.list
    echo "deb-src http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial-backports main restricted universe multiverse" | tee -a /etc/apt/sources.list
    echo "deb-src http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial main restricted" | tee -a /etc/apt/sources.list
    echo "deb-src http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial multiverse" | tee -a /etc/apt/sources.list
    echo "deb-src http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial universe" | tee -a /etc/apt/sources.list
    echo "deb-src http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial-updates main restricted" | tee -a /etc/apt/sources.list
    echo "deb-src http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial-updates multiverse" | tee -a /etc/apt/sources.list
    echo "deb-src http://nova.clouds.archive.ubuntu.com/ubuntu/ xenial-updates universe" | tee -a /etc/apt/sources.list
    echo "deb-src http://security.ubuntu.com/ubuntu xenial-security main restricted" | tee -a /etc/apt/sources.list
    echo "deb-src http://security.ubuntu.com/ubuntu xenial-security multiverse" | tee -a /etc/apt/sources.list
    echo "deb-src http://security.ubuntu.com/ubuntu xenial-security universe" | tee -a /etc/apt/sources.list

    apt-get -y update
    apt-get -y upgrade

    apt-get -y install wget

    mkdir MCR
    wget -p MCR http://ssd.mathworks.com/supportfiles/downloads/R2017b/deployment_files/R2017b/installers/glnxa64/MCR_R2017b_glnxa64_installer.zip

    cd MCR
    unzip MCR_R2017b_glnxa64_installer.zip
    ./install -mode silent -agreeToLicense yes -destinationFolder $HOME/MATLAB/MATLAB_Runtime/v93
    cd ..
    rm -rf MCR
