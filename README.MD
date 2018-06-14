
<p align='center'><img width='450' src='https://preview.ibb.co/dwerHy/00111.png'/></p>

# <center>Electronic music styles Neural Net</center> 

The repository contains the model, a convolution neural network, which was trained to distinguish 12 different styles of modern electronic music, trained to classify 12 classes. **Keras** model `.h5` and **super handy** Jupyter Notebook `.ipynb` as a guide with details are provided. Starring *Tensorflow* as backend.

## Data

The network was trained on a private dataset of labeled raw audio, processed as Mel Spectrograms. Data will not be provided. 12 electronic music styles (i.e. classes) are:

 - Ambient / Electronic (downtempo, abstract);
 - Brostep (*Dubstep*, as it more popularly known, songs of *Skrillex*, *MUST DIE!*, *Kill The Noise* and the others);
 - Deep House (proggy and techy, from the likes of *Anjunadeep*);
 - Drum & Bass (techstep, Neurofunk, liquid funk among the others);
 - EDM & Big Room (SHM, Hardwell, Martin Garrix and the others);
 - Electro & Future House;
 - Trance (Uplifting, psy, stadium);
 - Halftime (*Drum & Bass* subgenre with the same tempo, but with a half less drum kicks);
 - House / Nu Disco / Disco;
 - Progressive House (also, its modern form, mostly);
 - Techno / Tech House;
 - Trap
 
A potential problem with the model reasoning is objectivity since the data was labeled manually mostly. The goal of choosing exactly them is to check ability to distinguish relatively similar styles. Like, distinguish the style of Trap from Halftime.

## How good is it?

You can find the full description of model inference in `handy_guide.ipynb`. 

We evaluate our model in terms of Precision @ K:

 - Precision @ **1** = 67% (i.e. accuracy, *top one class*)
 - Precision @ 2 = 83% (*top two classes*)
 - Precision @ 3 = **89%** (*three top classes*)
 
## Requirements
FFMPEG | `ffmpeg version N-91266-g8c20ea8ee0` | https://www.ffmpeg.org/

Python 3.6.5 package requirements:
```
tensorflow-gpu==1.8.0
librosa==0.6.1
keras==2.1.6
mutagen==1.40.0
kapre==0.1.3
numpy==1.14.3
pandas==0.23.0
```
All together in requirements.txt. Sitting in the directory, execute
`pip3 install -r requirements.txt`

## All the sources of priceless knowledges

Transfer learning for music classification and regression tasks | https://arxiv.org/abs/1703.09179
AUTOMATIC TAGGING USING DEEP CONVOLUTIONAL NEURAL NETWORKS – Keunwoo Choi, et al ｜ [https://arxiv.org/abs/1606.00298](https://arxiv.org/abs/1606.00298)
Recommending music on Spotify with deep learning | http://benanne.github.io/2014/08/05/spotify-cnns.html
Japan company QOSMO AI DJ Project | http://qosmo.jp/projects/2016/11/21/ai-dj-human-dj-b2b/
