# Sample Data

이 폴더의 `option_position_scenarios.csv`는 baseline 계산을 검증하기 위해 만든 합성 데이터입니다.

## Columns

- `scenario_id`
- `spot`
- `strike`
- `rate`
- `volatility`
- `maturity`
- `option_type`
- `position_contracts`
- `contract_multiplier`
- `shock_spot_pct`
- `shock_vol_abs`

## Usage

```bash
python -m src.run_baseline
```

