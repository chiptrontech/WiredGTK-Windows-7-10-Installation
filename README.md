# Wired-GTK Windows7/10
Download http://wirethemall.com/WiredGTK2.1Windows.zip
Follow Instructions in the readmelink.txt 


Python3.7 With Tensorflow and PyGobject installation

install miniconda
from start menu run Anaconda Prompt(miniconda3)

#this environment will be use for trianing tensorflow dataset
conda create --name tensorflow1_15 tensorflow==1.15
conda activate tensorflow1_15 
pip install pandas
pip install pillow

download models from https://github.com/tensorflow/models.git

1.extract to c:\tensorflow

2.rename models-master to models

make sure we are still in tensorflow1_15 virtual environment otherwise issue conda activate tensorflow1_15 

cd c:\tensorflow\models\research

protoc object_detection/protos/*.proto --python_out=.

python setup.py build

python setup.py install

conda deactivate tensorflow1_15 


#this environment will be use for WiredGTK with object_detection tensorflow detection

conda create --name wgtk tensorflow==2.0

conda activate wgtk 

conda install -c conda-forge gtk3

conda install -c conda-forge pygobject

conda install pillow

conda install -c conda-forge mysqlclient

conda install -c conda-forge opencv

pip install pandas

pip install requests

pip install pyserial

pip install imutils


cd c:\tensorflow\models\research

protoc object_detection/protos/*.proto --python_out=.

open label_map_util.py from c:\tensorflow\models\research\object_detection\utils

replace tf.gfile.GFile ===>>> tf.io.gfile.GFile

python setup.py build

python setup.py install

missing icons?

Download icon folder above extract it to c:\C:\Users\Acer\miniconda3\envs\wgtk\Library


run WiredGTK.bat

under Option-Runtime select python.exe in C:\Users\Acer\miniconda3\envs\wgtk	(Acer is your computer home)

open TensorflowTraining in WiredGTK(download it in my github repo)



Wired GTK 2.1 Screenshot may 2020
![](img.png)

