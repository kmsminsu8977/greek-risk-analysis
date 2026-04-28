# 발표 초안

## 1. 문제 정의

기초자산과 변동성이 동시에 움직이면 보유 옵션 포지션 손익은 어떤 Greek에 가장 민감한가?

## 2. 데이터와 가정

- 합성 샘플 데이터: `data/sample/option_position_scenarios.csv`
- 재현 가능한 baseline 실행을 우선 구성

## 3. 방법

옵션 포지션의 Delta, Gamma, Vega 노출을 충격 시나리오 손익으로 연결한다.

## 4. 현재 산출물

- 실행 스크립트: `python -m src.run_baseline`
- 결과 표: `outputs/tables/baseline_results.csv`

## 5. 후속 작업

- 실제 데이터 연결
- 민감도 분석
- 차트/보고서 산출
- 프로젝트별 상세 검증
