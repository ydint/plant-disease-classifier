# 🌿 Plant Disease Classifier

식물의 잎 사진을 입력 받아 15가지의 질병 혹은 건강 상태를 분류하는 딥러닝 기반 이미지 분류 프로젝트입니다.

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/15/Tomato_blight.jpg/640px-Tomato_blight.jpg" width="500"/>
</p>

---

## 📂 Dataset

- **출처**: [Kaggle - PlantVillage](https://www.kaggle.com/datasets/emmarex/plantdisease)
- 총 이미지 수: 약 26,000장
- 클래스 수: 15개 (병든 식물 + 정상 식물)

---

## 🧠 Model

- 사전학습된 ResNet18 모델을 활용하여 fine-tuning 수행
- 마지막 layer4와 fc 레이어만 학습하도록 설정 (Transfer Learning)

---

## ⚙️ 기술 스택

| 항목 | 내용 |
|------|------|
| 언어 | Python |
| 프레임워크 | PyTorch |
| 환경 | Google Colab |
| 기타 | torchvision, matplotlib, seaborn, sklearn |

---

## 📊 Results

- **Test Accuracy**: 99%
- 데이터 불균형 → WeightedRandomSampler로 해결
- EarlyStopping 적용

---

## 💡 회고 및 개선점

- 클래스 불균형을 처리하니 성능이 크게 향상되었다
- 데이터 증강은 소수 클래스에 더욱 효과적이었다
- 추후 Grad-CAM으로 시각화 + 모델 경량화 + 모바일 배포 고려 중

---

## ✅ 실행 방법

1. `plant-disease-classifier-final-eval.ipynb` 열기
2. Colab에서 순차적으로 셀 실행
3. test accuracy, confusion matrix, 시각화 결과 확인
