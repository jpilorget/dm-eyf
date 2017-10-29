# To-do list for the first deliver

## 1. Brainstorm features

### 1.1. Representing timestamps

### 1.2. Missing value treatment (deletion, mean, predict, knn)

* I'm not doing imputation.

* Analyze how LightGBM deals with missing values.

### 1.3 Create new ratios and proportions

* Build ratios with regressions written in C++ (they're way faster than R code) and actual variables.

* Add previous months (6?) variables. 

### 1.4 Binning/bucketing 

* Develop ranks for selected features.

* LightGBM already discretize some variables (into 256 categories).

### 1.5 Reframe numerical quantities 

* Turn quantities into hundreds or thousands. This allows to put together all the low values.

* Reframe days into months or months into years.

### 1.6 Variable transformation (raíz cuadrada/cúbica o logaritmo - simetrizar distribuciones)

### 1.7 Outlier detection and treatment

* I won't, in this instance, try to detect any outliers

### 1.8 Decomposing categorical attrributes

* Binarization and one-hot encoding is done in almost all variables that need it in the original dataset.

## 2. Devise features

## 3. Select features

## 4. Evaluate features

### Feature crosses - fe_presente.R y fe_tendencia.R

### Feature importance

* I made an importance rank using **lightgbm_final.R** and got the following ordered attributes:
1. mpasivos_margen
2. Visa_Finiciomora
3. Visa_marca_atraso
4. mcaja_ahorro_Paquete
5. tmovimientos_ultimos90dias
6. Master_Finiciomora
7. mcuenta_corriente_Paquete
8. mcuentas_saldo
9. Visa_mpagospesos
10. mtarjeta_visa_consumo

* Need to check the most important attributes using **fe_presente_abril.R** and **fe_tendencia_abril.R**.
