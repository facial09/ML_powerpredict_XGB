# ML_section2_XGB

###과거 기상정보,건물정보 등과 전력사용량이 주어지고, 이를 통해서 향후 발생할 1주일간의 전력량을 예측하는 프로젝트**

- Modeling 이전 적절한 metrics 선정 : SMAPE
- Feature Engineering 을 진행하여 유의미 하다고 여겨지는 추가적인 feautres 생성
- Boxplot,histogram을 통해 outlier 확인후 standardlized( skewness(3), kurtosis(7) 을 기준으로 진행 )
- Trend/ Seasonality / Cycle / Residual 분석
- Linear regressor를 base model로 잡고 XGB regressor model을 구현
    - Arima model 또한 고려하였지만, 성능과 자원활용에 있어서 좋은성능을 보인 XGB를 선택
- validation에 대한 predict와 real value를 시각적으로 비교

**결과 : SMAPE 10~20 이상의 base model 과 비교했을 때, 10이하의 SMAPE를 보이는 XGB model을 만들어냄**
