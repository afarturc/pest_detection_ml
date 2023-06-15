## PRE-TRAINED WITH IMAGE NET

### RESNET 18

----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1         [-1, 64, 128, 128]           9,408
       BatchNorm2d-2         [-1, 64, 128, 128]             128
              ReLU-3         [-1, 64, 128, 128]               0
         MaxPool2d-4           [-1, 64, 64, 64]               0
            Conv2d-5           [-1, 64, 64, 64]          36,864
       BatchNorm2d-6           [-1, 64, 64, 64]             128
              ReLU-7           [-1, 64, 64, 64]               0
            Conv2d-8           [-1, 64, 64, 64]          36,864
       BatchNorm2d-9           [-1, 64, 64, 64]             128
             ReLU-10           [-1, 64, 64, 64]               0
       BasicBlock-11           [-1, 64, 64, 64]               0
           Conv2d-12           [-1, 64, 64, 64]          36,864
      BatchNorm2d-13           [-1, 64, 64, 64]             128
             ReLU-14           [-1, 64, 64, 64]               0
           Conv2d-15           [-1, 64, 64, 64]          36,864
      BatchNorm2d-16           [-1, 64, 64, 64]             128
             ReLU-17           [-1, 64, 64, 64]               0
       BasicBlock-18           [-1, 64, 64, 64]               0
           Conv2d-19          [-1, 128, 32, 32]          73,728
      BatchNorm2d-20          [-1, 128, 32, 32]             256
             ReLU-21          [-1, 128, 32, 32]               0
           Conv2d-22          [-1, 128, 32, 32]         147,456
      BatchNorm2d-23          [-1, 128, 32, 32]             256
           Conv2d-24          [-1, 128, 32, 32]           8,192
      BatchNorm2d-25          [-1, 128, 32, 32]             256
             ReLU-26          [-1, 128, 32, 32]               0
       BasicBlock-27          [-1, 128, 32, 32]               0
           Conv2d-28          [-1, 128, 32, 32]         147,456
      BatchNorm2d-29          [-1, 128, 32, 32]             256
             ReLU-30          [-1, 128, 32, 32]               0
           Conv2d-31          [-1, 128, 32, 32]         147,456
      BatchNorm2d-32          [-1, 128, 32, 32]             256
             ReLU-33          [-1, 128, 32, 32]               0
       BasicBlock-34          [-1, 128, 32, 32]               0
           Conv2d-35          [-1, 256, 16, 16]         294,912
      BatchNorm2d-36          [-1, 256, 16, 16]             512
             ReLU-37          [-1, 256, 16, 16]               0
           Conv2d-38          [-1, 256, 16, 16]         589,824
      BatchNorm2d-39          [-1, 256, 16, 16]             512
           Conv2d-40          [-1, 256, 16, 16]          32,768
      BatchNorm2d-41          [-1, 256, 16, 16]             512
             ReLU-42          [-1, 256, 16, 16]               0
       BasicBlock-43          [-1, 256, 16, 16]               0
           Conv2d-44          [-1, 256, 16, 16]         589,824
      BatchNorm2d-45          [-1, 256, 16, 16]             512
             ReLU-46          [-1, 256, 16, 16]               0
           Conv2d-47          [-1, 256, 16, 16]         589,824
      BatchNorm2d-48          [-1, 256, 16, 16]             512
             ReLU-49          [-1, 256, 16, 16]               0
       BasicBlock-50          [-1, 256, 16, 16]               0
           Conv2d-51            [-1, 512, 8, 8]       1,179,648
      BatchNorm2d-52            [-1, 512, 8, 8]           1,024
             ReLU-53            [-1, 512, 8, 8]               0
           Conv2d-54            [-1, 512, 8, 8]       2,359,296
      BatchNorm2d-55            [-1, 512, 8, 8]           1,024
           Conv2d-56            [-1, 512, 8, 8]         131,072
      BatchNorm2d-57            [-1, 512, 8, 8]           1,024
             ReLU-58            [-1, 512, 8, 8]               0
       BasicBlock-59            [-1, 512, 8, 8]               0
           Conv2d-60            [-1, 512, 8, 8]       2,359,296
      BatchNorm2d-61            [-1, 512, 8, 8]           1,024
             ReLU-62            [-1, 512, 8, 8]               0
           Conv2d-63            [-1, 512, 8, 8]       2,359,296
      BatchNorm2d-64            [-1, 512, 8, 8]           1,024
             ReLU-65            [-1, 512, 8, 8]               0
       BasicBlock-66            [-1, 512, 8, 8]               0
