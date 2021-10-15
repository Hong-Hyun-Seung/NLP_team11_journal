# 팀 NLP 11조 Week11 Day4

## 목차


- [피어세션](#피어세션)
	- [추가 결정사항](#추가-결정사항)
	- [팀 분배](#팀-분배)
	- [계획 수립하기](#계획-수립하기)
		- [Read](#read)
		- [Retrieval](#retrieval)
		- [data 분석 (+ 각 페이즈별 input - output)](#data-분석--각-페이즈별-input---output)
	- [Baseline 코드 발표](#baseline-코드-발표)
	- [code](#code)
		- [wandb](#wandb)
		- [black autoFormatting](#black-autoformatting)
	- [gitignore](#gitignore)

## 일자
- 2021.10.15 금

## 팀원
- 문석암_T2075
- 박마루찬_T2078
- 박아멘_T2090
- 우원진_T2137
- 윤영훈_T2142
- 장동건_T2185
- 홍현승_T2250

## 주간 일정
![](https://i.imgur.com/eOAapYi.png)


## 피어세션
### 추가 결정사항
- 코드 이해를 위해 PR시 6명 approve를 기대해보자.
- 피어세션에서 코드리뷰를 해 보자 (최대한 빠르게)

### 팀 분배
- Reader
    - 박마루찬
    - 우원진
    - 윤영훈
    - 홍현승
    
- Retrieval 
    - 문석암
    - 장동건
    - 박아멘
    
### 계획 수립하기
- MRC 논문에서 제시한 모델 고려.
- baseline 코드, 입출력에 관한 설명을 준비해보자. (팀 분배 참고)

#### Read
- 아이디어
    - Retriever 훈련 할 때, 여러 문서 선택할 수 있게 하기
- Refactoring (train.py) - 원진, 영훈
- 코드 이해  - 현승
- Eval score 차이의 원인 파악 혹은 문제 없는지 확인 - 박마루찬

#### Retrieval
- Sparse 비교 가능한 평가
    - 자체 평가 진행 필요 (do_eval) -문석암, 박아멘, 장동건
        - Question,Context pair로 만 가지고서 비교

- Dense 따로 구성
    - 할 일 끝내놓고 시도해보자.
- 하이브리드 또는 성능 개선
    - 이건 선행이 끝나야 가능한? 맞아용 

#### data 분석 (+ 각 페이즈별 input - output)
- 시간이 남거나, 다음 도전이 어렵다면 짬을 내서 시도해 보자. 빠를수록 좋다.


### Baseline 코드 발표
- Retrieval 
    - 약간의 코드 문제가 있다. default 대신 metavar로 설정된 점 등.
    - docstring이 많은 것을 설명해줌
    - inference.py --do_eval 하면 이런 문제가 생김 (train dataset에 대해서 해도)
    ![](https://i.imgur.com/qAxGFix.png)


### code
```
code
    asset
    install
    output
    retrieval
        arguments.py (임시)
        retriever.py
        train.py
        saved_models
    read
        arguments.py (임시)
        train.py
        custom_reader.py
        reader.py
        saved_models
        utils_qa.py
        train_qa.py
    arguments.py (최종 릴리즈 때)
    inference.py    

data (path 는 고정)

```
#### wandb
- 개인 프로젝트에서 메인 프로젝트로 넘기기


#### black autoFormatting
- pre commit (관련 수행 문서로 올릴게요)
- 포맷팅만 자동으로 수행주는 (python 공식 규격)

### gitignore

```
**/wandb/
**/__pycache__/
**/.ipynb_checkpoints/
**/data/
**/results/*
**/prediction/*
**/best_model/*
**/models/*
**/.*/
**/outputs/
!.gitignore
!sample_submission.csv
nohup.*
**run.sh
```


[한국어 지원 목차 생성](https://magnetikonline.github.io/markdown-toc-generate/)


