# 2021

## August

1. Factorization Machine
    - SVM의 장점(real value feature를 사용)과 Factorization Model의 장점(feature들끼리의 interaction 고려)를 합친 모델이다.
    - $$ \hat{y}(x) = w_{0} + \sum_{i=1}^{n} w_{i} x_{i} + \sum_{i=1}^{n} \sum_{j=i+1}^{n} <v_{i},v_{j}> x_{i} x_{j}  $$ 

    > $$w_{ij} ( \in R^{n \times n})$$ 대신, factorizing $$v_{i} ( \in R^{n \times k}$$하여 사용

    - 위의 model equation에서 특별한 제약은 없기에 특수한 변환없이 바로 optimize가 가능하고 linear time에 수행된다.

2. Wide and Deep learning for Recommender System
    - Linear model(with nonlinear feature transformation의 장점(Sparse에 강한 간단한 feature interaction 캡쳐) 과 Deep Neural Network의 장점(unseen feature combination)을 합친 모델이다
        > Linear model은 generalization에 대해, DNN은 sparse feature를 캡쳐하지 못한다는 단점을 가지고 있다

    - Wide component: 
        - Input: raw feature, transformed feature(binary feature)
        - Model: Linear model, Cross-product transformation
    - Deep component: 
        - Input: categorical feature
        

3. DLRM

    - Numerical feature(Dense feature)를 Bottom MLP로, Categorical feature를 Embedding하여 나온 결과들을 pairwise interaction하여 상호작용을 고려한다 (자세한건 안나옴)

    - Butterfly shuffle을 통해 병렬화 (사실상 핵심)
