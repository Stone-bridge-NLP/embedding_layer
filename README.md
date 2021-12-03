# Embedding layer
Genre classification by lyrics using keras Embedding layer   

</br>

## Code
- main.ipynb : Genre classification by lyrics with keras Embedding layer and LSTM layer [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1L7IdtLYqZxobeXrN2xPqFfJWxrTbwgbc?usp=sharing)

</br>

## Result

### 1. Use unbalanced train data
#### Genre plot   
![download](https://user-images.githubusercontent.com/44018094/144588387-f4023473-e1d4-4752-a2c9-58ddc3a4f096.png)

#### accuracy & loss   
![download](https://user-images.githubusercontent.com/44018094/144588519-076f532b-a7cb-4edd-b065-076e19978aaa.png)
![download](https://user-images.githubusercontent.com/44018094/144588521-1415852f-f9e8-476a-b1ed-59464f9ddfb4.png)

#### F1-score
```
              precision    recall  f1-score   support

     Hip-Hop       0.00      0.00      0.00       960
       Indie       0.00      0.00      0.00       510
       Metal       0.58      0.59      0.58       810
         Pop       0.22      0.44      0.30      1110
     Country       0.00      0.00      0.00       810
        Jazz       0.58      0.26      0.36       659
        Rock       0.24      0.77      0.36      1410
         R&B       0.00      0.00      0.00       509
  Electronic       0.00      0.00      0.00       659
        Folk       0.26      0.04      0.06       495

    accuracy                           0.28      7932
   macro avg       0.19      0.21      0.17      7932
weighted avg       0.20      0.28      0.20      7932
```

</br>

### 2. Use balanced train data
#### Genre plot
![download](https://user-images.githubusercontent.com/44018094/144588782-0fc21653-605e-4395-bb4b-2df1db571644.png)

#### accuracy & loss   
![download](https://user-images.githubusercontent.com/44018094/144590178-cf4cebb8-ddb1-42e8-a754-cab7ba3f919b.png)
![download](https://user-images.githubusercontent.com/44018094/144590188-84a5b623-aaac-4e42-956c-953d6d2b3935.png)

#### F1-score
```
              precision    recall  f1-score   support

     Hip-Hop       0.55      0.66      0.60       960
       Indie       0.14      0.14      0.14       510
       Metal       0.35      0.42      0.38       810
         Pop       0.18      0.02      0.04      1110
     Country       0.32      0.34      0.33       810
        Jazz       0.28      0.31      0.29       659
        Rock       0.22      0.12      0.16      1410
         R&B       0.12      0.21      0.15       509
  Electronic       0.13      0.20      0.16       659
        Folk       0.15      0.26      0.19       495

    accuracy                           0.26      7932
   macro avg       0.24      0.27      0.24      7932
weighted avg       0.26      0.26      0.25      7932
```

</br>

### 3. Use balanced train data & drop out, normalization
#### accuracy & loss   
![download](https://user-images.githubusercontent.com/44018094/144589782-8897f892-8c21-4d77-9edb-e32e69621106.png)
![download](https://user-images.githubusercontent.com/44018094/144589786-8105527d-63f9-47db-ad3a-c3c560ae1abc.png)

#### F1-score
```
              precision    recall  f1-score   support

     Hip-Hop       0.63      0.72      0.67       960
       Indie       0.11      0.35      0.17       510
       Metal       0.43      0.63      0.51       810
         Pop       0.27      0.08      0.12      1110
     Country       0.31      0.34      0.32       810
        Jazz       0.24      0.29      0.26       659
        Rock       0.26      0.03      0.06      1410
         R&B       0.13      0.26      0.18       509
  Electronic       0.17      0.10      0.13       659
        Folk       0.15      0.14      0.15       495

    accuracy                           0.28      7932
   macro avg       0.27      0.29      0.26      7932
weighted avg       0.29      0.28      0.26      7932
```

</br>

## Reference
- keras Embedding layer
  - https://keras.io/api/layers/core_layers/embedding/
  - https://heegyukim.medium.com/keras-embedding%EC%9D%80-word2vec%EC%9D%B4-%EC%95%84%EB%8B%88%EB%8B%A4-619bd683ded6
- keras LSTM
  - https://wikidocs.net/32105
  - https://keras.io/api/layers/recurrent_layers/lstm/
  - https://cheris8.github.io/artificial%20intelligence/DL-Keras-Loss-Function/
- performance improvement
  - https://www.tensorflow.org/tutorials/keras/overfit_and_underfit?hl=ko
  - https://keras.io/api/layers/regularization_layers/dropout/

