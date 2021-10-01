# 팀 NLP 11조 Week9 Day5

## 목차
- [피어세션](#피어세션)
	- [토론](#토론)
	- [TODO](#todo)
	- [앞으로 할 일](#앞으로-할-일)

## 일자
- 2021.10.01 금

## 팀원
- 문석암_T2075
- 박마루찬_T2078
- 박아멘_T2090
- 우원진_T2137
- 윤영훈_T2142
- 장동건_T2185
- 홍현승_T2250

## 피어세션

### 토론
- roberta-base가 bert-base보다 Submission이 왜 낮은가? (논문에서는 비슷함)
    - 설정이 잘못 되었을 가능성이 있지 않을까?
    - roberta-large 성능에도 영향을 주지 않을까?

- 논의 사항은 앞으로 Issue 또는 Disscussions에 논의 해보기!
    - 카톡 등을 이용해서 충분히 가능하나 외부에 활발한 활동 자료로 보여지기 위함.
    - 의문은 Disscussions, 명백히 고칠 점이 있다면 Issue. 정 애매하면 Disscussion 후 Issue.

- 앞으로 어떤 실험을 할까?
    - klue/bert-base, batch = 32, lr = 5e-5, warmupstep = 500(default), lr_decay = 0.01
    1. Adaptation 문석암, 장동건
    2. AEDA    박마루찬
    3. EDA     박아멘
    4. Entity embedding     윤영훈, 우원진, 홍현승
    
    - 어제자 오피스아워 
    -> Entity marker
    -> Additional embedding layer
    -> 아웃풋 모델 추가하기
    -> 도메인 데이터로 한번 더 사전학습

- bestModel
    - f1 기준으로 ??? best model 기준 제출해보고 checkpoint 기준 제출


### TODO

-  TODO
    1. Adaptation 문석암, 장동건
    2. AEDA    박마루찬
    3. EDA     박아멘
    4. Entity embedding     윤영훈, 우원진, 홍현승 
    5. Early stopping       추가


### 앞으로 할 일


- 윤영훈 - roberta-large (10-5, 0, 0)(10-5, 0, 0.01)(10-5, 0.6, 0) 
- 홍현승 - roberta-large (5e-5, 0, 0.01)(5e-5, 0.6, 0) 

