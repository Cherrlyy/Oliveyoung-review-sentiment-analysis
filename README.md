# 올리브영 스킨케어 광고 키워드 바탕의 사용자 리뷰 긍정도 분석


## 프로젝트 소개
구매의 바탕이 되는 리뷰의 제품 긍정도를 분석함으로써 광고에서 주장하는 제품 효능과 실제 사용 후기에서의 구매자가 경험한 효능의 정도를 분석하고, 이로부터 소비자의 제품 선택에 도움 줄 수 있도록 목표했습니다.

데이터 수집 및 분석의 자세한 내용은 밑 벨로그 주소를 찹고해 주세요.

[올리브영 스킨케어 광고 키워드 바탕의 사용자 리뷰 긍정도 분석(개선판)](https://velog.io/@_chaerry_/%EC%98%AC%EB%A6%AC%EB%B8%8C%EC%98%81-%EC%8A%A4%ED%82%A8%EC%BC%80%EC%96%B4-%EA%B4%91%EA%B3%A0-%ED%82%A4%EC%9B%8C%EB%93%9C-%EB%B0%94%ED%83%95%EC%9D%98-%EC%82%AC%EC%9A%A9%EC%9E%90-%EB%A6%AC%EB%B7%B0-%EA%B8%8D%EC%A0%95%EB%8F%84-%EB%B6%84%EC%84%9D%EA%B0%9C%EC%84%A0%ED%8E%B8)


## 폴더 구조
- code : 전처리 / 분석 등의 코드
- data : 원본 데이터 및 전처리 후의 데이터
- model : 학습 후의 머신러닝 모델
```
Oliveyoung-review-sentiment-analysis
 ┣ code
 ┃ ┣ advertisement_LDA.ipynb
 ┃ ┣ Oliveyoung_data_preprocessing.ipynb
 ┃ ┣ product_polarity_predict.ipynb
 ┃ ┣ review_type_polarity_count.ipynb
 ┃ ┗ Tfidf_Logisticregression_modeling.ipynb
 ┣ data
 ┃ ┣ ai_hub_data.csv
 ┃ ┣ oliveyoung_advertisement.csv
 ┃ ┣ oliveyoung_advertisement_preprocessed.csv
 ┃ ┣ product_polarity.csv
 ┃ ┣ review.csv
 ┃ ┣ review_final_preprocessed.csv
 ┃ ┗ review_type_polarity.csv
 ┣ model
 ┃ ┣ model.pk1
 ┃ ┣ model_pca_2500.pk1
 ┃ ┣ pca_2500.pk1
 ┃ ┗ tf_idf_vec.pk1
 ┗ README.md
```

## 과정
![image](https://github.com/user-attachments/assets/646af138-448f-461d-ba26-721fb56c7bbb)
### 전처리
- 불용어 처리, 토큰화(TfidfVectorizer 및 CountVectorizer)
- 데이터 균형을 위한 언더샘플링 및 오버샘플링(RandomUnderSampling 및 SMOTE)
- 차원 축소(PCA)

### 모델링
- 광고 주요 토픽 및 토픽별 주요 키워드 추출 위한 LDA
- 제품의 토픽별 리뷰 긍정도 분석 위한 LogisticRegression

### 분석 결과
![스킨케어 제품 평균 긍정도](https://github.com/user-attachments/assets/ead1632e-1c3f-42d3-9e92-06fca5a8bbcb)

