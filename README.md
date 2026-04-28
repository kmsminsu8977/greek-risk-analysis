# Greek Risk Analysis

Greek 리스크 분석 프로젝트의 기본 연구 구조와 재현 가능한 baseline 산출물을 담은 저장소입니다.

**핵심 연구 질문**

> 기초자산과 변동성이 동시에 움직이면 보유 옵션 포지션 손익은 어떤 Greek에 가장 민감한가?

## 저장소 구조

```text
greek-risk-analysis/
├── src/                         # baseline 계산 로직과 실행 엔트리포인트
├── data/sample/                 # 합성 샘플 입력 데이터
├── docs/                        # 방법론과 해석 기준
├── notebooks/                   # 실행 흐름을 보여주는 최소 노트북
├── outputs/tables/              # 재현 가능한 결과 CSV
├── presentation/                # 발표/보고서 초안
└── references/                  # 재작성 개념 노트와 참고문헌 메모
```

## 빠른 시작

```bash
python -m src.run_baseline
```

실행 결과는 `outputs/tables/baseline_results.csv`에 저장됩니다.

## 구현 범위

- Black-Scholes Greek을 계산한 뒤 작은 충격에 대한 2차 근사 손익을 만든다.
- Delta는 방향성, Gamma는 곡률, Vega는 변동성 충격의 영향으로 분리한다.
- 수치는 포지션 규모와 충격 손익 연결을 보여주는 학습용 합성 포지션이다.

## 주요 파일

- `src/greek_risk_baseline.py`: 옵션 포지션의 Delta, Gamma, Vega 노출을 충격 시나리오 손익으로 연결한다.
- `data/sample/option_position_scenarios.csv`: baseline 실행용 합성 입력값
- `docs/methodology.md`: 계산 절차, 입력/출력 정의, 해석상 주의점
- `outputs/tables/baseline_results.csv`: 현재 baseline 산출물

## 다음 확장 방향

- 실제 공개 데이터 또는 별도 수집 데이터 연결
- notebook 기반 탐색 분석 추가
- 차트와 표를 포함한 최종 보고서 작성
- 모델 검증, 민감도 분석, 비용/리스크 가정 보강
