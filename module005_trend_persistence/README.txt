# Module 005: Trend Persistence Analysis

## Status: Phase 1 - Trend Segmentation ✓

## Research Question
How long do BTC trends statistically persist?

## Null Hypothesis
**H0**: Trend direction is independent from candle to candle.

## Phase 1 Scope
Identifies consecutive directional movements (trends) in BTC returns.

### Implemented:
- ✅ Log returns calculation
- ✅ Trend direction assignment (+1/-1/0)
- ✅ Consecutive trend segmentation
- ✅ Trend length statistics (mean, median, max)
- ✅ Comparison to expected lengths under independence

### Output:
- `trend_segments.csv` - Each identified trend with start, end, direction, length
- `trend_summary.csv` - Summary statistics
- `statistics.csv` - All computed metrics

### Expected Under H0:
If direction is independent: expected trend length ≈ 2.0 candles
Observed/Expected ratio > 1.5 indicates significant trend persistence.

## Synthetic Validation:
- [x] Alternating directions → correctly detects short trends
- [x] Clustered directions → correctly detects long persistent trends

## Next Phase
**Phase 2**: Pullback detection within trends