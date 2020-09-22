    crear paquete con bdist_wheel : python setup.py sdist bdist_wheel  

     C:\gh\modulo3_twine>python setup.py sdist bdist_wheel
        running sdist
        running egg_info
        writing paqmulti.egg-info\PKG-INFO
        writing dependency_links to paqmulti.egg-info\dependency_links.txt
        writing top-level names to paqmulti.egg-info\top_level.txt
        reading manifest file 'paqmulti.egg-info\SOURCES.txt'
        writing manifest file 'paqmulti.egg-info\SOURCES.txt'
        running check
        creating paqmulti-1.0.1
        creating paqmulti-1.0.1\libmulti
        creating paqmulti-1.0.1\paqmulti.egg-info
        copying files to paqmulti-1.0.1...
        copying README.md -> paqmulti-1.0.1
        copying setup.py -> paqmulti-1.0.1
        copying libmulti\__init__.py -> paqmulti-1.0.1\libmulti
        copying libmulti\fmathmulti.py -> paqmulti-1.0.1\libmulti
        copying paqmulti.egg-info\PKG-INFO -> paqmulti-1.0.1\paqmulti.egg-info
        copying paqmulti.egg-info\SOURCES.txt -> paqmulti-1.0.1\paqmulti.egg-info
        copying paqmulti.egg-info\dependency_links.txt -> paqmulti-1.0.1\paqmulti.egg-info
        copying paqmulti.egg-info\top_level.txt -> paqmulti-1.0.1\paqmulti.egg-info
        Writing paqmulti-1.0.1\setup.cfg
        Creating tar archive
        removing 'paqmulti-1.0.1' (and everything under it)
        running bdist_wheel
        running build
        running build_py
        creating build
        creating build\lib
        creating build\lib\libmulti
        copying libmulti\fmathmulti.py -> build\lib\libmulti
        copying libmulti\__init__.py -> build\lib\libmulti
        installing to build\bdist.win32\wheel
        running install
        running install_lib
        creating build\bdist.win32
        creating build\bdist.win32\wheel
        creating build\bdist.win32\wheel\libmulti
        copying build\lib\libmulti\fmathmulti.py -> build\bdist.win32\wheel\.\libmulti
        copying build\lib\libmulti\__init__.py -> build\bdist.win32\wheel\.\libmulti
        running install_egg_info
        Copying paqmulti.egg-info to build\bdist.win32\wheel\.\paqmulti-1.0.1-py3.8.egg-info
        running install_scripts
        creating build\bdist.win32\wheel\paqmulti-1.0.1.dist-info\WHEEL
        creating 'dist\paqmulti-1.0.1-py3-none-any.whl' and adding 'build\bdist.win32\wheel' to it
        adding 'libmulti/__init__.py'
        adding 'libmulti/fmathmulti.py'
        adding 'paqmulti-1.0.1.dist-info/METADATA'
        adding 'paqmulti-1.0.1.dist-info/WHEEL'
        adding 'paqmulti-1.0.1.dist-info/top_level.txt'
        adding 'paqmulti-1.0.1.dist-info/RECORD'
        removing build\bdist.win32\wheel

++> crear paquete sin bdist_wheel : python setup.py sdist 
    subir paquete : Twine upload -r nexus dist/*

        C:\gh\modulo3_twine> Twine upload -r nexus dist/*
        Uploading distributions to http://localhost:8081/repository/mirepo-hosted/
        Uploading paqmulti-1.0.0.tar.gz
        100%|██| 4.21k/4.21k [00:01<00:00, 3.71kB/s]



    pip install paqmulti -i http://localhost:8081/repository/mirepo-group/simple



===============================================
como usar en la la app test.py:

from libmulti.fmathmulti import *
print("multiplicar(3,4)=",multiplicar(3,4))