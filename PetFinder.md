

### 데이터셋 구성 및 설명
1. **Breed Labels (품종 데이터)**: `BreedID`, `Type`(1: 개, 2: 고양이), `BreedName`.
2. **Color Labels (색상 데이터)**: `ColorID`, `ColorName`.
3. **State Labels (지역 데이터)**: `StateID`, `StateName`.

---

### 1. EDA (Exploratory Data Analysis)로 특이점 발견하기

#### (1) **데이터 분포 확인**
- **품종 분포**: `Type`을 기준으로 개와 고양이 품종의 분포 확인 가능. 개의 품종 데이터가 고양이 품종보다 많음. 이 분포를 기반으로 유형별 수요 패턴을 분석할 수 있음.
  
- **색상 분포**: `ColorID`를 기준으로 어떤 색상이 더 자주 등장하는지, 특정 색상이 인기가 있는지 확인 가능.

- **지역 분포**: `StateID`로 지역별 데이터를 분포를 확인 가능. 말레이시아의 주(State)별로 구매 패턴이 달라질 수 있으며, 인구 밀도나 경제적 요인과 연결될 수 있음.

#### (2) **Null 값 또는 이상치 확인**
- 

#### (3) **변수 간의 상관관계 분석**
- **Type**(개와 고양이)과 **ColorID**(색상) 또는 **StateID**(지역) 간의 관계를 분석하여, 특정 지역에서 선호하는 품종이나 색상 패턴 분석.
  
#### (4) **구매 패턴 분석**
- 구매 패턴이 시간에 따라 어떻게 변하는지 확인하려면 추가적인 시간 데이터를 결합 필요.

---

### 2. 피처 엔지니어링 아이디어

#### (1) **지역성**
- 각 주(State)의 인구 밀도, 소득 수준 등 외부 요인을 반영한 피처.

#### (2) **연령대**
- 연령대에 따라 선호하는 품종이나 색상 차이가 있을 수 있습니다. 5년 간격으로 나눈 연령대 데이터가 있다면, 연령대별로 소비 패턴을 분석하여 맞춤형 마케팅 전략을 세울 수 있습니다.

#### (3) **시간 요인**
- 월별.

#### (4) **카테고리**
- 대/중/소 카테고리 간의 상호작용을 분석, 각 카테고리에서 인기... 있는 품종 및 색상을 분석.

---

### 3. 예측 모델 아이디어 (궁극적 목표)

#### (1) **수요 예측**
- 각 품종이나 색상별로 월별, 지역별 수요를 예측하는 모델을 구축.

#### (2) **타겟 마케팅**
- 지역별, 연령대별로 어떤 품종이나 색상이 선호되는지를 예측하여 맞춤형 홍보. (유기동물의 더 많은 입양을 위해.)

#### (3) **군집 분석**
- 구매자들을 군집화하여, 비슷한 구매 성향을 가진 고객끼리 그룹화. 클러스터링 가능.