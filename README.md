# Paper Notes

논문을 읽고 핵심 내용을 정리한 개인 학습/공유용 저장소입니다.  
각 논문별로 별도 폴더를 만들고, GitHub Pages로 바로 볼 수 있는 HTML 페이지를 함께 관리합니다.

## iTransformer

통신 KPI 예측과 이상 탐지 관점에서 `iTransformer` 논문을 정리했습니다.

- 논문: **iTransformer: Inverted Transformers Are Effective for Time Series Forecasting**
- arXiv: https://arxiv.org/abs/2310.06625
- DOI: https://doi.org/10.48550/arXiv.2310.06625
- 공식 코드: https://github.com/thuml/iTransformer

### 미리보기

- 개요 페이지: https://geonheeye.github.io/Paper/itransformer/
- Figure 2 설명: https://geonheeye.github.io/Paper/itransformer/figure2.html
- Figure 4 설명: https://geonheeye.github.io/Paper/itransformer/figure4.html

### 핵심 관점

기존 Transformer 기반 시계열 모델은 보통 시간 포인트를 token으로 보고 attention을 적용합니다.  
iTransformer는 이 관점을 뒤집어, 각 변수의 전체 lookback 구간을 하나의 token으로 보고 attention을 변수 간 관계 학습에 사용합니다.

통신 KPI처럼 여러 지표가 서로 영향을 주고받는 환경에서는 변수 간 상관관계를 잘 모델링하는 것이 중요합니다.  
따라서 iTransformer는 KPI 예측값과 실제값의 차이를 이용해 이상 유무를 판단하는 흐름에서 참고할 만한 중요한 backbone 모델입니다.

## 구조

```text
Paper/
├── README.md
└── itransformer/
    ├── index.html
    ├── figure2.html
    └── figure4.html
```