AdaptiveAvgPool2d-67            [-1, 512, 1, 1]               0
           Linear-68                   [-1, 38]          19,494
================================================================
Total params: 11,196,006
Trainable params: 19,494
Non-trainable params: 11,176,512
----------------------------------------------------------------
Input size (MB): 0.75
Forward/backward pass size (MB): 82.00
Params size (MB): 42.71
Estimated Total Size (MB): 125.46
----------------------------------------------------------------
None

Epoch [0], last_lr: 0.00812, train_loss: 0.6971, val_loss: 0.3277, val_acc: 0.9219
Epoch [1], last_lr: 0.00000, train_loss: 0.2106, val_loss: 0.1286, val_acc: 0.9623
CPU times: user 1min 59s, sys: 2min 13s, total: 4min 12s
Wall time: 3min 19s

![Accuracy History](./images/pt_imagenet/18_acc.png)

![Loss History](./images/pt_imagenet/18_lr.png)

![LR History](./images/pt_imagenet/18_loss.png)

Classification Report: 

                                                    precision    recall  f1-score   support

                                Apple___Apple_scab       0.97      0.95      0.96       504
                                 Apple___Black_rot       0.97      0.99      0.98       497
                          Apple___Cedar_apple_rust       0.98      0.98      0.98       440
                                   Apple___healthy       0.98      0.97      0.98       502
                               Blueberry___healthy       0.97      1.00      0.98       454
          Cherry_(including_sour)___Powdery_mildew       0.98      1.00      0.99       421
                 Cherry_(including_sour)___healthy       0.99      1.00      0.99       456
Corn_(maize)___Cercospora_leaf_spot Gray_leaf_spot       0.94      0.90      0.92       410
                       Corn_(maize)___Common_rust_       1.00      0.99      0.99       477
               Corn_(maize)___Northern_Leaf_Blight       0.92      0.94      0.93       477
                            Corn_(maize)___healthy       0.99      1.00      1.00       465
                                 Grape___Black_rot       0.97      0.98      0.98       472
                      Grape___Esca_(Black_Measles)       0.98      0.98      0.98       480
        Grape___Leaf_blight_(Isariopsis_Leaf_Spot)       1.00      0.99      1.00       430
                                   Grape___healthy       1.00      0.99      0.99       423
          Orange___Haunglongbing_(Citrus_greening)       0.99      1.00      1.00       503
                            Peach___Bacterial_spot       0.97      0.97      0.97       459
                                   Peach___healthy       0.99      0.99      0.99       432
                     Pepper,_bell___Bacterial_spot       0.96      0.98      0.97       478
                            Pepper,_bell___healthy       0.96      0.98      0.97       497
                             Potato___Early_blight       0.99      0.97      0.98       485
                              Potato___Late_blight       0.93      0.95      0.94       485
                                  Potato___healthy       0.97      0.97      0.97       456
                               Raspberry___healthy       0.99      1.00      0.99       445
                                 Soybean___healthy       0.98      0.99      0.98       505
                           Squash___Powdery_mildew       1.00      1.00      1.00       434
                          Strawberry___Leaf_scorch       0.99      1.00      0.99       444
                              Strawberry___healthy       0.99      1.00      0.99       456
                           Tomato___Bacterial_spot       0.95      0.96      0.95       425
                             Tomato___Early_blight       0.89      0.81      0.85       480
                              Tomato___Late_blight       0.88      0.90      0.89       463
                                Tomato___Leaf_Mold       0.93      0.93      0.93       470
                       Tomato___Septoria_leaf_spot       0.94      0.84      0.89       436
     Tomato___Spider_mites Two-spotted_spider_mite       0.88      0.92      0.90       435
                              Tomato___Target_Spot       0.85      0.86      0.85       457
            Tomato___Tomato_Yellow_Leaf_Curl_Virus       0.95      0.98      0.96       490
                      Tomato___Tomato_mosaic_virus       0.98      0.95      0.96       448
                                  Tomato___healthy       0.96      0.96      0.96       481

                                          accuracy                           0.96     17572
                                         macro avg       0.96      0.96      0.96     17572
                                      weighted avg       0.96      0.96      0.96     17572

