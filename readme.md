
# Script para generación y crop de imágenes con formatos preestablecidos (alta, media, baja) con criterios de modelo OpenCV


## Motivación

Para plataformas que se necesite tener imágenes en múltiples formatos (alta, media baja), es engorroso tener que dedicarle mucho tiempo a un proceso que podría hacerse manual. El problema de automatizar el cropeo o recorte de fotos es que si se automatiza sin criterio, se puede llegar a obtener resultados que no favorecen el output (por ejemplo incluyendo en la zona de corte cosas que no son de interés o que hubiese sido mejor un corte diferente incluyendo objetos identificables como casas, obras, personas, carteles). 

La idea de este pequeño proyecto es poder automatizar el corte de fotos con algún criterio de detección de objetos o valoración de los objetos para la zona de corte.

Para esto se encontraron 2 librerías y estos scripts simplemente automatizan la ejecución de dichas librerías.

Se realizaron pruebas con ambas librerías, obteniendo mejores resultados con la versión 1 del script publicado en dicho repo.


## Requerimientos

### Versión 1 

Utiliza: 

* Open CV https://pypi.org/project/opencv-python/ (pip install opencv-python)
* Smartcrop https://github.com/epixelic/python-smart-crop (pip install git+https://github.com/epixelic/python-smart-crop)


### Versión 2 

Utiliza:

* Smartcroppy https://github.com/smartcrop/smartcrop.py (pip install -e git+git://github.com/hhatto/smartcrop.py.git@master#egg=smartcrop)


## Instalación de entorno y librerías

Usar venv para entorno virtual python:
- python -m venv venv
- source venv/scripts/activate
- pip install -r requirements.txt

## ejecución

### Versión 1

Se ejecutan las lineas por foto:

python v1_run.py

**Se obtuvieron mejores resultados con version 1**

### Versión 2

python v2_run.py

## proceso

ambos recorren la carpeta img_demo y dejan las salidas en output

## to-do

* dejar el json de tamaño por fuera del script.

* probar con más fotos (se realizaron pruebas con stock de 20 fotos con buenos resultados).

* sumar un py unit-test.

* Poder clasificar "buenas fotos" de obra vs "malas fotos de obra", dandole así un peso de publicación a la foto.

