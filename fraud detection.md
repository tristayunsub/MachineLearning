https://laboputer.github.io/machine-learning/2020/05/29/creditcardfraud/

https://log-laboratory.tistory.com/category/Competition?page=1

 284,807 건의 거래내역이 제공됩니다. 이 중 492건이 사기 거래(Fraud Transaction)이고 사기 거래가 정상 거래에 비해 매우 적은 0.172%로
 
 
 ‘Highly unbalanced’한 특징을 가진 데이터셋입니다
 
 
 
 
 Highly unbalanced datasets
 
 신용카드 사기 거래 감지하기(Credit Card Fraud Detection) 문제를 통해 
 
 
 Highly unbalnced한 데이터셋을 다루기 위한 모델 평가 지표와 레이블 을 알 수 없는 데이터 (사기 거래인지 모르는)를 어떻게 접근했는지를 정리한 내용입니다.
 
 
 
 분류 문제의 평가지표 ‘F1-score’
 
 각 경우의 수를 어떻게 계산하느냐. 여러가지 의미를 ㅏ지는 지표.
 
 accuracy, precision recall, f1-score
 
 정확도는: 모든 예측이 실제로 맞은 비율
 
 precision: 정밀도 'true' 라고 예측한 것 중 실제로 true인 비율
 
 recall(재현율: 모든 true인 것 중 'true'로 예측한 것의 비율
 
 
 f1-score: 정밀도, 재현율의 조화 평균
 
 
 flase negative? 예를들어 1개의 거래만 사기라고 예측해서 실제로 맞히면. precision은 1임. 한번의 시도가 맞ㅇㅁ.
 
 반면에 전체거래가 사기면 recall도 무조건 1. precision과 recall 은 항상 역의 관계를 가짐
 
 
 우리가 기상청ㅇ이라고 가정. 강수확률이 90퍼센트일때만 우천방송한다하면. 강수확률이 60~80퍼센트일떄도 예보를안하면 그것도 좀이상함.
 
 근데 비가오지않을경우가 많을때 (precision이 낮은). 그래서 욕먹음. 
 
 precision과 recall의 조화 평균인 f-1score를 가장 중요한 평가지표로..
 
 
 먼저 할일 EDA(Exploratory data analysis)로 주어진 데이터가 어떤 형태인지 각자 자유롭게 파악한다
 
 
 실제 현실에서는 레이블링되어잇는 데이터가 없는 경우가 많기에. 이럴경우는 어떤 방식으로 접근해야 되는지.
 
 이렇게 만든 모델을 어떻게 평가할수있는지
 
 
 
 
 
 
