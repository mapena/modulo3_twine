++> crear paquete : python setup.py sdist bdist_wheel
    subir paquete : Twine upload -r nexus dist/* # -r can choose the warehouse address
    pip install basespiders -i http://localhost:8081/repository/mypypi-group/simple



===============================================
como usar en la la app test.py:

from libmulti.fmathmulti import *
print("multiplicar(3,4)=",multiplicar(3,4))