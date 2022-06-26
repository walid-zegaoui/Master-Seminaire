Link of the Method GFPGAN : 
* https://xinntao.github.io/projects/gfpgan 
* https://github.com/TencentARC/GFPGAN
 
 
Steps to run the scripts:

1- Download the folder **GFPGAN-master**

2- Install Pytorch from https://pytorch.org/get-started/locally/ or use this command:

*pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu113*

3- Install libraries : 
  * pip install opencv-python scipy tqdm yapf lmdb pyyaml
  * pip install opencv-python-headless==4.5.2.52
  * pip install basicsr facexlib realesrgan
 
4- Execute this command : python setup.py develop
  
Download pre-trained models: (put them in the directory: .../GFPGAN-master/experiments/pretrained_models)
* Version 1.3: https://github.com/TencentARC/GFPGAN/releases/download/v1.3.0/GFPGANv1.3.pth
* Version 1.2: https://github.com/TencentARC/GFPGAN/releases/download/v0.2.0/GFPGANCleanv1-NoCE-C2.pth

Put the inputs images on the directory: .../GFPGAN-master/inputs/whole_imgs

Run this command to execute the script: 
* python inference_gfpgan.py -i inputs/whole_imgs -o results -v 1.3 -s 2 (Version 1.3)
* python inference_gfpgan.py -i inputs/whole_imgs -o results -v 1.2 -s 2 (Version 1.2)


The results will be in the directory: .../GFPGAN-master/results


# **IMPORTANT**: 

Il faut un gpu pour exécuter la version v1 en local, c'est la version de l'article, celle que nous avons utilisé.
Vous pouvez tester cette version sur colab.

Les versions v1.2 et v1.3 de la technique peuvent être exécuté en local sans gpu. Elle donnent des résultats différents
par exemple elle ne font pas la colorisation.

Comparaisons entre les versions : 
https://github.com/TencentARC/GFPGAN/blob/master/Comparisons.md
