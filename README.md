# Aeration Tank Process Monitor
**Industrial biological wastewater treatment — two-stage activated sludge**
Chemical manufacturing facility  · Q ≈ 210 m³/h · Total HRT ≈ 80 h · Surface mechanical aerators
## Project overview
This project applies data-driven process engineering to operational data
from a two-stage activated sludge system treating industrial wastewater from chemical production.
⚠️ Data notice: All data used in this repository are synthetic and anonymized. They preserve the statistical properties, correlations, and temporal patterns of real industrial measurements but contain no actual plant-confidential information. Results are for methodological demonstration only.

The methodology builds on statistical approaches from Makarau (2019) PhD thesis
(municipal groundwater monitoring) and extends them with industrial SPC methods.

**Monitoring points:**
| Point | Description |
| S0   | Inlet to stage 1 aeration tank |
| S1   | After stage 1 + secondary clarifier |
| S2   | After stage 2 + secondary clarifier (final effluent) |

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

**Live dashboard:** [link when deployed]

## Data
**Not real — statistically preserved synthetic dataset.**

To enable open sharing while respecting industrial confidentiality, the original operational data were transformed into an anonymized synthetic version using a privacy-preserving generation method.

## Methods
Statistical SPC: X-MR Shewhart, CUSUM, EWMA, Cp/Cpk
Time series: STL decomposition, ACF/PACF, SARIMA, NARX
Regression: MLR, polynomial, logistic
Economic: RF discharge fee methodology, CapdetWorks (GPS-X scenarios)

Stack: Python · pandas · scipy · statsmodels · plotly · Streamlit · GPS-X · CapdetWorks

*Author: Dzmitry Makarau | Water Treatment Process Engineer*
