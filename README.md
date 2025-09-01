# Traffic_Sign_Detection

## Dataset Link: https://www.kaggle.com/datasets/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign

## Kaggle Notebook: https://www.kaggle.com/code/shasan038/traffic-sign-detection/

The images were transformed and normalized using torch, then we fed them to the **pretrained PVTv2-b0 model for fine-Tuning**

**The best validation accuracy achieved by our model is 99.94%**.

Training Summary:

    Epoch [1/10]  Train Loss: 0.2721 | Train Acc: 92.75%  || Val Loss: 0.0397 | Val Acc: 98.61%
    Saved new best model with val_acc: 98.61%
    Epoch [2/10]  Train Loss: 0.0421 | Train Acc: 98.90%  || Val Loss: 0.0136 | Val Acc: 99.72%
    Saved new best model with val_acc: 99.72%
    Epoch [3/10]  Train Loss: 0.0248 | Train Acc: 99.35%  || Val Loss: 0.0133 | Val Acc: 99.58%
    Epoch [4/10]  Train Loss: 0.0289 | Train Acc: 99.26%  || Val Loss: 0.0041 | Val Acc: 99.94%
    Saved new best model with val_acc: 99.94%
    Epoch [5/10]  Train Loss: 0.0132 | Train Acc: 99.65%  || Val Loss: 0.0254 | Val Acc: 99.36%
    Epoch [6/10]  Train Loss: 0.0207 | Train Acc: 99.43%  || Val Loss: 0.0172 | Val Acc: 99.53%
    Epoch [7/10]  Train Loss: 0.0140 | Train Acc: 99.59%  || Val Loss: 0.0429 | Val Acc: 99.00%
    Epoch [8/10]  Train Loss: 0.0172 | Train Acc: 99.57%  || Val Loss: 0.0151 | Val Acc: 99.58%
    Epoch [9/10]  Train Loss: 0.0133 | Train Acc: 99.70%  || Val Loss: 0.0168 | Val Acc: 99.53%
    Epoch [10/10]  Train Loss: 0.0121 | Train Acc: 99.74%  || Val Loss: 0.0404 | Val Acc: 99.03%


Obtained Results:

    Classification Report:

                  precision    recall  f1-score   support
    
               0       1.00      1.00      1.00        42
               1       1.00      1.00      1.00       100
              10       1.00      1.00      1.00       100
              11       1.00      1.00      1.00       100
              12       1.00      1.00      1.00       100
              13       1.00      1.00      1.00       100
              14       1.00      1.00      1.00       100
              15       1.00      1.00      1.00       100
              16       1.00      1.00      1.00        84
              17       1.00      1.00      1.00       100
              18       1.00      1.00      1.00       100
              19       1.00      1.00      1.00        42
               2       1.00      1.00      1.00       100
              20       1.00      1.00      1.00        72
              21       1.00      1.00      1.00        66
              22       1.00      1.00      1.00        78
              23       1.00      1.00      1.00       100
              24       1.00      1.00      1.00        54
              25       1.00      1.00      1.00       100
              26       1.00      1.00      1.00       100
              27       1.00      1.00      1.00        48
              28       1.00      1.00      1.00       100
              29       1.00      1.00      1.00        54
               3       1.00      1.00      1.00       100
              30       1.00      1.00      1.00        90
              31       1.00      1.00      1.00       100
              32       1.00      1.00      1.00        48
              33       1.00      1.00      1.00       100
              34       1.00      1.00      1.00        84
              35       1.00      0.99      0.99       100
              36       1.00      1.00      1.00        78
              37       0.98      1.00      0.99        42
              38       1.00      1.00      1.00       100
              39       1.00      1.00      1.00        60
               4       1.00      1.00      1.00       100
              40       1.00      1.00      1.00        72
              41       1.00      1.00      1.00        48
              42       1.00      1.00      1.00        48
               5       0.99      1.00      1.00       100
               6       1.00      1.00      1.00        84
               7       1.00      0.99      0.99       100
               8       1.00      1.00      1.00       100
               9       1.00      1.00      1.00       100
    
        accuracy                           1.00      3594
       macro avg       1.00      1.00      1.00      3594
    weighted avg       1.00      1.00      1.00      3594


![Confusion Matrix: ](Conf_Mat.png)

![Accuracy Curve: ](Acc.png)

![Loss_Curve): ](Loss.png)
