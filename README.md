# baseball
KBO 야구 데이터 분석

# 주제
: 선수의 능력 분석을 통한 승률 예측
```
목적 : 시장? post-corona 로 한국 야구에 대한 세계 관심도 증가 -> 미래 발전 가능성 있음
wordcloud 분석으로 관심도 증가 보여주고

구단의 선수 구성 시에 영입 리스트 
구단 연봉 총액 대비 구단 등수에 대한 비교

WBO 선수 리스트

```

# 데이터셋
2013 - 2019 년도의 7년치 데이터 (근거 : 신규 구단 창단)
- 방법 : 크롤링
- 관련사이트
  https://www.koreabaseball.com/Record/Player/HitterBasic/Basic1.aspx
```
투수, 유격수
```

# 분석 방법
1) 문제 정의 및 분석 목표 세우기
- 둘로 나누어 예측
- 머신러닝 모델 활용 -> 정확도 높은 모델 제안 -> 중요한 변수 도출

2) 데이터 전처리
- 결측치 처리
- 컬럼 추가 / 정리

3) 시각화
- 변수별 관계 시각화 -> 비율 도출
```
1. 문제 정의
- 2개의 요소로 나누어 예측: 각 데이터를 독립변수와 종속변수로 비교분석을 위해 데이터를 나누어 예측한다 -> 패턴 -> 인사이트 예측
- 주제 배경 관련하여 가설 설정 -> 2개 요소의 상관관계를 분석하여 사실여부 확인 / 검증
(분석 목적 -> 가설 설정)

2. 데이터 수집
- 분석 범위 정하기 -> 몇개년의 데이터를 표본으로 준비할 것인지? -> 중심극한 정리에 따라 데이터 정규성 확보 -> 데이터 수집 (가장 높고, 낮은으로 나누어)
- 크롤링하여 데이터 받아보기

3. 데이터 정제
- 크롤링하여 받은 데이터를 분석에 필요한 자료들만 추출하여 데이터를 정리
- R로 데이터 불러오기
- 독립변수 데이터 vs 종속변수 데이터 만들기 -> 데이터 합치기!

4. 분석
- 현상의 관련성 위해서 각 변수 간의 그래프 그려보고 비율 비교: 상관관계 분석 -> 산점도, 회귀 직선 그려보기

5. 결론
- 가설 검증 결과 -> 상관관계 있다는 것을 밝힘 -> 해결 방안이나 필요성 도출 (+ 근거에 대한 내용; 관련 논문/기타)

6. 요구사항
-R, python

```

4) 통계 분석
```
1. 상관 분석
2. T-test : 컬럼 제외
3. 카이제곱 검정 : 비율 차이 비교
4. PCA 주성분 분석 (screeplot 시각화)
```

5) 머신러닝 적용
- 랜덤포레스트, 의사결정나무(decision tree) -> 변수 중요도를 도표로 시각화

6) 결론
```
1. 가장 정확도 높은 모델의 비율
2. 중요 변수 도출
```

7) 요구사항
- 엑셀, R : 비율 시각화
- SAS : 통계 분석
- python : 머신러닝 적용(colab)

