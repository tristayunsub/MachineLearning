https://techblog-history-younghunjo1.tistory.com/5?category=863123


머신 러닝의 다양한 모델중 하나인 decision tree 



분류와 회귀 방법에 모두 적용 가능. 새로운 데이터가 특정 terminal node에 속한다는 정보를 확인하고. 해당 terminal node에서 가장 빈도가 높은 범주에

새로운 데이터를 분류시킴.

<불순도/ 불확실성?>

의사결정 나무는 하나의 분기떄마다 변수 영역 두개


분류나무는 구분 뒤 각 영역의 순도(homogeneity)의 증가, 불순도(impurity) 혹은 불확실성(uncertainty)이 최대한 감소하도록 하는 방향으로 학습을 진행한다.


 그리고 이러한 이상적인 상태를 정보획득(information gain)이라고도 부른다
 
 
 가지치기 prunning?
 
 모든 terminal node의 순도가 100%(엔트로피가 0)인 상태를 Full tree라고 하는데 이렇게 Full tree를 생성한 뒤

적절한 수준에서 terminal node를 결합(가지치기)를 해주어야 한다. 왜냐면 이것은 분기가 너무 많아서 학습데이터에 과적합을 막기 위한 것이다(


<비용 함수(Cost Function)>

 

마지막으로 가지치기의 비용함수(cost functio)를 보자. 의사결정나무는 이 비용함수를 최소로 하는 분기를 찾아내도록 학습된다. 정의는 밑과 같다.

 

* CC(T)=Err(T)+α×L(T)CC(T)=Err(T)+α×L(T)

 

CC(T)=의사결정나무의 비용 복잡도(=오류가 적으면서 terminal node 수가 적은 단순한 모델일 수록 작은 값)

ERR(T)=검증데이터에 대한 오분류율

L(T)=terminal node의 수(구조의 복잡도)

Alpha=ERR(T)와 L(T)를 결합하는 가중치(사용자에 의해 부여됨, 보통 0.01~0.1의 값을 씀)
