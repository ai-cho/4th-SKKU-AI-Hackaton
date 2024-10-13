# 제4회 SKKU AI 해커톤
---

 [제4회 성균관대학교 AI 해커톤](https://sco.skku.edu/sco/community/notice.do?mode=view&articleNo=181479&article.offset=0&articleLimit=10)에서 진행한 프로젝트입니다. 
 
 **Contributors**
 - *김준령, 김현우, 이채은, 조정환*
 
---
### 데이터 소개

[AI Hub](https://www.aihub.or.kr/aihubdata/data/view.do?currMenu=115&topMenu=100&aihubDataSe=data&dataSetSn=71667) 데이터를 사용하였습니다.

본 프로젝트에서 사용된 데이터는 다음과 같은 정보를 포함하고 있습니다:
- **이미지 데이터**: 성충 및 유충 이미지
  
![image](https://github.com/user-attachments/assets/9662ba67-815d-4425-9ccd-3373cd71ec02)
- **JSON 데이터**: 온도, 습도, 이산화탄소 농도 시계열 값
  
![image](https://github.com/user-attachments/assets/d996cd86-4e6a-432d-a836-f947ba3bcb94)

---
### 모델 소개

#### 1. **Model 1** *using time series data*
- **입력 데이터**: 시계열 데이터 (내부 온도, 내부 습도, 내부 이산화탄소 농도)
- **목표**: 환경 데이터를 기반으로 특정 상태를 예측하는 시계열 분석 모델입니다.
- **사용 방법**: JSON 파일에서 시간에 따른 온도 및 습도, 이산화탄소 데이터를 추출하여 EfficientNet 모델을 학습시킵니다.
- **추가**: 시계열 특징 반영을 위한 LSTM Model code 추가
- [network.hdf5](https://github.com/ai-cho/4th-SKKU-AI-Hackaton/tree/master/training/model)

#### 2. **Model 2** *using image data*
- **입력 데이터**: 이미지 데이터
- **목표**: 주어진 이미지가 특정 범주에 속하는지 예측하는 이미지 분류 모델입니다.
- **사용 방법**: 이미지 데이터를 통해 각 클래스(예: 유충_부저병, 성충_정상 등)를 분류합니다.
- [bee_classification_efficientnet.pth](https://github.com/ai-cho/4th-SKKU-AI-Hackaton/tree/master/training/model)
- [bee_classification_resnet.pth](https://github.com/ai-cho/4th-SKKU-AI-Hackaton/tree/master/training/model)
