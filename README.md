# erfnet_colab

## Intro :

This code uses **ERFNet [[HERE]](https://github.com/Eromera/erfnet_pytorch)**. This is a merge of erfnet's code to run on Google Colab.
 
## Requirements :

[**The Cityscapes dataset**](https://www.cityscapes-dataset.com/): Download the "leftImg8bit" and "gtFine". You need to use **[conversor](https://github.com/mcordts/cityscapesScripts)** because for training you should use "_labelTrainIds". (To use the conversor you just set the gtFine file under the cityscapesScripts file and run the **createTrainIdLabelImgs.py**.)

## Dataset :

I used only 1 city each for train, val, test

## About the code :

Use the Google Colaboratory to run the code. **ERFNetTrain** is for training ERFNet. **ERFNetEval** is for evaluating the trained erfnet. You need to change savedir and datadir path in ArgumentParser to match your files. In the **ERFNetTrain**, the batch size must be under 6. If it is over 6, you might have error of 'CUDA out of memory'. In the **ERFNetEval**, change loadDir and loadWeights to run pretrained model or your trained model.
