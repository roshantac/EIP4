Both the training are did in different notebook files.

final validation accuracy of base network : 82.68
Highest Accuracy on test data is: 82.15

Model

# Define the model
model = Sequential()
model.add(SeparableConv2D(48, (3,3), depth_multiplier=1, activation='relu',input_shape=(32, 32, 3))) 
model.add(BatchNormalization())
model.add(Dropout(0.20))

model.add(SeparableConv2D(64, (3,3), depth_multiplier=1, activation='relu')) #30x30
model.add(BatchNormalization())
model.add(Dropout(0.20))

model.add(SeparableConv2D(96, (3,3), depth_multiplier=1, activation='relu')) #28x28
model.add(MaxPooling2D(pool_size=(2, 2)))
model.add(BatchNormalization())
model.add(Dropout(0.20))

model.add(SeparableConv2D(128, (3,3), depth_multiplier=1, activation='relu')) #13x13
model.add(BatchNormalization())
model.add(Dropout(0.20))


model.add(SeparableConv2D(186, (3,3), depth_multiplier=1, activation='relu')) #11x11
model.add(BatchNormalization())
model.add(MaxPooling2D(pool_size=(2, 2)))
model.add(Dropout(0.20))


model.add(SeparableConv2D(232, (3,3), depth_multiplier=1, activation='relu')) #4x4
model.add(BatchNormalization())
model.add(MaxPooling2D(pool_size=(2, 2)))
model.add(Dropout(0.20))

model.add(SeparableConv2D(10, 1, depth_multiplier=1, activation='relu'))

model.add(Flatten())
model.add(Activation('softmax'))

model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])



=========================================================================================================================================================================

