BootStrap: debootstrap
OSVersion: bionic 
MirrorURL: http://us.archive.ubuntu.com/ubuntu/


%runscript
    echo ""
    echo "Available programs:"
    echo "    Panorama Stitching"
    echo "        hugin"
    #echo "    Panorama Viewing"
    #echo "        Panini"
    echo "    RAW Photo Editing"
    echo "        darktable"
    echo "        rawtherapee" 
    #echo "        lightzone"
    echo "    HDR Photos"
    echo "        luminance-hdr"
    #echo "        hdrmerge"
    echo "    Photo Combination"
    echo "        photocollage"
    echo ""
    echo "Run a program with:    singularity exec <Container Name> <PROGRAM>"
    echo ""


%post
    sed -i 's/$/ universe/' /etc/apt/sources.list
    
    apt-get -y install software-properties-common #python-software-properties
    add-apt-repository ppa:ubuntuhandbook1/apps
    add-apt-repository ppa:dhor/myway

    apt-get -y update

    apt-get -y --force-yes install vim hugin darktable rawtherapee photocollage luminance-hdr 

