# digit-recog

1) Dataset has been imported using keras, which contains both training set(60000) & testing set(10000).
2) X_train & X_test data has been normalized.
3) We have created a sequential model: 
2DConvolutionLyr  -> 2DMaxPoolingLyr -> 2DConvolutionLyr -> 2DConvolutionLyr -> 2DMaxPoolingLyr -> Flatten -> DenseLyr -> Output(Dense)Lyr
  (32U , (3,3))          (2,2)            (32U , (3,3))      (32U , (3,3))          (2,2)                      (20U)         (10U)
     RELU                  -                  RELU               RELU                 -              -          RELU        SOFTMAX
4) We have used SGD optimizer with learning rate  = 0.1 & momentum = 0.9 . Loss function used is categorical cross entropy since it is a multi-classification model.
5) We have used 5-fold cross-validation to test the data on validation set
