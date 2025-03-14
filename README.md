# LSTM-Based Prediction for Chemical Production

## Project Overview
This project focuses on using an [LSTM](w) model to predict key chemical production outputs based on timeseries data from multiple reactors. The dataset consists of hourly resolution data collected over a year, totaling **37,728 samples** from **six reactors**.

![Forecasting](https://github.com/batxes/Chemical-Production-Forecasting/blob/master/figures/evaluation_model_reactor_2_target_2%7CCB.pdf)

## Dataset
Each sample contains multiple sensor readings. For example, Reactor 2 includes:

- CB 2
- Erdgas 2
- Konst.Stufe 2
- Perlwasser 2
- Regelstufe 2
- Sorte 2
- V-Luft 2
- VL Temp 2
- Fuelöl 2
- Makeöl 2
- Makeöl Temperatur 2
- Makeöl Ventil 2
- CCT 2
- CTD 2
- FCC 2
- SCT 2
- C 2, H 2, N 2, O 2, S
- CO2 R2, SO2 R2

Additionally, some values are common across all six reactors:

- KD|Dampfmenge, KD|Restgasmenge, KD|NOx, KD|Rauchgasmenge, KD|SO2
- KE|Dampfmenge, KE|Restgasmenge, KE|NOx, KE|Rauchgasmenge, KE|SO2

## Prediction Task
The goal is to predict the following **output variables**:
- **CB** (the product)
- **SO₂**
- **CO₂**
- **Dampfmenge** (steam)
- **Rauchgasmenge** (tail gas, all reactors combined)

### Input Variables
The input consists of all available sensor values except for the shared reactor-independent values:
- KD|Dampfmenge, KD|Restgasmenge, KD|NOx, KD|Rauchgasmenge, KD|SO2
- KE|Dampfmenge, KE|Restgasmenge, KE|NOx, KE|Rauchgasmenge, KE|SO2

## Summary
Developed an [LSTM](w) model to predict key chemical production outputs from multivariate timeseries data (37,728 samples, six reactors), optimizing industrial process forecasting.