Balanced accuracy score: 
0.962035797815418

![Heatmap](./images/pt_imagenet//18_heatmap.png)

### RESNET 34

----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1         [-1, 64, 128, 128]           9,408
       BatchNorm2d-2         [-1, 64, 128, 128]             128
              ReLU-3         [-1, 64, 128, 128]               0
         MaxPool2d-4           [-1, 64, 64, 64]               0
            Conv2d-5           [-1, 64, 64, 64]          36,864
       BatchNorm2d-6           [-1, 64, 64, 64]             128
              ReLU-7           [-1, 64, 64, 64]               0
            Conv2d-8           [-1, 64, 64, 64]          36,864
       BatchNorm2d-9           [-1, 64, 64, 64]             128
             ReLU-10           [-1, 64, 64, 64]               0
       BasicBlock-11           [-1, 64, 64, 64]               0
           Conv2d-12           [-1, 64, 64, 64]          36,864
      BatchNorm2d-13           [-1, 64, 64, 64]             128
             ReLU-14           [-1, 64, 64, 64]               0
           Conv2d-15           [-1, 64, 64, 64]          36,864
      BatchNorm2d-16           [-1, 64, 64, 64]             128
             ReLU-17           [-1, 64, 64, 64]               0
       BasicBlock-18           [-1, 64, 64, 64]               0
           Conv2d-19           [-1, 64, 64, 64]          36,864
      BatchNorm2d-20           [-1, 64, 64, 64]             128
             ReLU-21           [-1, 64, 64, 64]               0
           Conv2d-22           [-1, 64, 64, 64]          36,864
      BatchNorm2d-23           [-1, 64, 64, 64]             128
             ReLU-24           [-1, 64, 64, 64]               0
       BasicBlock-25           [-1, 64, 64, 64]               0
           Conv2d-26          [-1, 128, 32, 32]          73,728
      BatchNorm2d-27          [-1, 128, 32, 32]             256
             ReLU-28          [-1, 128, 32, 32]               0
           Conv2d-29          [-1, 128, 32, 32]         147,456
      BatchNorm2d-30          [-1, 128, 32, 32]             256
           Conv2d-31          [-1, 128, 32, 32]           8,192
      BatchNorm2d-32          [-1, 128, 32, 32]             256
             ReLU-33          [-1, 128, 32, 32]               0
       BasicBlock-34          [-1, 128, 32, 32]               0
           Conv2d-35          [-1, 128, 32, 32]         147,456
      BatchNorm2d-36          [-1, 128, 32, 32]             256
             ReLU-37          [-1, 128, 32, 32]               0
           Conv2d-38          [-1, 128, 32, 32]         147,456
      BatchNorm2d-39          [-1, 128, 32, 32]             256
             ReLU-40          [-1, 128, 32, 32]               0
       BasicBlock-41          [-1, 128, 32, 32]               0
           Conv2d-42          [-1, 128, 32, 32]         147,456
      BatchNorm2d-43          [-1, 128, 32, 32]             256
             ReLU-44          [-1, 128, 32, 32]               0
           Conv2d-45          [-1, 128, 32, 32]         147,456
      BatchNorm2d-46          [-1, 128, 32, 32]             256
             ReLU-47          [-1, 128, 32, 32]               0
       BasicBlock-48          [-1, 128, 32, 32]               0
           Conv2d-49          [-1, 128, 32, 32]         147,456
      BatchNorm2d-50          [-1, 128, 32, 32]             256
             ReLU-51          [-1, 128, 32, 32]               0
           Conv2d-52          [-1, 128, 32, 32]         147,456
      BatchNorm2d-53          [-1, 128, 32, 32]             256
             ReLU-54          [-1, 128, 32, 32]               0
       BasicBlock-55          [-1, 128, 32, 32]               0
           Conv2d-56          [-1, 256, 16, 16]         294,912
      BatchNorm2d-57          [-1, 256, 16, 16]             512
             ReLU-58          [-1, 256, 16, 16]               0
           Conv2d-59          [-1, 256, 16, 16]         589,824
      BatchNorm2d-60          [-1, 256, 16, 16]             512
           Conv2d-61          [-1, 256, 16, 16]          32,768
      BatchNorm2d-62          [-1, 256, 16, 16]             512
             ReLU-63          [-1, 256, 16, 16]               0
       BasicBlock-64          [-1, 256, 16, 16]               0
           Conv2d-65          [-1, 256, 16, 16]         589,824
      BatchNorm2d-66          [-1, 256, 16, 16]             512
             ReLU-67          [-1, 256, 16, 16]               0
           Conv2d-68          [-1, 256, 16, 16]         589,824
      BatchNorm2d-69          [-1, 256, 16, 16]             512
             ReLU-70          [-1, 256, 16, 16]               0
       BasicBlock-71          [-1, 256, 16, 16]               0
           Conv2d-72          [-1, 256, 16, 16]         589,824
      BatchNorm2d-73          [-1, 256, 16, 16]             512
             ReLU-74          [-1, 256, 16, 16]               0
           Conv2d-75          [-1, 256, 16, 16]         589,824
      BatchNorm2d-76          [-1, 256, 16, 16]             512
             ReLU-77          [-1, 256, 16, 16]               0
       BasicBlock-78          [-1, 256, 16, 16]               0
           Conv2d-79          [-1, 256, 16, 16]         589,824
      BatchNorm2d-80          [-1, 256, 16, 16]             512
             ReLU-81          [-1, 256, 16, 16]               0
           Conv2d-82          [-1, 256, 16, 16]         589,824
      BatchNorm2d-83          [-1, 256, 16, 16]             512
             ReLU-84          [-1, 256, 16, 16]               0
       BasicBlock-85          [-1, 256, 16, 16]               0
           Conv2d-86          [-1, 256, 16, 16]         589,824
      BatchNorm2d-87          [-1, 256, 16, 16]             512
             ReLU-88          [-1, 256, 16, 16]               0
           Conv2d-89          [-1, 256, 16, 16]         589,824
      BatchNorm2d-90          [-1, 256, 16, 16]             512
             ReLU-91          [-1, 256, 16, 16]               0
       BasicBlock-92          [-1, 256, 16, 16]               0
           Conv2d-93          [-1, 256, 16, 16]         589,824
      BatchNorm2d-94          [-1, 256, 16, 16]             512
             ReLU-95          [-1, 256, 16, 16]               0
           Conv2d-96          [-1, 256, 16, 16]         589,824
      BatchNorm2d-97          [-1, 256, 16, 16]             512
             ReLU-98          [-1, 256, 16, 16]               0
       BasicBlock-99          [-1, 256, 16, 16]               0
          Conv2d-100            [-1, 512, 8, 8]       1,179,648
     BatchNorm2d-101            [-1, 512, 8, 8]           1,024
            ReLU-102            [-1, 512, 8, 8]               0
          Conv2d-103            [-1, 512, 8, 8]       2,359,296
     BatchNorm2d-104            [-1, 512, 8, 8]           1,024
          Conv2d-105            [-1, 512, 8, 8]         131,072
     BatchNorm2d-106            [-1, 512, 8, 8]           1,024
            ReLU-107            [-1, 512, 8, 8]               0
      BasicBlock-108            [-1, 512, 8, 8]               0
          Conv2d-109            [-1, 512, 8, 8]       2,359,296
     BatchNorm2d-110            [-1, 512, 8, 8]           1,024
            ReLU-111            [-1, 512, 8, 8]               0
          Conv2d-112            [-1, 512, 8, 8]       2,359,296
     BatchNorm2d-113            [-1, 512, 8, 8]           1,024
            ReLU-114            [-1, 512, 8, 8]               0
      BasicBlock-115            [-1, 512, 8, 8]               0
          Conv2d-116            [-1, 512, 8, 8]       2,359,296
     BatchNorm2d-117            [-1, 512, 8, 8]           1,024
            ReLU-118            [-1, 512, 8, 8]               0
          Conv2d-119            [-1, 512, 8, 8]       2,359,296
     BatchNorm2d-120            [-1, 512, 8, 8]           1,024
            ReLU-121            [-1, 512, 8, 8]               0
      BasicBlock-122            [-1, 512, 8, 8]               0
AdaptiveAvgPool2d-123            [-1, 512, 1, 1]               0
          Linear-124                   [-1, 38]          19,494
================================================================
Total params: 21,304,166
Trainable params: 19,494
Non-trainable params: 21,284,672
----------------------------------------------------------------
Input size (MB): 0.75
Forward/backward pass size (MB): 125.75
Params size (MB): 81.27
Estimated Total Size (MB): 207.77
----------------------------------------------------------------

Epoch [0], last_lr: 0.00812, train_loss: 0.7205, val_loss: 0.4138, val_acc: 0.9009
Epoch [1], last_lr: 0.00000, train_loss: 0.2279, val_loss: 0.1445, val_acc: 0.9576
CPU times: user 2min 51s, sys: 3min 39s, total: 6min 31s
Wall time: 5min 39s

![Accuracy History](./images/pt_imagenet/34_acc.png)

![Loss History](./images/pt_imagenet/34_loss.png)

![LR History](./images/pt_imagenet/34_lr.png)

Classification Report: 

                                                    precision    recall  f1-score   support

                                Apple___Apple_scab       0.97      0.94      0.96       504
                                 Apple___Black_rot       0.98      0.99      0.99       497
                          Apple___Cedar_apple_rust       0.96      0.97      0.97       440
                                   Apple___healthy       0.96      1.00      0.98       502
                               Blueberry___healthy       0.95      0.99      0.97       454
          Cherry_(including_sour)___Powdery_mildew       0.99      0.99      0.99       421
                 Cherry_(including_sour)___healthy       0.99      0.99      0.99       456
Corn_(maize)___Cercospora_leaf_spot Gray_leaf_spot       0.95      0.91      0.93       410
                       Corn_(maize)___Common_rust_       1.00      0.99      1.00       477
               Corn_(maize)___Northern_Leaf_Blight       0.92      0.96      0.94       477
                            Corn_(maize)___healthy       1.00      1.00      1.00       465
                                 Grape___Black_rot       0.95      0.97      0.96       472
                      Grape___Esca_(Black_Measles)       0.96      0.96      0.96       480
        Grape___Leaf_blight_(Isariopsis_Leaf_Spot)       0.99      1.00      0.99       430
                                   Grape___healthy       1.00      0.99      0.99       423
          Orange___Haunglongbing_(Citrus_greening)       0.99      1.00      1.00       503
                            Peach___Bacterial_spot       0.98      0.97      0.98       459
                                   Peach___healthy       0.98      0.99      0.99       432
                     Pepper,_bell___Bacterial_spot       0.97      0.98      0.98       478
                            Pepper,_bell___healthy       0.97      0.96      0.96       497
                             Potato___Early_blight       0.99      0.99      0.99       485
                              Potato___Late_blight       0.96      0.96      0.96       485
                                  Potato___healthy       0.93      0.95      0.94       456
                               Raspberry___healthy       0.99      0.98      0.99       445
                                 Soybean___healthy       0.99      0.97      0.98       505
                           Squash___Powdery_mildew       1.00      1.00      1.00       434
                          Strawberry___Leaf_scorch       0.98      0.99      0.99       444
                              Strawberry___healthy       0.99      1.00      1.00       456
                           Tomato___Bacterial_spot       0.91      0.96      0.94       425
                             Tomato___Early_blight       0.88      0.78      0.83       480
                              Tomato___Late_blight       0.87      0.88      0.87       463
                                Tomato___Leaf_Mold       0.92      0.93      0.92       470
                       Tomato___Septoria_leaf_spot       0.87      0.87      0.87       436
     Tomato___Spider_mites Two-spotted_spider_mite       0.91      0.90      0.91       435
                              Tomato___Target_Spot       0.88      0.81      0.84       457
            Tomato___Tomato_Yellow_Leaf_Curl_Virus       0.96      0.97      0.97       490
                      Tomato___Tomato_mosaic_virus       0.93      0.94      0.94       448
                                  Tomato___healthy       0.95      0.97      0.96       481

                                          accuracy                           0.96     17572
                                         macro avg       0.96      0.96      0.96     17572
                                      weighted avg       0.96      0.96      0.96     17572

Balanced accuracy score: 
0.9573455178425663

![Heatmap](./images/pt_imagenet/34_heatmap.png)

## PRE-TRAINED WITH PLANT DATASET

### RESNET 34

----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1         [-1, 64, 128, 128]           9,408
       BatchNorm2d-2         [-1, 64, 128, 128]             128
              ReLU-3         [-1, 64, 128, 128]               0
         MaxPool2d-4           [-1, 64, 64, 64]               0
            Conv2d-5           [-1, 64, 64, 64]          36,864
       BatchNorm2d-6           [-1, 64, 64, 64]             128
              ReLU-7           [-1, 64, 64, 64]               0
            Conv2d-8           [-1, 64, 64, 64]          36,864
       BatchNorm2d-9           [-1, 64, 64, 64]             128
             ReLU-10           [-1, 64, 64, 64]               0
       BasicBlock-11           [-1, 64, 64, 64]               0
           Conv2d-12           [-1, 64, 64, 64]          36,864
      BatchNorm2d-13           [-1, 64, 64, 64]             128
             ReLU-14           [-1, 64, 64, 64]               0
           Conv2d-15           [-1, 64, 64, 64]          36,864
      BatchNorm2d-16           [-1, 64, 64, 64]             128
             ReLU-17           [-1, 64, 64, 64]               0
       BasicBlock-18           [-1, 64, 64, 64]               0
           Conv2d-19           [-1, 64, 64, 64]          36,864
      BatchNorm2d-20           [-1, 64, 64, 64]             128
             ReLU-21           [-1, 64, 64, 64]               0
           Conv2d-22           [-1, 64, 64, 64]          36,864
      BatchNorm2d-23           [-1, 64, 64, 64]             128
             ReLU-24           [-1, 64, 64, 64]               0
       BasicBlock-25           [-1, 64, 64, 64]               0
           Conv2d-26          [-1, 128, 32, 32]          73,728
      BatchNorm2d-27          [-1, 128, 32, 32]             256
             ReLU-28          [-1, 128, 32, 32]               0
           Conv2d-29          [-1, 128, 32, 32]         147,456
      BatchNorm2d-30          [-1, 128, 32, 32]             256
           Conv2d-31          [-1, 128, 32, 32]           8,192
      BatchNorm2d-32          [-1, 128, 32, 32]             256
             ReLU-33          [-1, 128, 32, 32]               0
       BasicBlock-34          [-1, 128, 32, 32]               0
           Conv2d-35          [-1, 128, 32, 32]         147,456
      BatchNorm2d-36          [-1, 128, 32, 32]             256
             ReLU-37          [-1, 128, 32, 32]               0
           Conv2d-38          [-1, 128, 32, 32]         147,456
      BatchNorm2d-39          [-1, 128, 32, 32]             256
             ReLU-40          [-1, 128, 32, 32]               0
       BasicBlock-41          [-1, 128, 32, 32]               0
           Conv2d-42          [-1, 128, 32, 32]         147,456
      BatchNorm2d-43          [-1, 128, 32, 32]             256
             ReLU-44          [-1, 128, 32, 32]               0
           Conv2d-45          [-1, 128, 32, 32]         147,456
      BatchNorm2d-46          [-1, 128, 32, 32]             256
             ReLU-47          [-1, 128, 32, 32]               0
       BasicBlock-48          [-1, 128, 32, 32]               0
           Conv2d-49          [-1, 128, 32, 32]         147,456
      BatchNorm2d-50          [-1, 128, 32, 32]             256
             ReLU-51          [-1, 128, 32, 32]               0
           Conv2d-52          [-1, 128, 32, 32]         147,456
      BatchNorm2d-53          [-1, 128, 32, 32]             256
             ReLU-54          [-1, 128, 32, 32]               0
       BasicBlock-55          [-1, 128, 32, 32]               0
           Conv2d-56          [-1, 256, 16, 16]         294,912
      BatchNorm2d-57          [-1, 256, 16, 16]             512
             ReLU-58          [-1, 256, 16, 16]               0
           Conv2d-59          [-1, 256, 16, 16]         589,824
      BatchNorm2d-60          [-1, 256, 16, 16]             512
           Conv2d-61          [-1, 256, 16, 16]          32,768
      BatchNorm2d-62          [-1, 256, 16, 16]             512
             ReLU-63          [-1, 256, 16, 16]               0
       BasicBlock-64          [-1, 256, 16, 16]               0
           Conv2d-65          [-1, 256, 16, 16]         589,824
      BatchNorm2d-66          [-1, 256, 16, 16]             512
             ReLU-67          [-1, 256, 16, 16]               0
           Conv2d-68          [-1, 256, 16, 16]         589,824
      BatchNorm2d-69          [-1, 256, 16, 16]             512
             ReLU-70          [-1, 256, 16, 16]               0
       BasicBlock-71          [-1, 256, 16, 16]               0
           Conv2d-72          [-1, 256, 16, 16]         589,824
      BatchNorm2d-73          [-1, 256, 16, 16]             512
             ReLU-74          [-1, 256, 16, 16]               0
           Conv2d-75          [-1, 256, 16, 16]         589,824
      BatchNorm2d-76          [-1, 256, 16, 16]             512
             ReLU-77          [-1, 256, 16, 16]               0
       BasicBlock-78          [-1, 256, 16, 16]               0
           Conv2d-79          [-1, 256, 16, 16]         589,824
      BatchNorm2d-80          [-1, 256, 16, 16]             512
             ReLU-81          [-1, 256, 16, 16]               0
           Conv2d-82          [-1, 256, 16, 16]         589,824
      BatchNorm2d-83          [-1, 256, 16, 16]             512
             ReLU-84          [-1, 256, 16, 16]               0
       BasicBlock-85          [-1, 256, 16, 16]               0
           Conv2d-86          [-1, 256, 16, 16]         589,824
      BatchNorm2d-87          [-1, 256, 16, 16]             512
             ReLU-88          [-1, 256, 16, 16]               0
           Conv2d-89          [-1, 256, 16, 16]         589,824
      BatchNorm2d-90          [-1, 256, 16, 16]             512
             ReLU-91          [-1, 256, 16, 16]               0
       BasicBlock-92          [-1, 256, 16, 16]               0
           Conv2d-93          [-1, 256, 16, 16]         589,824
      BatchNorm2d-94          [-1, 256, 16, 16]             512
             ReLU-95          [-1, 256, 16, 16]               0
           Conv2d-96          [-1, 256, 16, 16]         589,824
      BatchNorm2d-97          [-1, 256, 16, 16]             512
             ReLU-98          [-1, 256, 16, 16]               0
       BasicBlock-99          [-1, 256, 16, 16]               0
          Conv2d-100            [-1, 512, 8, 8]       1,179,648
     BatchNorm2d-101            [-1, 512, 8, 8]           1,024
            ReLU-102            [-1, 512, 8, 8]               0
          Conv2d-103            [-1, 512, 8, 8]       2,359,296
     BatchNorm2d-104            [-1, 512, 8, 8]           1,024
          Conv2d-105            [-1, 512, 8, 8]         131,072
     BatchNorm2d-106            [-1, 512, 8, 8]           1,024
            ReLU-107            [-1, 512, 8, 8]               0
      BasicBlock-108            [-1, 512, 8, 8]               0
          Conv2d-109            [-1, 512, 8, 8]       2,359,296
     BatchNorm2d-110            [-1, 512, 8, 8]           1,024
            ReLU-111            [-1, 512, 8, 8]               0
          Conv2d-112            [-1, 512, 8, 8]       2,359,296
     BatchNorm2d-113            [-1, 512, 8, 8]           1,024
            ReLU-114            [-1, 512, 8, 8]               0
      BasicBlock-115            [-1, 512, 8, 8]               0
          Conv2d-116            [-1, 512, 8, 8]       2,359,296
     BatchNorm2d-117            [-1, 512, 8, 8]           1,024
            ReLU-118            [-1, 512, 8, 8]               0
          Conv2d-119            [-1, 512, 8, 8]       2,359,296
     BatchNorm2d-120            [-1, 512, 8, 8]           1,024
            ReLU-121            [-1, 512, 8, 8]               0
      BasicBlock-122            [-1, 512, 8, 8]               0
AdaptiveAvgPool2d-123            [-1, 512, 1, 1]               0
          Linear-124                   [-1, 38]          19,494
================================================================
Total params: 21,304,166
Trainable params: 19,494
Non-trainable params: 21,284,672
----------------------------------------------------------------
Input size (MB): 0.75
Forward/backward pass size (MB): 125.75
Params size (MB): 81.27
Estimated Total Size (MB): 207.77
----------------------------------------------------------------


Epoch [0], last_lr: 0.00812, train_loss: 0.7205, val_loss: 0.4138, val_acc: 0.9009
Epoch [1], last_lr: 0.00000, train_loss: 0.2279, val_loss: 0.1445, val_acc: 0.9576
CPU times: user 3min, sys: 3min 38s, total: 6min 38s
Wall time: 5min 41s

![Accuracy History](./images/pt_plant/34_acc.png)

![Loss History](./images/pt_plant/34_loss.png)

![LR History](./images/pt_plant/34_lr.png)

Classification Report: 

                                                    precision    recall  f1-score   support

                                Apple___Apple_scab       0.97      0.94      0.96       504
                                 Apple___Black_rot       0.98      0.99      0.99       497
                          Apple___Cedar_apple_rust       0.96      0.97      0.97       440
                                   Apple___healthy       0.96      1.00      0.98       502
                               Blueberry___healthy       0.95      0.99      0.97       454
          Cherry_(including_sour)___Powdery_mildew       0.99      0.99      0.99       421
                 Cherry_(including_sour)___healthy       0.99      0.99      0.99       456
Corn_(maize)___Cercospora_leaf_spot Gray_leaf_spot       0.95      0.91      0.93       410
                       Corn_(maize)___Common_rust_       1.00      0.99      1.00       477
               Corn_(maize)___Northern_Leaf_Blight       0.92      0.96      0.94       477
                            Corn_(maize)___healthy       1.00      1.00      1.00       465
                                 Grape___Black_rot       0.95      0.97      0.96       472
                      Grape___Esca_(Black_Measles)       0.96      0.96      0.96       480
        Grape___Leaf_blight_(Isariopsis_Leaf_Spot)       0.99      1.00      0.99       430
                                   Grape___healthy       1.00      0.99      0.99       423
          Orange___Haunglongbing_(Citrus_greening)       0.99      1.00      1.00       503
                            Peach___Bacterial_spot       0.98      0.97      0.98       459
                                   Peach___healthy       0.98      0.99      0.99       432
                     Pepper,_bell___Bacterial_spot       0.97      0.98      0.98       478
                            Pepper,_bell___healthy       0.97      0.96      0.96       497
                             Potato___Early_blight       0.99      0.99      0.99       485
                              Potato___Late_blight       0.96      0.96      0.96       485
                                  Potato___healthy       0.93      0.95      0.94       456
                               Raspberry___healthy       0.99      0.98      0.99       445
                                 Soybean___healthy       0.99      0.97      0.98       505
                           Squash___Powdery_mildew       1.00      1.00      1.00       434
                          Strawberry___Leaf_scorch       0.98      0.99      0.99       444
                              Strawberry___healthy       0.99      1.00      1.00       456
                           Tomato___Bacterial_spot       0.91      0.96      0.94       425
                             Tomato___Early_blight       0.88      0.78      0.83       480
                              Tomato___Late_blight       0.87      0.88      0.87       463
                                Tomato___Leaf_Mold       0.92      0.93      0.92       470
                       Tomato___Septoria_leaf_spot       0.87      0.87      0.87       436
     Tomato___Spider_mites Two-spotted_spider_mite       0.91      0.90      0.91       435
                              Tomato___Target_Spot       0.88      0.81      0.84       457
            Tomato___Tomato_Yellow_Leaf_Curl_Virus       0.96      0.97      0.97       490
                      Tomato___Tomato_mosaic_virus       0.93      0.94      0.94       448
                                  Tomato___healthy       0.95      0.97      0.96       481

                                          accuracy                           0.96     17572
                                         macro avg       0.96      0.96      0.96     17572
                                      weighted avg       0.96      0.96      0.96     17572

Balanced accuracy score: 
0.9573455178425663

![Heatmap](./images/pt_plant/34_heatmap.png)


## CUSTOM

### RESNET 9 
