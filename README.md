## About this work

Most recent studies on deep learning based speech enhance-ment (SE) focused on improving denoising performance. However, successful SE applications require striking a desirable balance between denoising performance and computational cost in real scenarios. In this study, we propose a novelparameter pruning (PP) technique, which removes redundant channels in a neural network. In addition, a parameter quan-tization (PQ) technique was applied to reduce the size of aneural network by representing weights with fewer  clustercentroids. Because the techniques are derived based on dif-ferent concepts, the PP and PQ can be integrated to provideeven  more compact SE models. The experimental resultsshow that the PP and PQ techniques produce a compactedSE model with a size of only  9.76% compared to that of the original model, resulting in minor performance losses of 1.17% (from 0.85 to 0.84) for STOI and 1.17%(from 2.55to 2.52) for PESQ. The promising results suggest that the PPand PQ techniques can be used in an SE system in devices with limited storage and computation resources.

### Training/Testing environment setup

- Conda 8.0
- tensorflow-gpu 1.4.0
- Python 2.7
- Keras 1.1
- Nvidia GTX-1080Ti

```markdown
How to use the TIMIT_FCN_MSE.py

- Get python 2.7 environment
- Install Keras 1.1 (if you already have later version of Keras, please reinstall this version). 
- Fill in the GPU that is being used (default = 0, for 1 GPU computation resource, -1 for no CPU computation resource).
- Fill in the paths of the data expected to train/test with.
- Command: python TIMIT_FCN_MSE.py, you will get the model used in this work.
- This baseline model follows the settings in Fu, et.al's research: 
  <https://github.com/JasonSWFu/End-to-end-waveform-utterance-enhancement>
```
Normally, the learning curve of this model will be like the following graph:
![image](https://github.com/WilliamYu1993/ICSE/blob/master/images/Learning_curve_FCNN_TIMIT_MSE.png)



The proposed PP process be like:
![image](https://github.com/WilliamYu1993/ICSE/blob/master/images/pruning_overall.png)

The proposed PQ process be like:
![image](https://github.com/WilliamYu1993/ICSE/blob/master/images/process.png)

### Experimental Results
The integration of these two approaches achieved 10 times model compression ratio with minor performance drop, like:
- PESQ
![image](https://github.com/WilliamYu1993/ICSE/blob/master/images/FP1632_pesq.pdf)
- STOI
![image](https://github.com/WilliamYu1993/ICSE/blob/master/images/FP1632_stoi.pdf)

### Additional Experimental Results

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
