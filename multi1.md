최근 얼굴인식 기술 동향과 대표 모델 성능 비교

박지희*, 심재창**
*디제이패밀리
**국립경국대학교 컴퓨터공학과
e-mail : wg9382@djfamilygroup.com

Recent Trends and Application-Oriented Advances in Face Recognition: A Comparative Study of Lightweight and Quality-Aware Models

Jihee Park*, Jaechang Shim**
*DJ Family
**Dept of Computer Engineering, Gyeongkuk National University

1. 연구 필요성 및 문제점
얼굴인식 기술은 개인 인증, 보안 감시, 디지털 접근 제어 등 다양한 분야에서 널리 활용되고 있으며, 특히 딥러닝 기반 모델들이 높은 정확도로 주목받고 있다. ArcFace, CosFace, FaceNet과 같은 모델은 기존 얼굴인식의 성능 한계를 뛰어넘으며 기술 발전의 기반이 되었다. 이후 연구는 완전히 새로운 구조 제안보다는 기존 모델을 다양한 환경에 적용하고 실질적 문제를 해결하는 방향으로 전개되고 있다.

특히, 최근 연구는 경량화, 품질 인식, 프라이버시 보장 등 실용적 목적을 중심으로 진행되고 있으며, 이는 실제 적용 가능성을 높이는 데 기여하고 있다. 본 논문은 이러한 응용 지향적 접근을 바탕으로 최근 발표된 대표 모델들을 선정하고, 다양한 벤치마크 환경에서 보고된 성능을 정량적으로 비교함으로써 기술 동향을 체계적으로 분석한다. 아울러 각 모델의 적용 가능성과 기술적 특징에 대한 고찰을 통해 향후 연구 방향에 대한 시사점을 제공하고자 한다.

2. 연구 내용과 방법
본 논문은 최근 발표된 응용 기반 얼굴인식 모델 중 경량화, 통합 손실 함수, 품질 인식 기반 접근을 대표하는 세 가지 모델을 비교 대상으로 선정하였다.

- EdgeFace [1]: ArcFace 기반 구조에 EdgeNeXt를 적용하여 모델 경량화에 최적화된 구조를 제안. 특히 엣지 디바이스에서의 실시간 추론에 적합.
- UniTSFace [2]: 샘플 간 거리 기반의 통합 임계값 손실 함수를 통해 다양한 조건에서의 일반화 성능을 강화.
- QMagFace [3]: 이미지 품질을 임베딩 벡터의 크기로 해석하여, 품질 인식 기반 학습을 통해 고정밀 인식을 가능케 함.

각 모델에 대해 적용된 기술적 전략과 구조를 간략히 설명하고, 성능 평가에 사용된 벤치마크 데이터셋(LFW, IJB-B, IJB-C, AgeDB, CFP-FP, XQLFW)에 대한 주요 특징을 정리하였다. 벤치마크별 과제 특성(예: 동일인 식별, 연령 차 극복, 포즈 다양성 등)과 평가 지표는 기존 연구 기준에 따라 정리하였다.

표 1. 얼굴인식 응용 모델 성능 비교

| 모델명     | 벤치마크 데이터셋 | 정확도 (%) |
|------------|--------------------|-------------|
| EdgeFace   | LFW               | 99.73       |
|            | IJB-B              | 92.67       |
|            | IJB-C              | 94.85       |
| UniTSFace  | LFW               | 99.83       |
|            | CFP-FP             | 96.31       |
|            | AgeDB              | 98.15       |
| QMagFace   | AgeDB              | 98.50       |
|            | XQLFW              | 83.95       |
|            | CFP-FP             | 98.74       |

각 모델의 성능은 대부분의 벤치마크에서 95% 이상의 높은 정확도를 보이고 있으며, QMagFace는 품질 기반 접근을 통해 특히 AgeDB와 CFP-FP에서 우수한 성능을 달성하였다. UniTSFace는 다양한 조건에서도 안정적인 성능을 유지하며, EdgeFace는 리소스 제약 환경에서의 활용 가능성을 보여준다.

3. 결론 및 향후 연구
본 논문은 얼굴인식 기술의 최근 흐름을 경량화, 품질 인식, 손실 함수 설계 등 실용적 요소에 초점을 맞추어 고찰하였다. 단순한 정확도 향상을 넘어서 다양한 환경에서의 실용성을 추구하는 응용 중심 접근은 다음과 같은 향후 연구 방향을 제시한다.

- 초경량 모델 및 실시간 처리 모델 개발 (특히 엣지/모바일 환경)
- 합성 데이터 및 품질 기반 정규화 전략 도입
- 생체정보 보호 및 프라이버시 보장 학습 기술 강화
- 다양한 평가 지표와 실제 사용자 환경에서의 테스트 수행

본 연구는 세 가지 대표 모델에 대한 기술적 비교 및 분석을 통해 얼굴인식 기술의 현재 위치를 조망하고, 향후 응용 가능성과 연구 방향에 대한 체계적 관점을 제공한다. 특히, 모델 선택 기준과 평가 지표의 설명, 그리고 정량적 비교를 통해 실제 적용 시 고려해야 할 요소들을 명확히 하였다.

참고문헌
[1] A. George, C. Ecabert, H. Shahreza et al., "EdgeFace: Efficient Face Recognition Model for Edge Devices," arXiv preprint, arXiv:2307.01838, 2023.  
[2] Q. Li, X. Jia, J. Zhou et al., "UniTSFace: Unified Threshold Integrated Sample-to-Sample Loss for Face Recognition," arXiv preprint, arXiv:2311.02523, 2023.  
[3] P. Terhörst, M. Ihlefed, M. Huber et al., "QMagFace: Simple and Accurate Quality-Aware Face Recognition," arXiv preprint, arXiv:2111.13475, 2021.

