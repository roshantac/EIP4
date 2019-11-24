1. Logs

Train on 60000 samples, validate on 10000 samples
Epoch 1/20

Epoch 00001: LearningRateScheduler setting learning rate to 0.003.
60000/60000 [==============================] - 22s 368us/step - loss: 0.7585 - acc: 0.7532 - val_loss: 0.1305 - val_acc: 0.9762
Epoch 2/20

Epoch 00002: LearningRateScheduler setting learning rate to 0.0022744503.
60000/60000 [==============================] - 12s 194us/step - loss: 0.4123 - acc: 0.8522 - val_loss: 0.0762 - val_acc: 0.9838
Epoch 3/20

Epoch 00003: LearningRateScheduler setting learning rate to 0.0018315018.
60000/60000 [==============================] - 12s 192us/step - loss: 0.3425 - acc: 0.8694 - val_loss: 0.0607 - val_acc: 0.9847
Epoch 4/20

Epoch 00004: LearningRateScheduler setting learning rate to 0.0015329586.
60000/60000 [==============================] - 11s 189us/step - loss: 0.3069 - acc: 0.8778 - val_loss: 0.0556 - val_acc: 0.9861
Epoch 5/20

Epoch 00005: LearningRateScheduler setting learning rate to 0.0013181019.
60000/60000 [==============================] - 11s 189us/step - loss: 0.2892 - acc: 0.8790 - val_loss: 0.0393 - val_acc: 0.9891
Epoch 6/20

Epoch 00006: LearningRateScheduler setting learning rate to 0.0011560694.
60000/60000 [==============================] - 11s 189us/step - loss: 0.2740 - acc: 0.8806 - val_loss: 0.0365 - val_acc: 0.9901
Epoch 7/20

Epoch 00007: LearningRateScheduler setting learning rate to 0.0010295127.
60000/60000 [==============================] - 11s 190us/step - loss: 0.2661 - acc: 0.8823 - val_loss: 0.0289 - val_acc: 0.9918
Epoch 8/20

Epoch 00008: LearningRateScheduler setting learning rate to 0.0009279307.
60000/60000 [==============================] - 11s 191us/step - loss: 0.2578 - acc: 0.8831 - val_loss: 0.0261 - val_acc: 0.9929
Epoch 9/20

Epoch 00009: LearningRateScheduler setting learning rate to 0.0008445946.
60000/60000 [==============================] - 12s 192us/step - loss: 0.2538 - acc: 0.8839 - val_loss: 0.0255 - val_acc: 0.9932
Epoch 10/20

Epoch 00010: LearningRateScheduler setting learning rate to 0.0007749935.
60000/60000 [==============================] - 11s 188us/step - loss: 0.2491 - acc: 0.8843 - val_loss: 0.0231 - val_acc: 0.9928
Epoch 11/20

Epoch 00011: LearningRateScheduler setting learning rate to 0.0007159905.
60000/60000 [==============================] - 11s 189us/step - loss: 0.2433 - acc: 0.8862 - val_loss: 0.0246 - val_acc: 0.9925
Epoch 12/20

Epoch 00012: LearningRateScheduler setting learning rate to 0.000665336.
60000/60000 [==============================] - 12s 192us/step - loss: 0.2395 - acc: 0.8872 - val_loss: 0.0223 - val_acc: 0.9933
Epoch 13/20

Epoch 00013: LearningRateScheduler setting learning rate to 0.0006213753.
60000/60000 [==============================] - 11s 191us/step - loss: 0.2379 - acc: 0.8848 - val_loss: 0.0220 - val_acc: 0.9934
Epoch 14/20

Epoch 00014: LearningRateScheduler setting learning rate to 0.0005828638.
60000/60000 [==============================] - 11s 191us/step - loss: 0.2377 - acc: 0.8852 - val_loss: 0.0211 - val_acc: 0.9948
Epoch 15/20

Epoch 00015: LearningRateScheduler setting learning rate to 0.0005488474.
60000/60000 [==============================] - 11s 189us/step - loss: 0.2361 - acc: 0.8863 - val_loss: 0.0222 - val_acc: 0.9938
Epoch 16/20

Epoch 00016: LearningRateScheduler setting learning rate to 0.0005185825.
60000/60000 [==============================] - 11s 187us/step - loss: 0.2283 - acc: 0.8891 - val_loss: 0.0215 - val_acc: 0.9936
Epoch 17/20

Epoch 00017: LearningRateScheduler setting learning rate to 0.000491481.
60000/60000 [==============================] - 11s 188us/step - loss: 0.2278 - acc: 0.8896 - val_loss: 0.0199 - val_acc: 0.9938
Epoch 18/20

Epoch 00018: LearningRateScheduler setting learning rate to 0.0004670715.
60000/60000 [==============================] - 12s 206us/step - loss: 0.2253 - acc: 0.8876 - val_loss: 0.0188 - val_acc: 0.9947
Epoch 19/20

Epoch 00019: LearningRateScheduler setting learning rate to 0.0004449718.
60000/60000 [==============================] - 11s 191us/step - loss: 0.2271 - acc: 0.8873 - val_loss: 0.0196 - val_acc: 0.9947
Epoch 20/20

Epoch 00020: LearningRateScheduler setting learning rate to 0.000424869.
60000/60000 [==============================] - 11s 191us/step - loss: 0.2290 - acc: 0.8869 - val_loss: 0.0191 - val_acc: 0.9946

<keras.callbacks.History at 0x7f5df40c1710>





2. Model evaluation Score

[0.019124836034327745, 0.9946]

3. Stratergy 
i have changed the number of filters in the second convolutional from 32 to 16 inorder to reduce parameters. and the parameter become 14,060 which is less than 15k( the requirement).
changed the Dropout value from .1 to .19 which remove overfitting. 

