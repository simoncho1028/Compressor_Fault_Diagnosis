# Paper
Explainable Multimodal Diagnostic Framework for Anomaly Classification and Predictive Maintenance in Industrial Compressors

## 📁 Directory Structure

```
.
├── raw_data/                      # 원본 진동 데이터
├── processed_data_raw/           # 전처리된 raw (1D) 데이터 (1번 코드 결과)
├── processed_data_stft/          # 전처리된 STFT (2D) 데이터 (1번 코드 결과)
├── shap_attention_results/       # SHAP 및 Attention Map 결과 (2번 코드 결과)
├── final_results/                # 모델별 5회 실험 평가 결과 (multimodal / 1D / 2D)
├── figures/                      # 논문 수록용 시각화 결과 (3번 코드 결과)
├── test_raw/                     # 테스트용 raw 파일 저장 폴더
├── 1. data_split_and_preprocess.ipynb  # 데이터 전처리 및 분할 코드
├── 2. main_code.ipynb                  # 모델 학습 및 평가 코드
└── 3. visualize.ipynb                  # 시각화 및 결과 해석 코드
```

## 📄 Code Overview

### `1. data_split_and_preprocess.ipynb`
- 원본 진동 데이터를 불러와 sliding window 기반 분할 수행
- 1D / STFT 형태로 전처리하여 각각 `processed_data_raw/`, `processed_data_stft/`에 저장

### `2. main_code.ipynb`
- Multimodal (1D + 2D Cross Attention), 1D TCN, 2D CNN 모델 학습
- 모델별 5회 학습 후 성능 저장
- SHAP 및 Attention 기반 해석 결과 저장 (`shap_attention_results/`)

### `3. visualize.ipynb`
- 대표 시계열 샘플에 대한 모델 해석 시각화
- 각 class별 raw shap, stft shap, attention map 결과 시각화# Compressor_Fault_Diagnosis
