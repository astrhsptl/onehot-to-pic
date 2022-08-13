One-hot -> Num (28*28*1)
========================


# What it do?
This model just convert one-hot vector (shapes 1,10) in picture 28x28x1 px

# Model`s structure:

1. Input: shape = (1,10)
2. Dense: 12544, activation='relu'
3. BatchNormalization
4. Reshape: (7, 7, 256)
5. Conv2DTranspose: units=128 kernel=5 strides=(1, 1) padding='same' activation='relu'
6. BatchNormalization
7. Conv2DTranspose: units=64 kernel=5 strides=(2, 2) padding='same' activation='relu'
8. BatchNormalization
9. Conv2DTranspose: units=1 kernel=5 strides=(2, 2) padding='same' activation='sigmoid'

I take model from [this](https://www.youtube.com/watch?v=mTd-AlYp5IE&list=PLA0M1Bcd0w8yv0XGiF1wjerjSZVSrYbjh&index=33)

# If u want to use it:
1. Method 1:

```python
import keras

model = keras.models.load_model('/path/')
model.compile(loss='mae', optimizer='adam', metrics=['acc'])

...
```

2. Method 2

go to [this](https://drive.google.com/file/d/1HUjHl3BglWCurCXA4Es6zXdq3cEePsza/view?usp=sharing)
and start for modules