# Listado de tareas para el trabajo

## 1. Brainstorm features

### 1.1. Representing timestamps

### 1.2. Missing value treatment (deletion, mean, predict, knn)

* Me quedo con los valores como vienen.

* Falta analizar cómo toma LightGBM los valores nulos.

### 1.3 Create new ratios and proportions (tirar regresiones)

* Construyo los cocientes que armó Denicolay (ver cómo los hace).

* Incorporo la historia de los 6 meses anteriores. 

### 1.4 Binning/bucketing (crear intervalos para variables significativas)

* El LightGBM discretiza en 256 valores.

### 1.5 Reframe numerical quantities (convertir a cientos o miles de pesos)

* Esto lo puedo hacer para las variables monetarias. Sirve también para llevar a cero a todos los valores menores a mil.

### 1.6 Variable transformation (raíz cuadrada/cúbica o logaritmo - simetrizar distribuciones)

### 1.7 Outlier detection and treatment (detección de valores extremos)

* No voy a aplicar detección de valores extremos.

### 1.8 Decomposing categorical attrributes (binarización y one-hot encoding)

* Esto ya está mayormente hecho con el conjunto de variables originales.

## 2. Devise features

## 3. Select features

## 4. Evaluate features

### Feature crosses - fe_presente.R y fe_tendencia.R

### Feature importance

* Evalué la importancia en el modelo de abril con **lightgbm_final.R** y obtuve el siguiente ranking:
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

* Para la importancia en febrero con historia (construida con **fe_presente_abril.R** y **fe_tendencia_abril.R**) los primeros 10 son:
