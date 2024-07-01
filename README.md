# 🖥 Machine Learning Project
---
## 💡 Introduction
**넷플릭스 시즌제 드라마의 후속작 흥행 예측**  
Project: Predicting the Next Big Hit Netflix Sequel Drama

## 🎈 프로젝트 개요
1. 팀원: 강민지, 김이영, 이예슬, 조규리, 천준규
2. 수행 기간: 2024.05.28 \~ 2024.06.28 (4주)

## **🕹 프로젝트 소개**
### 배경
- why Netflix?
- why Drama?

## 📌 프로젝트 진행 순서
![플로우차트 (1)](https://github.com/ML-project-3/ML_project/assets/155655348/007df57f-8f62-4b23-9fed-230d74c56556)

## 📑데이터 수집
/데이터 프레임/![image](https://github.com/ML-project-3/ML_project/assets/155655348/ab643ec3-cec5-4766-8f92-c6ef9bc92a59)

- 프로젝트 전제조건
- JustWatch
- IMDb
- Watcha

## ⌨ 데이터 전처리
<details>
<summary><b> 결측치, 이상치 처리 1090개 ➡ 904개 </b></summary>
  
> **결측치** :  
> < IMDb >
> 1. 연령 등급 보완: 넷플릭스 공식 자료를 참고하여 연령 등급 결측치 보완
> 2. 에피소드 별 평점 결측치 삭제: 드라마 시즌 1, 2의 에피소드 별 평점에 하나라도 결측치가 있을 시 제외
> 3. 한국 방영과의 괴리 해소: 외국에서는 방영했으나 한국에서 서비스하지 않은 경우 그 시즌만 삭제
> 4. 외전 삭제: 정식 시즌이 아니므로 제외
> ---
> < Watcha >
> 1. 평점 통합: 하나의 시즌을 파트 1, 파트 2로 구분한 경우 평균으로 처리
> 2. 결측치 보완 및 삭제:드라마 평점이 존재하지 않는 경우 제작 국가 별 중앙값으로 처리
>
> **이상치** :
> 드라마 간 평점과 인기의 불균형은 존재하지만 어떤 것이 이상치이고, 이상치가 아닌지 구분할 수 없음
> ➡ 대중의 의견을 존중하기 위해 이상치 제거는 하지 않음


  
</details>

## 🔍EDA


## 📝흥행 지표 생성
![image](https://github.com/ML-project-3/ML_project/assets/155655348/d1fdd8e0-d8b5-42a8-93dd-4933835cdd78)
<details>
<summary><b> 흥행지표 자세한 내용</b></summary>
  
> **가중치_참고** : 
>
> **계산식** : 
  
</details>

## 📈머신러닝
- 초기
- 최종
- 흥행 등급

## 👀추가 분석
- 추가 파생변수 season_gaps
- 오징어 게임 2 예측

  
## 🔥이슈 및 트러블슈팅

<details>
<summary><b> 이슈</b></summary>
  
> **문제** : 
>
> **해결** : 
  
</details>
