# LlamaFineTuningProject

## 파일 설명

transform_data : 데이터를 적합한 형태로 정제한 코드

translate : 파인튜닝을 진행한 후, 번역문을 출력하고 BLEU 스코어를 측정한 코드

## 내용

- 데이터 로드
  
LLaMA 모델을 학습시키는데 필요한 데이터의 형식인 json파일 형태로 로드합니다.
- 데이터 전처리
  
LLaMA 모델을 학습시키는데 적합한 프롬프트 형식으로 새로운 json 파일을 write한 뒤 저장합니다. 전체 데이터 중 200개의 데이터 쌍을 선택했습니다.
- 파인튜닝
  
HuggingFace의 autotrain 모듈을 이용해 LLaMA2 모델을 파인튜닝 합니다.
- 번역문 출력
  
파인튜닝한 모델에 데이터를 입력해 번역문을 출력하도록 합니다.
- 평가
  
BLEU 스코어를 이용해 모델을 평가합니다.

### 성과

번역된 문장의 품질을 평가하기 위해 BLEU 스코어를 활용하였고, 이를 통해 구글 번역기 대비 약 33% 높은 스코어를 달성.

### 주요기술

- python
- AutoTrain
- NLTK
- Transformers
