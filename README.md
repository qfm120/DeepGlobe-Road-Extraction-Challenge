# DeepGlobe-Road-Extraction-Challenge
Code for the 1st place solution in [DeepGlobe Road Extraction Challenge](https://competitions.codalab.org/competitions/18467).

# Requirements

- Cuda 8.0
- Python 2.7
- Pytorch 0.2.0
- cv2

# Usage

### Data
Place '*train*', '*valid*' and '*test*' data folders in the '*dataset*' folder.

Data is from [DeepGlobe Road Extraction Challenge](https://competitions.codalab.org/competitions/18467#participate-get_starting_kit). You should sign in first to get the data.

You also can download the data from the URL: https://pan.baidu.com/s/1tsUsXj_ohgWuSY4VL3grxg Extraction code: xqsj

### Train
- Run `python train.py` to train the default D-LinkNet34.

### Predict
- Run `python test.py` to predict on the default D-LinkNet34.

If an "out of memory" error occured in the procedure of training or testing, you should resize the input images into a small ones and decrease the batch size. 
e.g., you may need to insert the following code into the front of reading images ops.
crop_size=(512,512)
img=cv2.resize(img,crop_size,interpolation=cv2.INTER_CUBIC)

### Download trained D-LinkNet34
- [Dropbox](https://www.dropbox.com/sh/h62vr320eiy57tt/AAB5Tm43-efmtYzW_GFyUCfma?dl=0)
- [百度网盘](https://pan.baidu.com/s/1wqyOEkw5o0bzbuj7gBMesQ)
