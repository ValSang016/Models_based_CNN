Active Learning #2

1) 학습 Schema를 변환시키는 경우
1. Idea를 통해 학습 Scheme 변환 (데이터 전처리, 학습에 사용되는 hyperparameter)
2. 여러 개의 모델 학습을 통해 성능 비교
3. 성능으로 본 가장 좋은 모델 선정 (Transfer Learning)

2) 모델을 변형 시키는 경우
1. 여러 개의 모델 학습을 통해 데이터에 맞는 성능 좋은 모델 선정(Transfer Learning). 
2. 모델 학습방법 변형. 논문을 통해 사용한 방법론이 젤 좋기는 하다..... ex) BN사용, Global average 사용

3) 1번 방법과 2번 방법을 합쳐서 결과를 비교하는 방법.
- 1번, 2번 모델이 같은 경우 : 1번, 2번 방법을 합쳐, (1번 방법, 2번 방법, 3번 방법을 비교한다)

- 1번, 2번 모델이 다를 경우 : 두 결과를 기준으로 성능을 높이는 방향으로 학습을 시킨다.

#모델 선정
새 50마리를 Classification하는 tasks이기 때문에 Pytorch에서 제공하는 ImageNet-1k를 test한 결과 성능(Acc@5)이 가장 잘 나온 Top4 모델을 선정할 것이다. 
1. EfficientNet_V2_M_Weights.IMAGENET1K_V1
2. ResNet50_Weights.IMAGENET1K_V2 : parameter수가 2배 차이나지만, 성능은 6퍼센트 높다
3. RegNet_Y_1_6GF_Weights_IMAGENET1K_V2 : ResNet18 parameter 수와 같은데 성능이 6퍼센트 높다.
4. ConvNext_Tiny_Weights.IMAGENET1K_V1 
