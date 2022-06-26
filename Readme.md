Liens de la méthode GFPGAN : 
* https://xinntao.github.io/projects/gfpgan 
* https://github.com/TencentARC/GFPGAN
 
 
Etape a suivre pour executer le script:

1- Telecharger le dossier **GFPGAN-master**

2- Installer Pytorch a partir de https://pytorch.org/get-started/locally/ ou utiliser cette commande:

*pip3 install torch torchvision torchaudio --extra-index-url https://download.pytorch.org/whl/cu113*

3- Installer les librairies : 
  * pip install opencv-python scipy tqdm yapf lmdb pyyaml
  * pip install opencv-python-headless==4.5.2.52
  * pip install basicsr facexlib realesrgan
 
4- Execute la commande : python setup.py develop
  
Telecharger les pre-trained models: (mettez-les dans le repertoire suivant: .../GFPGAN-master/experiments/pretrained_models)
* Version 1.3: https://github.com/TencentARC/GFPGAN/releases/download/v1.3.0/GFPGANv1.3.pth
* Version 1.2: https://github.com/TencentARC/GFPGAN/releases/download/v0.2.0/GFPGANCleanv1-NoCE-C2.pth

Mettez les images inputs dans le repertoire suivant: .../GFPGAN-master/inputs/whole_imgs

Executer l'une des commandes suivantes: 
* python inference_gfpgan.py -i inputs/whole_imgs -o results -v 1.3 -s 2 (Version 1.3)
* python inference_gfpgan.py -i inputs/whole_imgs -o results -v 1.2 -s 2 (Version 1.2)


Les resultats seront dans le repertoire suivant: .../GFPGAN-master/results


# **IMPORTANT**: 

Il faut un gpu pour exécuter la version v1 en local, c'est la version de l'article, celle que nous avons utilisé.
Vous pouvez tester cette version sur colab.

Les versions v1.2 et v1.3 de la technique peuvent être exécuté en local sans gpu. Elle donnent des résultats différents
par exemple elle ne font pas la colorisation.

Comparaisons entre les versions : 
https://github.com/TencentARC/GFPGAN/blob/master/Comparisons.md
