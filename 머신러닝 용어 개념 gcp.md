gcp에서도 이거 다룸


2. Feature란? Attribute 와 다른가?

결론적으로 Feature와 Attribute는 똑같은 개념이다. 사람들이 혼용해 부르기도 한다. Feature은 여러가지 데이터 타입(type)이 될 수 있다. 예를들어, Categorical(Nominal)이라 부르는 범주형 데이터, String(문자열), Number(숫자) 가 될 수 있다.

 

그렇다면 Feature의 갯수는 어느정도가 적당할까? 우선 분류문제에서는 label(class)갯수 < Feature 갯수 < Data 갯수 

가 되는 것이 일반적이다. 그러면 Feature 갯수를 무작정 늘린다면 과연 어떻게 될까? **차원의 저주** 에 걸리게 된다. 


또한 Feature를 잘 정의하기 위해서는 머신러닝 모델을 적용하려고 하는 해당 분야의 지식 즉, 도메인 전문지식이 요구된다.

 


그런데 만약 도메인 전문지식을 얻기가 너무 힘들다면 어떻게 할까? 이 때 바로 딥러닝이라는 개념이 등장한다.

딥러닝은 머신러닝처럼 Feature을 굳이 정의하지 않아도 데이터들에 기반해 Feature을 스스로 찾아 스스로 학습하게 된다


딥러닝을 하기 위해서는 대신 딥러닝 모델의 노드(Node)갯수나 여러가지 학습방법 중 어떤 방법을 사용할지에 대한 선별능력을 갖추기 위한 지식이 필요하다.


3.모델이란? 우리는 이걸 hypothesis 라고도 부른다. 데이터를 통해 배운다.

모델선정시 두가지 개념 고려 매우 중요

Complexity(복잡성)과 Data(Sample Consistency)

Complexity : 데이터 수가 증가함에 따라 Computational Operation(컴퓨팅연산)이 얼마나 증가하는지 이다. 

복잡성은 만약 두 개의 모델이 동일한 결과물을 낸다는 가정 하에 복잡성이 더 큰 모델이 좋지 않음을 의미한다.

Data : 데이터 개수가 증가함에 따라 결과값의 품질(Quality)가 얼마나 좋은지를 의미한다. Data라는 특성이 클수록 좋은 것이다.



보통 비지도 학습들은. parametric과 non-parametric으로 구분됨.

parametric: 주어진 데이터가 어떤 분포로 부터 생성된건지 가설로 세우고. 파라미터를 통해 접근.

non-parametric: feature가 너무 많거나 데이터 분포 양상에 대해 가설을 세우지 못할때 사용, knn 또는 decision tree




ROC Curve 매우 중요~

여러 임계값을 기준으로 recall-fallout의 변화를 시각화한것. 

참고로 이러한 ROC Curve를 그래프가 아닌 수치로 비교한 것이 AUC(Area Under Curve)이며 클수록 1에 가까워 진다.


<모델 평가 기준>

모델 평가할 때 어떤 기준으로 평가를 해야할까?

- Bias와 Variance를 고려한다. 각 값들이 높을 때 모델의 error가 어떤 그래프로 그려지는지 그림을 통해 살펴보자.



6. 데이터를 어떻게 Sampling할 것인가?

데이터들은 분포(Bias)가 치우쳐져있으면 안된다. 따라서 다음과 같은 Sampling 방법들을 사용한다.

 

Down-Sampling : 비율이 많은 데이터들 중 적게 일부를 선택해 사용

Up-Sampling : 데이터 수가 적어서 비슷한 데이터들을 임의로 만들어 사용

Distant-Supervision : 반지도학습 방식으로 어떠한 '가정'을 Label로 취급한다. 예를들어 "머리카락 길이가 30cm이상이다" -> "여자이겠구나!" 

Bagging(Bootstrap aggregating) : 데이터가 충분하지 않을 때 사용한다. 예를들어 총 데이터 갯수가 100개가 있다면 10개가 들어갈 수 있는 여러개의 가방들을 만들고 한 가방에 10개만 넣고 그 가방속의 10개 데이터들로만 모델을 학습시키는 방법
- 
