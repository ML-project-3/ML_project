# 🖥 Machine Learning Project
<img src="https://github.com/ML-project-3/ML_project/assets/80812507/517d9b68-7894-495f-ba95-f16bd69b61ea  width="800"/>
---
## 💡 Introduction
**넷플릭스 시즌제 드라마의 후속작 흥행 예측**  
Predicting the Next Big Hit Netflix Sequel Drama

## 프로젝트 개요
1. 팀원: 강민지, 김이영, 이예슬, 조규리, 천준규
2. 수행 기간: 2024.05.28 \~ 2024.06.28 (4주)

## 프로젝트 소개
### 배경
- Why Netflix?
    - 넷플릭스는 글로벌 스트리밍 시장을 선도하는 기업으로, 현재 190개 국가에서 서비스 中
    - OTT 시장의 성숙기 진입 -> 미국을 중심으로 스트리밍 시장 포화
    - 넷플릭스 또한 수익 증가율, 구독자 증가율이 둔화되고 있음
    -> '컨텐츠'를 통해 비즈니스 문제를 해결할 수 있음  
  <출처:한국콘텐츠진흥원, '글로벌 OTT 트렌드 Vol 5', 2024.05.14., 'https://www.kocca.kr/globalOTT/vol05/main/index.html'>
- Why Drama?
    - 드라마는 긴 서사 구조 -> 시청자들의 지속적인 관심을 확보 가능
    -> 구독자 유지, 수익 안정성에 기여

![넷플릭스그래프](https://github.com/ML-project-3/ML_project/assets/80812507/654ac587-59f8-43cb-b5c8-c90ea909fa97)
<출처:BACKLINKO, 'Netflix User & Growth Stats: How Many People Subscribe?', 2024.04.08., https://backlinko.com/netflix-users>


### 프로젝트 진행 순서
![플로우차트 (1)](https://github.com/ML-project-3/ML_project/assets/155655348/007df57f-8f62-4b23-9fed-230d74c56556)

## 데이터 수집(크롤링)
![image](https://github.com/ML-project-3/ML_project/assets/155655348/ab643ec3-cec5-4766-8f92-c6ef9bc92a59)

- **프로젝트 전제조건**: 한국 넷플릭스에서 현재 시청 가능한 드라마 중 ~ 2023. 12. 31까지의 작품
- **JustWatch**
    - 스트리밍 동영상 검색 엔진
    - 국내에서 서비스 중인 넷플릭스 드라마 데이터 확보에 이용
   **IMDb**
   - 세계 최대의 영상 매체 데이터 베이스
   - 글로벌 평반 반영
- **Watcha**
  - 한국의 영상 매체 데이터 베이스
  - 동양권 드라마에 대한 평판 보완

## 데이터 전처리
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
> -> 대중의 의견을 존중하기 위해 이상치 제거는 하지 않음


  
</details>

## EDA
![image](https://github.com/ML-project-3/ML_project/assets/80812507/812a1b3d-1fcb-4b79-9938-a149091b2cb2)
- 시즌 1개만 있는 드라마가 639개, 시즌 2개가 있는 드라마는 266개

![image](https://github.com/ML-project-3/ML_project/assets/155655348/abd01e5d-c250-4e8a-941b-68ad61d565a7)
- 시즌제 드라마의 제작이 2021년부터 감소 추세를 보임. 반면 단일 드라마의 제작은 활발함.

## 흥행 지표 생성
![image](https://github.com/ML-project-3/ML_project/assets/155655348/d1fdd8e0-d8b5-42a8-93dd-4933835cdd78)
<details>
<summary><b> 흥행지표 자세한 내용</b></summary>
  
> **가중치_참고** : 
>
> **계산식** : ![image](https://github.com/ML-project-3/ML_project/assets/155655348/251c3725-fd5a-4e13-ba42-9ee0d7387a42)

  
</details>

## 머신러닝
- 초기
- 최종
- 흥행 등급: ![ML_Netflix project 평일오후3조 final (2)](https://github.com/ML-project-3/ML_project/assets/80812507/6d012b4f-b122-4f08-a19a-8cb5e12c4022)
- **대흥행**: 상위 5%에 해당하는 드라마로, 전체 드라마 중에서 가장 높은 흥행 성적을 기록한 드라마들  
  **흥행**: 상위 6-30%에 해당하는 드라마로, 전체 드라마 중에서 비교적 높은 흥행 성적을 기록한 드라마들  
  **호불호**: 전체 31-70%에 해당하는 드라마로, 대중에게 호불호가 갈리는 드라마들  
  **부진**: 전체 71-100%에 해당하는 드라마로, 흥행 성적이 저조한 드라마들  


## 추가 분석
- 추가 파생변수 season_gaps
- 오징어 게임 2 예측

  
## 🔥이슈 및 트러블슈팅

<details>
<summary><b> 이슈</b></summary>
  
> **문제** : 
>
> **해결** : 
  
</details>
