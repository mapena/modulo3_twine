    crear paquete con bdist_wheel : python setup.py sdist bdist_wheel
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