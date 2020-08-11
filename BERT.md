## BERT
- 딥러닝 자연어처리에서 단어를 벡터로 표현하는 단어임베딩은 필수적임
- 심볼인 단어를 실수 벡터로 표현해야 뉴럴네트워크 적용 가능
- BERT에서는 입력 문장의 단어에 대해서 뉴럴넷을 적용한 결과를 단어의 문맥 반영 벡터로 활용

### Pre-training(사전 학습)
1. 공백 단어 예측
- 입력 문장 중, 15%의 단어를 Masking 후 해당 단어를 맞히는 과정
- 양방향 정보를 이용하여 단어 예측
2. 문장 선후관계 예측
- 임의의 두 문장에 대해, 두 문장이 선/후 관계가 맞는지 맞히는 과정
※ 두 과정 모두 별도의 정답 없이 대용량 말뭉치 데이터로부터 자동으로 생성 가능

### Fine-tuning(응용 단계)
- 언어처리, 텍스트 분류, 기계독해 등에 적용
- 언어처리 : 개체명 인식, 구문 분석 등 언어처리 문제에 적용
- 문장분류 : 단일 문장 주제 분류 또는 두 문장 사이의 유사성 분석 문제에 적용
- 기계독해 : 질문과 단락을 입력 받은 후, 단락에서 정답 경계 인식 문제에 적용