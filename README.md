# horse2zebras-GAN
**horse2zebras Cycle GAN (weights included). [ENG]**

Task
-----------------------------------
The task was to turn the horses in the photo into zebras and vice versa.

![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/3sYrRpR2fso.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/9z4SwUr53-k.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/GNx9bEQZmeg.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/HkXdRRMXtf0.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/JQgLhS9kjXo.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/MiGetfodaMs.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/bAoEgiZNwMM.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/cgARhCwXwgI.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/fOiy0oDO-kk.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/gKdI6LPo4Gk.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/gwxX7xFvYys.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/jq-lP-WFLkQ.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/lQGTKk5S4-o.jpg)
![alt text](https://github.com/t0efL/horse2zebras-GAN/blob/master/results/tseO0ZcEAro.jpg)

Dataset
-----------------------------------
As a dataset, I chose a dataset from the UC Berkeley website that was designed specifically for cycleGAN. It is downloaded directly to your laptop via [the following link](https://people.eecs.berkeley.edu/~taesung_park/CycleGAN/datasets/horse2zebra.zip).

The dataset is divided into 4 parts in advance (folders):
1. testA (120 Files)
2. testB (140 Files)
3. trainA (1,067 Files)
4. trainB (1,334 Files)

`A-files - horses, B-files - zebras.`

Weights
-----------------------------------
The weights were too large to directly add them to github, so I leave you links to download them. You will need to download them and, without changing the name, put them in the root of your Google drive, and the corresponding cell in the code will pass them to the necessary models. To implement Cycle GAN, you need 4 different models, so there will also be 4 weights.

Links:
* https://drive.google.com/file/d/1kaKwasQWc3iJVa5q1X1NQnuQzXrk9hf0/view?usp=sharing
* https://drive.google.com/file/d/19C7OMiPY_7YcoD8Z6Z2bgQfLvaDnsNZY/view?usp=sharing
* https://drive.google.com/file/d/1oMJE0FXpSSTybD0PA5PKsP4907klNTXD/view?usp=sharing
* https://drive.google.com/file/d/15TfxxtFaT4h-ebqdJerF78ekn5srIxuQ/view?usp=sharing

Training
-----------------------------------
All training parameters can be found in the laptop. I decided to do 200 epochs of training. If you suddenly decide to train this network yourself, keep in mind that for a full day on Google Colab Pro, approximately 150 epochs are performed. In this regard, I had to load weights several times and start with checkpoints. The code for loading weights is in the laptop. The training cycle also contains a block of code that saves weights to your Google drive every 5 epochs, specifying the era number in the name.

You can change the training parameters to get a better result. **n_cpu** (the number of cores in the processor) I have costs 2, because my processor only has two cores, you can put the number of cores of your processor. **Batchsize** I have is 6, this is the maximum size that fits on the GPU provided by Google Colab Pro. If you get an error, try reducing this parameter.

Other
-----------------------------------
All other comments and explanations are contained in the laptop itself. There is an illustration of the final results at the end of the notebook. You can also find two cells before the learning cycle cell that will help you convert your own image (preferably JPG).
