# Aeration Tank Process Monitor
**Industrial biological wastewater treatment — two-stage activated sludge**
PET/PETF production · Q ≈ 250 m³/h · Total HRT ≈ 80 h · Surface mechanical aerators
## Project overview
This project applies data-driven process engineering to operational data
from a two-stage activated sludge system treating PET/PETF wastewater.

The methodology builds on statistical approaches from Makarau (2019) PhD thesis
(municipal groundwater monitoring) and extends them with industrial SPC methods.

**Monitoring points:**
| Point | Description |
| S10   | Inlet to stage 1 aeration tank |
| S23   | After stage 1 + secondary clarifier |
| S36   | After stage 2 + secondary clarifier (final effluent) |

## Key findings
Results will be updated as analysis progresses

## Analysis pipeline
| Phase | Description | Status |
| 0 | Environment setup + Git | ✅ |
| A | Data quality, outliers, descriptive stats, distributions, temporal patterns | 🔄 |
| B | STL decomposition, ACF/PACF, cross-correlation | ⏳ |
| C | SPC: X-MR charts, CUSUM, EWMA, Cp/Cpk | ⏳ |
| D | Correlation matrix, regression analysis | ⏳ |
| E | Efficiency analysis: waterfall, η vs load, F/M | ⏳ |
| F | Forecasting: SARIMA + NARX for inlet COD and outlet quality | ⏳ |
| G | OPEX: discharge fee, scenario analysis | ⏳ |
| H | GPS-X fractionation + CapdetWorks economic evaluation | ⏳ |

## Quick start
```
pip install -r requirements.txt
streamlit run streamlit_app/app.py
```

**Live dashboard:** [link when deployed]

## Data
Data not included due to confidentiality (industrial operational data).

## Methods
Statistical SPC: X-MR Shewhart, CUSUM, EWMA, Cp/Cpk
Time series: STL decomposition, ACF/PACF, SARIMA, NARX
Regression: MLR, polynomial, logistic
Economic: RF discharge fee methodology, CapdetWorks (GPS-X scenarios)

Stack: Python · pandas · scipy · statsmodels · plotly · Streamlit · GPS-X · CapdetWorks

*Author: Dzmitry Makarau | Water Treatment Process Engineer*
