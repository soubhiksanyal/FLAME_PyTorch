## FLAME: Faces Learned with an Articulated Model and Expressions (PyTorch)
This is an implementation of the [FLAME](http://flame.is.tue.mpg.de/) 3D head model in PyTorch.

# FLAME

FLAME is a lightweight and expressive generic head model learned from over 33,000 of accurately aligned 3D scans. This repository provides sample PyTorch code to experiment with the FLAME model. For details how to adapt FLAME to images or 3D meshes, see the [Chumpy](https://github.com/Rubikplayer/flame-fitting) or the [Tensorflow](https://github.com/TimoBolkart/TF_FLAME) FLAME repositories.

<p align="center"> 
<img src="gifs/model_variations.gif">
</p>

FLAME combines a linear identity shape space (trained from 3800 scans of human heads) with an articulated neck, jaw, and eyeballs, pose-dependent corrective blendshapes, and additional global expression blendshapes. For details please about the model, please see the [scientific publication](https://ps.is.tuebingen.mpg.de/uploads_file/attachment/attachment/400/paper.pdf) and the [supplementary video](https://youtu.be/36rPTkhiJTM).

## Installation

The code uses **Python 3.7** and it is tested on PyTorch 1.4.

### Setup FLAME PyTorch Virtual Environment

```
python3.7 -m venv <your_home_dir>/.virtualenvs/FLAME_PyTorch
source <your_home_dir>/.virtualenvs/FLAME_PyTorch/bin/activate
```
### Clone the project and install requirements

```
git clone https://github.com/soubhiksanyal/FLAME_PyTorch
cd FLAME_PyTorch
pip install -r requirements.txt
mkdir model
```

## Download models

* Download FLAME model from [here](http://flame.is.tue.mpg.de/). Copy it inside the **model** folder. 
* Download Landmark embedings from [RingNet Project](https://github.com/soubhiksanyal/RingNet/tree/master/flame_model). Copy it inside the **model** folder. 

## Demo

#### Loading FLAME and visualising the 3D landmarks on the face

Please note we used the pose dependent conture for the face as intriduced by [RingNet Project](https://github.com/soubhiksanyal/RingNet/tree/master/flame_model).

Run the following command from the terminal

```
python main.py
```

## License

FLAME is available under [Creative Commons Attribution license](https://creativecommons.org/licenses/by/4.0/). By using the model or the code code, you acknowledge that you have read the license terms (http://flame.is.tue.mpg.de/model_license), understand them, and agree to be bound by them. If you do not agree with these terms and conditions, you must not use the code.

## Referencing FLAME

When using this code in a scientific publication, please cite 
```
@article{FLAME:SiggraphAsia2017,
  title = {Learning a model of facial shape and expression from {4D} scans},
  author = {Li, Tianye and Bolkart, Timo and Black, Michael. J. and Li, Hao and Romero, Javier},
  journal = {ACM Transactions on Graphics, (Proc. SIGGRAPH Asia)},
  volume = {36},
  number = {6},
  year = {2017},
  url = {https://doi.org/10.1145/3130800.3130813}
}
```
## Supported Projects

FLAME supports several projects such as

* [RingNet: 3D Face Shape and Expression Reconstruction from an Image without 3D Supervision](https://github.com/soubhiksanyal/RingNet)
* [VOCA: Voice Operated Character Animation](https://github.com/TimoBolkart/voca)
* [Expressive Body Capture: 3D Hands, Face, and Body from a Single Image](https://github.com/vchoutas/smplify-x)

FLAME is part of [SMPL-X: : A new joint 3D model of the human body, face and hands together](https://github.com/vchoutas/smplx)

## Contact

If you have any questions regarding the PyTorch implementation then you can contact us at soubhik.sanyal@tuebingen.mpg.de and timo.bolkart@tuebingen.mpg.de.

## Acknowledgement 

This repository is build with modifications from [SMPLX](https://github.com/vchoutas/smplx).