LOG
=========================================================================================================================================================================
Epoch 1/50
390/390 [==============================] - 50s 128ms/step - loss: 1.5843 - acc: 0.4320 - val_loss: 1.4572 - val_acc: 0.4815
Epoch 2/50
390/390 [==============================] - 42s 109ms/step - loss: 1.1908 - acc: 0.5801 - val_loss: 1.1180 - val_acc: 0.6083
Epoch 3/50
390/390 [==============================] - 42s 108ms/step - loss: 1.0597 - acc: 0.6248 - val_loss: 0.9947 - val_acc: 0.6457
Epoch 4/50
390/390 [==============================] - 42s 108ms/step - loss: 0.9751 - acc: 0.6572 - val_loss: 0.9274 - val_acc: 0.6763
Epoch 5/50
390/390 [==============================] - 42s 107ms/step - loss: 0.9127 - acc: 0.6792 - val_loss: 0.8512 - val_acc: 0.7017
Epoch 6/50
390/390 [==============================] - 42s 108ms/step - loss: 0.8592 - acc: 0.6983 - val_loss: 0.8078 - val_acc: 0.7169
Epoch 7/50
390/390 [==============================] - 42s 108ms/step - loss: 0.8228 - acc: 0.7121 - val_loss: 0.7578 - val_acc: 0.7381
Epoch 8/50
390/390 [==============================] - 42s 108ms/step - loss: 0.7914 - acc: 0.7237 - val_loss: 0.7477 - val_acc: 0.7375
Epoch 9/50
390/390 [==============================] - 42s 108ms/step - loss: 0.7701 - acc: 0.7296 - val_loss: 0.7342 - val_acc: 0.7446
Epoch 10/50
390/390 [==============================] - 42s 108ms/step - loss: 0.7417 - acc: 0.7401 - val_loss: 0.7457 - val_acc: 0.7391
Epoch 11/50
390/390 [==============================] - 42s 109ms/step - loss: 0.7263 - acc: 0.7448 - val_loss: 0.6920 - val_acc: 0.7575
Epoch 12/50
390/390 [==============================] - 43s 111ms/step - loss: 0.7009 - acc: 0.7567 - val_loss: 0.7155 - val_acc: 0.7479
Epoch 13/50
390/390 [==============================] - 42s 108ms/step - loss: 0.6897 - acc: 0.7603 - val_loss: 0.6745 - val_acc: 0.7654
Epoch 14/50
390/390 [==============================] - 42s 108ms/step - loss: 0.6799 - acc: 0.7622 - val_loss: 0.6916 - val_acc: 0.7610
Epoch 15/50
390/390 [==============================] - 42s 108ms/step - loss: 0.6620 - acc: 0.7690 - val_loss: 0.6318 - val_acc: 0.7789
Epoch 16/50
390/390 [==============================] - 42s 107ms/step - loss: 0.6504 - acc: 0.7727 - val_loss: 0.6480 - val_acc: 0.7743
Epoch 17/50
390/390 [==============================] - 42s 108ms/step - loss: 0.6464 - acc: 0.7730 - val_loss: 0.6433 - val_acc: 0.7746
Epoch 18/50
390/390 [==============================] - 42s 108ms/step - loss: 0.6332 - acc: 0.7761 - val_loss: 0.6409 - val_acc: 0.7774
Epoch 19/50
390/390 [==============================] - 42s 108ms/step - loss: 0.6201 - acc: 0.7816 - val_loss: 0.6134 - val_acc: 0.7881
Epoch 20/50
390/390 [==============================] - 42s 108ms/step - loss: 0.6117 - acc: 0.7852 - val_loss: 0.7294 - val_acc: 0.7457
Epoch 21/50
390/390 [==============================] - 42s 109ms/step - loss: 0.6030 - acc: 0.7880 - val_loss: 0.5915 - val_acc: 0.7952
Epoch 22/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5969 - acc: 0.7919 - val_loss: 0.5923 - val_acc: 0.7932
Epoch 23/50
390/390 [==============================] - 42s 107ms/step - loss: 0.5916 - acc: 0.7920 - val_loss: 0.6029 - val_acc: 0.7901
Epoch 24/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5836 - acc: 0.7954 - val_loss: 0.6098 - val_acc: 0.7916
Epoch 25/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5759 - acc: 0.7972 - val_loss: 0.5839 - val_acc: 0.7967
Epoch 26/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5725 - acc: 0.7982 - val_loss: 0.5698 - val_acc: 0.8004
Epoch 27/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5644 - acc: 0.8005 - val_loss: 0.5764 - val_acc: 0.8040
Epoch 28/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5622 - acc: 0.8024 - val_loss: 0.5794 - val_acc: 0.8001
Epoch 29/50
390/390 [==============================] - 42s 109ms/step - loss: 0.5522 - acc: 0.8054 - val_loss: 0.6210 - val_acc: 0.7832
Epoch 30/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5472 - acc: 0.8083 - val_loss: 0.5652 - val_acc: 0.8065
Epoch 31/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5435 - acc: 0.8102 - val_loss: 0.5681 - val_acc: 0.8020
Epoch 32/50
390/390 [==============================] - 42s 107ms/step - loss: 0.5371 - acc: 0.8119 - val_loss: 0.5523 - val_acc: 0.8094
Epoch 33/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5355 - acc: 0.8107 - val_loss: 0.5670 - val_acc: 0.8077
Epoch 34/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5302 - acc: 0.8146 - val_loss: 0.5464 - val_acc: 0.8139
Epoch 35/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5293 - acc: 0.8128 - val_loss: 0.5703 - val_acc: 0.8066
Epoch 36/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5199 - acc: 0.8172 - val_loss: 0.5546 - val_acc: 0.8135
Epoch 37/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5211 - acc: 0.8165 - val_loss: 0.5517 - val_acc: 0.8126
Epoch 38/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5098 - acc: 0.8197 - val_loss: 0.5595 - val_acc: 0.8069
Epoch 39/50
390/390 [==============================] - 43s 109ms/step - loss: 0.5108 - acc: 0.8204 - val_loss: 0.5327 - val_acc: 0.8188
Epoch 40/50
390/390 [==============================] - 43s 110ms/step - loss: 0.5107 - acc: 0.8202 - val_loss: 0.5299 - val_acc: 0.8217
Epoch 41/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5053 - acc: 0.8225 - val_loss: 0.5425 - val_acc: 0.8110
Epoch 42/50
390/390 [==============================] - 42s 108ms/step - loss: 0.5000 - acc: 0.8231 - val_loss: 0.5340 - val_acc: 0.8214
Epoch 43/50
390/390 [==============================] - 42s 108ms/step - loss: 0.4989 - acc: 0.8250 - val_loss: 0.5493 - val_acc: 0.8149
Epoch 44/50
390/390 [==============================] - 42s 108ms/step - loss: 0.4893 - acc: 0.8276 - val_loss: 0.5319 - val_acc: 0.8178
Epoch 45/50
390/390 [==============================] - 42s 108ms/step - loss: 0.4890 - acc: 0.8266 - val_loss: 0.5340 - val_acc: 0.8181
Epoch 46/50
390/390 [==============================] - 42s 108ms/step - loss: 0.4860 - acc: 0.8302 - val_loss: 0.5174 - val_acc: 0.8215
Epoch 47/50
390/390 [==============================] - 42s 108ms/step - loss: 0.4862 - acc: 0.8273 - val_loss: 0.5280 - val_acc: 0.8204
Epoch 48/50
390/390 [==============================] - 42s 108ms/step - loss: 0.4836 - acc: 0.8285 - val_loss: 0.5341 - val_acc: 0.8193
Epoch 49/50
390/390 [==============================] - 43s 109ms/step - loss: 0.4793 - acc: 0.8322 - val_loss: 0.5317 - val_acc: 0.8213
Epoch 50/50
390/390 [==============================] - 42s 108ms/step - loss: 0.4808 - acc: 0.8318 - val_loss: 0.5265 - val_acc: 0.8196
Model took 2118.27 seconds to train

Highest Accuracy on test data is: 82.15

